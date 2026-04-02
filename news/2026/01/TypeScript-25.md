# Report for 2026-01-25 (Sunday, January 25th, 2026)

7 different users commented on 6 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936) (Open, `Suggestion`, `Awaiting More Feedback`)

**Exact Types**

*Introduce an Exact<T> type (e.g. |T|) to enforce exact object types and disallow extra properties.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3795201973) **reverofevil** pointed out that TS is a static analyzer without typing, noted that OCaml already implements exact objects, and urged readers to avoid adding more comments
 * [yesterday](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3795201973) **reverofevil** pointed out that TS is a static analyzer without typing, noted that OCaml already implements exact objects, and urged readers to avoid adding more comments
 * [yesterday](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3795201973) **reverofevil** pointed out that TS is a static analyzer without typing, noted that OCaml already implements exact objects, and urged readers to avoid adding more comments
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve

### [Issue microsoft/TypeScript#63050](https://github.com/microsoft/TypeScript/issues/63050) (Open)

**Double error message when referencing variable of type union of string literals from ambient declaration**

*TypeScript 4.0.5 duplicates the same error message when assigning an ambient string-literal union to a number.*

 * created by **devanshj**
 * [later](https://github.com/microsoft/TypeScript/issues/63050#issuecomment-3798773309) **Andarist** pointed out the location where the source gets generalized and noted that the code is not union-aware and stems from a TypeScript PR

### [Issue microsoft/TypeScript#63051](https://github.com/microsoft/TypeScript/issues/63051) (Open)

**tsgo fails to report TS2769 for mutually\-exclusive object overloads**

*tsgo does not report TS2769 for mutually exclusive object overloads while tsc correctly flags the error.*

 * created by **r253hmdryou**
 * [today](https://github.com/microsoft/TypeScript/issues/63051#issuecomment-3796895410) **jcalz** said "Question for TS team... is https://tsgo.sxzz.dev is an acceptable playground for tsgo? "
 * [today](https://github.com/microsoft/TypeScript/issues/63051#issuecomment-3796914886) **r253hmdryou** filed a duplicate issue in microsoft/typescript-go to track tsgo-specific behavior

### [PR microsoft/TypeScript#63052](https://github.com/microsoft/TypeScript/pull/63052) (Closed, `For Backlog Bug`)

**feat: comprehensive Type Hierarchy LSP support**

*Implement comprehensive LSP Type Hierarchy support in the TypeScript service, enabling supertype and subtype navigation for classes, interfaces, and type aliases.*

 * created by **kbrilla**
 * [today](https://github.com/microsoft/TypeScript/pull/63052#issuecomment-3796857635) **typescript-bot** thanked the author for the PR, cautioned to preserve TSServer API compatibility, and pinged reviewers for extra review
 * [today](https://github.com/microsoft/TypeScript/pull/63052#issuecomment-3796857654) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63052#issuecomment-3796928352) **kbrilla** said "@microsoft-github-policy-service agree"
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63052#issuecomment-3796968192) **jakebailey** advised that the PR would not be accepted and suggested sending it to the typescript-go repo or waiting until this repo becomes the Go code
 * [today](https://github.com/microsoft/TypeScript/pull/63052#issuecomment-3796975568) **kbrilla** acknowledged the suggestion and thanked the contributor for the information

### [PR microsoft/TypeScript#63053](https://github.com/microsoft/TypeScript/pull/63053) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 2 updates**

*Upgrade GitHub Actions group by bumping actions/checkout from 6.0.1 to 6.0.2 and updating the github/codeql-action.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

