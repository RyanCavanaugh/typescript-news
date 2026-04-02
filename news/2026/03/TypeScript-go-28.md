# Report for 2026-03-28 (Saturday, March 28th, 2026)

5 different users commented on 21 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4100406855) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4113812716) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4114084080) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4148801620) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."

### [Issue microsoft/TypeScript-go#3204](https://github.com/microsoft/TypeScript-go/issues/3204) (Closed, `Crash`, **DanielRosenwasser**, **jakebailey**, **Copilot**)

**Panic with \`declarationMap\` in version 7\.0\.0\-dev\.20260323\.1**

*typescript-go 7.0.0-dev.20260323.1 panics with a slice bounds out of range error in scanner.SkipTriviaEx while generating declarationMap*

 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4144076140) **jakebailey** said "The changes I have do not actually fix this issue. (referring to a different branch; #3274 should fix this)"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3274](https://github.com/microsoft/TypeScript-go/pull/3274) (Closed)

**Fix declarationMap crash, text ranges**

*Improves text range handling in declarationMap to prevent crashes and resolve related bugs.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3276](https://github.com/microsoft/TypeScript-go/issues/3276) (Closed, `bug`, **ahejlsberg**)

**Intermittent typecheck error on optional inline object method parameter**

*tsgo intermittently produces a typecheck error for an optional inline object method parameter in a large TypeScript codebase*

 * (yesterday) **RyanCavanaugh** added label `bug`, and assigned to **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3276#issuecomment-4145837663) **RyanCavanaugh** described Copilot’s proposed fix to skip the type cache for binding elements and outlined the root cause involving optional types being cached due to goroutine scheduling
 * [today](https://github.com/microsoft/TypeScript-go/issues/3276#issuecomment-4149006743) **ahejlsberg** asserted that the Copilot suggestion was reasonable and that cached types cannot be reused for optional variables indistinguishable from undefined, thus requiring type resolution to be redone
 * [today](https://github.com/microsoft/TypeScript-go/issues/3276#issuecomment-4149008229) **ahejlsberg** said "I turned the suggestion into a PR in #3288."
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3282](https://github.com/microsoft/TypeScript-go/pull/3282) (Closed)

**Don't send progress reports for very short spans**

*Add a 250ms delay before sending progress tokens to prevent excessive reporting for very short spans.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3283](https://github.com/microsoft/TypeScript-go/pull/3283) (Closed)

**Fix TS1127 Invalid character error span width to match Strada**

*Change the Go scanner’s TS1127 invalid-character error span from the character size to zero to match TypeScript*

 * created by **samuelafblis**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3283#issuecomment-4148719416) **samuelafblis** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3283#issuecomment-4148729681) **samuelafblis** said "Closing — this is a low-value cosmetic baseline change. Will pursue more impactful convergence fixes instead."
 * (today) **samuelafblis** closed the issue

### [PR microsoft/TypeScript-go#3284](https://github.com/microsoft/TypeScript-go/pull/3284) (Closed)

**Use dot notation for internal symbol names in qualified paths**

*Update canUsePropertyAccess to recognize internal symbol prefixes, allowing dot notation for internal symbol names.*

 * created by **samuelafblis**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3284#issuecomment-4148719454) **samuelafblis** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3284#issuecomment-4148729727) **samuelafblis** said "Closing — purely test infrastructure formatting, no user-facing impact. Will pursue more impactful convergence fixes instead."
 * (today) **samuelafblis** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3284#issuecomment-4148735462) **jakebailey** criticized using Claude to send PRs without local review and questioned alt account usage

### [PR microsoft/TypeScript-go#3285](https://github.com/microsoft/TypeScript-go/pull/3285) (Closed)

**Remove GetOptionsDiagnostics, global diags in editor, restore checker affinity**

*Remove GetOptionsDiagnostics, expose global diagnostics to the editor, restore consistent checker affinity, and simplify the CheckerPool interface.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3286](https://github.com/microsoft/TypeScript-go/pull/3286) (Closed)

**Port per\-overload error elaboration for 2\-3 candidates**

*Display individual diagnostic errors for each of two to three function overloads instead of only the last one.*

 * created by **samuelafblis**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3286#issuecomment-4148777620) **samuelafblis** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3286#issuecomment-4148850092) **jakebailey** said "This is intentional "
 * (today) **samuelafblis** closed the issue

### [PR microsoft/TypeScript-go#3287](https://github.com/microsoft/TypeScript-go/pull/3287) (Closed)

**Fix rename crash on quoted single\-character property names**

*Prevent crash when renaming quoted single-character property names in TypeScript code*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3288](https://github.com/microsoft/TypeScript-go/pull/3288) (Closed)

**Fix binding element phantom error**

*Remove incorrect reuse of cached types for binding element parents to fix phantom error.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3289](https://github.com/microsoft/TypeScript-go/pull/3289) (Open)

**Fix organize imports crash with traceResolution**

*Fixes the crash occurring during organize imports when traceResolution is enabled.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3290](https://github.com/microsoft/TypeScript-go/pull/3290) (Closed)

**Fix call hierarchy harness crash on signatures from lib files**

*Corrects a crash in the call hierarchy harness when processing signatures from library files.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3291](https://github.com/microsoft/TypeScript-go/pull/3291) (Closed)

**Fix import require error**

*Update error reporting to remove TypeScript references in JavaScript files and eliminate unused parameters in error methods.*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#945](https://github.com/microsoft/TypeScript-go/issues/945) (Closed, `Domain: Editor`)

**\[feat\]\[lsp\] add support for custom config file name\(s\)**

*Allow the tsgo LSP to search for customizable TypeScript config filenames instead of only tsconfig.json.*

 * created by **mjames-c**
 * **jakebailey** added label `LSP`
 * [30 weeks ago](https://github.com/microsoft/TypeScript-go/issues/945#issuecomment-3226879292) **johnnycheng0210** mentioned a proposed feature change, asked about the flow to request reviewers, and noted that the contributing doc was unclear
 * [today](https://github.com/microsoft/TypeScript-go/issues/945#issuecomment-4149419765) **jakebailey** said "This was done in #2020"
 * (today) **jakebailey** closed the issue

