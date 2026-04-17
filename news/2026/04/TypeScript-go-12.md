# Report for 2026-04-12 (Sunday, April 12th, 2026)

5 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @jbeaudoin-lf provided version details and error output in [microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4236896401)
    * @vetptzru asked if the concurrency limit could be made configurable via tsgo/VSCode in [microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4235424817)

## Activity Summary

### [Issue microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685) (Closed, `Domain: Type Checking`, `Domain: JS`, **sandersn**)

**\`ts\-check\` used with \`@typedef\` causes an error on \`module\.exports = \.\.\.\`**

*Combining @ts-check and @typedef in a CommonJS file causes a TS2309 export assignment error with tsgo.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4218381008) **RyanCavanaugh** said "No longer repros with recent changes"
 * (3 days ago) **RyanCavanaugh** closed the issue
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4218922623) **jbeaudoin-lf** said "Thanks, gonna give it a try tomorrow then !"
 * [later](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4236896401) **jbeaudoin-lf** asked which version was used and provided the version output and resulting error messages

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Closed, `Needs More Info`, **jakebailey**)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4209932096) **jakebailey** proposed testing pull request 3369 to address potential thread limit issues due to blocking syscalls on macFUSE
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4215019134) **vetptzru** reported that the fix resolved crashes and reduced the macFUSE thread count to under 26
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4215101482) **jakebailey** said "I'm not sure if that's going to be the fix, as it very much hurts everyone else's perf."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4235424817) **vetptzru** proposed making the concurrency limit configurable to allow teams using macFUSE to opt in while keeping default unbounded performance for native filesystems
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4237328560) **jakebailey** rejected adding a flag and asked to retry the PR after recent changes

### [Issue microsoft/TypeScript-go#3372](https://github.com/microsoft/TypeScript-go/issues/3372) (Closed, **jakebailey**, **Copilot**)

**Not having dependency for type should make tsgo error**

*tsgo does not report an error when required Node type definitions are missing despite tsconfig specifying them, unlike tsc.*

 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (2 days ago) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3372#issuecomment-4237298663) **alexsch01** said "Working good!"

### [PR microsoft/TypeScript-go#3387](https://github.com/microsoft/TypeScript-go/pull/3387) (Closed)

**Typecheck scripts, fix convertFourslash**

*Enable typechecking of scripts in CI and incorporate the convertFourslash fix from PR 3304.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3392](https://github.com/microsoft/TypeScript-go/pull/3392) (Closed, `dependencies`, `github_actions`)

**Bump actions/upload\-artifact from 7\.0\.0 to 7\.0\.1 in the github\-actions group across 1 directory**

*Update actions/upload-artifact from version 7.0.0 to 7.0.1 in the GitHub Actions configuration*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

