# Report for 2026-08-05 (Wednesday, August 5th, 2026)

8 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @goldserg provided repro steps and details that require acknowledgment in [microsoft/TypeScript-go#3481](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-5203497587)

## Activity Summary

### [Issue microsoft/TypeScript-go#3481](https://github.com/microsoft/TypeScript-go/issues/3481) (Open, `help wanted`)

**Corsa differences in \`export=\` module augmentation**

*Corsa changes how export= module augmentation works, causing differences in exported name visibility.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4642469732) **apostate0** described that augmentExportEquals2.errors.txt.diff wasn't a real bug but caused by duplicate filename directives and asked why they're used; identified a real semantic regression in exportAssignmentMembersVisibleInAugmentation.errors.txt.diff due to module augmentation symbol lookup and suggested a root cause in checker.go
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4688695434) **hesam-oxe** offered to investigate the augmentation merge issue by examining checker.go:1409-1438 and tracing through getAccessibleSymbolChain and merge logic to fix binding propagation
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4688740491) **hesam-oxe** opened PR #4291 that fixed mergeModuleAugmentation symbol propagation by copying main module exports, initializing target exports, including parent exports, and enabling recursive parent search
 * [later](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-5203497587) **goldserg** described a real-world instance where augmenting PlatformPath from @types/node silently stopped applying in TS 7.0.2 and provided reproduction steps, expected vs actual outcomes, version comparisons, and additional notes

### [PR microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313) (Open)

**Assign checkers with cost/import\-aware algorithm**

*Develop a cost- and import-aware algorithm to assign diagnostic checkers more efficiently.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5149687767) **typescript-automation[bot]** reported that perf test started and provided build and results links
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5149784101) **typescript-automation[bot]** reported the performance run results in a comparison report
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5172557530) **walkerdb** reported that after reverting PR 4309, the build ran ~10% faster and used ~10% less RAM on a large monorepo
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5194974744) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5194975562) **typescript-automation[bot]** started CI jobs and posted status update
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5195258586) **typescript-automation[bot]** posted the requested perf run results with a detailed comparison report

### [PR microsoft/TypeScript-go#4732](https://github.com/microsoft/TypeScript-go/pull/4732) (Closed, `dependencies`, `javascript`)

**Bump fast\-uri from 3\.1\.2 to 3\.1\.4**

*Upgrade fast-uri dependency from version 3.1.2 to 3.1.4 to include security fixes.*

 * (1 week ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4732#issuecomment-5197877683) **dependabot[bot]** said "Superseded by #4833."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript-go#4820](https://github.com/microsoft/TypeScript-go/pull/4820) (Closed)

**Order variance computation by associated type symbol**

*Variance computation is now ordered by associated type symbol to ensure stable results for circular generic types.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5189135428) **typescript-automation[bot]** reported the start and status of build jobs with result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5189383192) **typescript-automation[bot]** reported the requested perf run results to @ahejlsberg
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5189882951) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the pull request merge showed everything looked good
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4830](https://github.com/microsoft/TypeScript-go/issues/4830) (Open, `Domain: API and Extensibility`)

**API feature roadmap**

*Proposed API roadmap for TypeScript 7.1 detailing TS Server plugin replacements and top-level utility API features.*

 * created by **andrewbranch**
 * **andrewbranch** added label `Domain: API and Extensibility`
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`

### [PR microsoft/TypeScript-go#4832](https://github.com/microsoft/TypeScript-go/pull/4832) (Open, **RyanCavanaugh**, **Copilot**)

**Report TS1518 for all negated Unicode\-set union operands**

*Negated Unicode-set unions in v-mode now report TS1518 errors for any operand that may match multiple characters, irrespective of operand order*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4833](https://github.com/microsoft/TypeScript-go/pull/4833) (Open, `dependencies`, `javascript`)

**Bump fast\-uri from 3\.1\.2 to 3\.1\.5**

*Bump fast-uri from 3.1.2 to 3.1.5 to apply critical security fixes.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

### [Issue microsoft/TypeScript-go#4834](https://github.com/microsoft/TypeScript-go/issues/4834) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**Default concurrent mode misses TS2307 that \`\-\-singleThreaded\` \(and TS 6\.0\) report, for import/export declarations inside non\-scope blocks**

*TypeScript's default concurrent mode omits TS2307 "Cannot find module" errors for import/export declarations inside non-scope blocks, unlike singleThreaded mode and TS 6.0.*

 * created by **mohsen1**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `Post-7.0`, assigned to **Copilot**, **RyanCavanaugh**, **Copilot**, and unassigned **Copilot**

### [PR microsoft/TypeScript-go#4835](https://github.com/microsoft/TypeScript-go/pull/4835) (Closed, **RyanCavanaugh**, **Copilot**)

**Preserve TS2307 in concurrent mode for import/export declarations inside non\-scope blocks**

*Restore module-resolution diagnostics TS2307 for import/export declarations in non-scope blocks under concurrent mode without altering TS1233 placement errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4836](https://github.com/microsoft/TypeScript-go/pull/4836) (Open, **RyanCavanaugh**, **Copilot**)

**Preserve nested module resolution diagnostics in concurrent mode**

*Restore TS2307 diagnostics for import/export declarations in non-scoped blocks during concurrent mode by deferring module resolution and updating CLI baselines.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4837](https://github.com/microsoft/TypeScript-go/issues/4837) (Open)

**\[API\] Narrow types of \`Node\` attributes when possible**

*Proposes narrowing Node attribute types in TS 7 by restoring specific typings for JSDocTypedefTag parent, typeExpression, and Node jsDoc.*

 * created by **Gerrit0**

### [Issue microsoft/TypeScript-go#4838](https://github.com/microsoft/TypeScript-go/issues/4838) (Open)

**\`tsc \-\-watch\` can't handle errors across files**

*TypeScript’s watch mode fails to detect cross-file errors when a variable declaration is removed in a dependent file.*

 * created by **Withered-Flower-0422**

