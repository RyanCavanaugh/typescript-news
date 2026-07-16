# Report for 2026-07-10 (Friday, July 10th, 2026)

3 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @ayosec asked if the issue should be moved to the microsoft/TypeScript repository in [microsoft/TypeScript#63648](https://github.com/microsoft/TypeScript/issues/63648#issuecomment-4985206740)

## Activity Summary

### [Issue microsoft/TypeScript#63094](https://github.com/microsoft/TypeScript/issues/63094) (Closed, `Bug`, `Help Wanted`, `Domain: Decorators`)

**Crash: Debug Failure\. False expression in getArgumentArityError when resolving overloaded decorators with \-\-experimentalDecorators**

*TypeScript crashes with a 'Debug Failure. False expression' error in getArgumentArityError when resolving overloaded decorators under --experimentalDecorators.*

 * (20 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Decorators`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63094#issuecomment-4939620640) **Andarist** said "@RyanCavanaugh this no longer reproduces in ts-go, it can likely be closed"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63627](https://github.com/microsoft/TypeScript/issues/63627) (Open, `Needs Investigation`, **ahejlsberg**)

**\`NoInfer\` changes behavior for type matching on spread**

*Applying NoInfer to spread types unexpectedly produces type errors whereas equivalent spreads without NoInfer succeed*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, removed label `Not a Defect`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/issues/63627#issuecomment-4939682173) **Andarist** said "This strongly overlaps with https://github.com/microsoft/TypeScript/issues/59668"

### [PR microsoft/TypeScript#63629](https://github.com/microsoft/TypeScript/pull/63629) (Closed, `For Milestone Bug`, `Voight-Kampff Anomaly`, **gabritto**)

**fix\(formatting\): recover from token spans outside property children**

*Recover from tokens overrunning node boundaries by fixing the formatting recursion guard in processChildNode and adding a regression test.*

 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * (3 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript/pull/63629#issuecomment-4939027264) **RyanCavanaugh** informed that the TypeScript repo was closed for development and directed the PR to the typescript-go repo referencing CONTRIBUTING.md and issue #62963
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63638](https://github.com/microsoft/TypeScript/pull/63638) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Fix inconsistent \`typeof this\` when \`this\` parameter comes from a contextual signature \(\#63616\)**

*TypeScript incorrectly resolves typeof this as the enclosing type instead of the contextual this in type queries.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63638#issuecomment-4924177988) **AmariahAK** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [today](https://github.com/microsoft/TypeScript/pull/63638#issuecomment-4937571940) **RyanCavanaugh** informed that the TypeScript repo was closed for development and directed the PR to the typescript-go repo referencing CONTRIBUTING.md and issue #62963
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63642](https://github.com/microsoft/TypeScript/issues/63642) (Open, `Bug`, `Domain: check: Control Flow`)

**TS2871 'always nullish' false positive on binding destructured from \.map over spread\-of\-union \(regression 5\.9\.3 → 6\.0\.3; also in 7\.0\.2\)**

*TypeScript 6.0.3 and 7.0.2 incorrectly report a map-destructured ternary over a spread union as always nullish.*

 * created by **nejim123**
 * [today](https://github.com/microsoft/TypeScript/issues/63642#issuecomment-4937170024) **RyanCavanaugh** provided a smaller repro with a concise TypeScript snippet
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: check: Control Flow`

### [Issue microsoft/TypeScript#63648](https://github.com/microsoft/TypeScript/issues/63648) (Open)

**Some colors make error messages hard to read on white backgrounds\.**

*Diagnosticwriter’s forced bright ANSI color codes make error messages illegible on white backgrounds and should use default colors instead.*

 * created by **ayosec**
 * [today](https://github.com/microsoft/TypeScript/issues/63648#issuecomment-4985206698) **jakebailey** questioned whether the issue was new in v7 and linked to existing code
 * [today](https://github.com/microsoft/TypeScript/issues/63648#issuecomment-4985206740) **ayosec** noted that the issue also existed in the original compiler and asked if it should be moved to the microsoft/TypeScript repository

