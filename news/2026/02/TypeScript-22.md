# Report for 2026-02-22 (Sunday, February 22nd, 2026)

10 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @Meligy asked if additional setup was needed to support .scss imports in [microsoft/TypeScript#62443](https://github.com/microsoft/TypeScript/pull/62443#issuecomment-3942579353)

## Activity Summary

### [Issue microsoft/TypeScript#61768](https://github.com/microsoft/TypeScript/issues/61768) (Open, `Bug`, `Domain: lib.d.ts`, **sandersn**)

**\`IntegerTypedArray\` type required for use with \`crypto\.getRandomValues\`**

*crypto.getRandomValues TypeScript definitions need to restrict parameters to integer typed arrays and exclude null and float arrays.*

 * (37 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and assigned to **sandersn**
 * [later](https://github.com/microsoft/TypeScript/issues/61768#issuecomment-3945060746) **aryzing** mentioned that the same would apply to crypto.subtle.importKey and linked the MDN documentation

### [PR microsoft/TypeScript#62443](https://github.com/microsoft/TypeScript/pull/62443) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Enable \`noUncheckedSideEffectImports\` by default**

*Enable the noUncheckedSideEffectImports flag by default to address the complications in PR #62442 and resolve issue #62421.*

 * [23 weeks ago](https://github.com/microsoft/TypeScript/pull/62443#issuecomment-3286845857) **jakebailey** suggested that it was probably fine not to take action, noted that DT cases needed fixing, and asked if the results meant ignoring these in declaration files
 * [23 weeks ago](https://github.com/microsoft/TypeScript/pull/62443#issuecomment-3287110571) **RyanCavanaugh** said "Erroring in .d.ts files is still correct IMO, since if it's not yours it's almost certainly suppressed by skipLibCheck"
 * (21 weeks ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/62443#issuecomment-3942579353) **Meligy** mentioned that .scss imports broke despite fake modules and asked if additional steps were needed to make them work
 * [today](https://github.com/microsoft/TypeScript/pull/62443#issuecomment-3942786193) **jakebailey** suggested turning off the flag or adding a TypeScript declaration for CSS modules and shared example links
 * [today](https://github.com/microsoft/TypeScript/pull/62443#issuecomment-3942787136) **jakebailey** requested filing an issue with a repro if the problem occurred

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3868769997) **DanielRosenwasser** said "@typescript-bot create release-6.0"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3868770106) **typescript-bot** reported build jobs starting and provided links to status and results
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3868792183) **typescript-bot** said "Hey, @DanielRosenwasser! I've created release-6.0 with version 6.0.0-beta for you."
 * [later](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3944591376) **HolgerJeromin** noted that the PR also deprecated --module=none and questioned whether it is less-used in the wild

### [Issue microsoft/TypeScript#63162](https://github.com/microsoft/TypeScript/issues/63162) (Closed, `Duplicate`)

**Module resolution: Extension required when moduleResolution=bundler and imports/exports used**

*TypeScript's bundler moduleResolution requires explicit .js extensions for imports and exports, causing build-time failures despite working in Vite.*

 * created by **polson136**
 * [today](https://github.com/microsoft/TypeScript/issues/63162#issuecomment-3940793062) **darshjme-codes** said "Triage: Module resolution error requiring extension Labels: Bug, Module Resolution, Suggestion | Context: ESM/CJS interop issue"
 * [today](https://github.com/microsoft/TypeScript/issues/63162#issuecomment-3941291226) **MartinJohns** said "@darshjme-codes Please don't let your AI trash script run on this repository, spamming issues with pointless comments."

### [Issue microsoft/TypeScript#63181](https://github.com/microsoft/TypeScript/issues/63181) (Closed)

**Module resolution: TS2882: Cannot find module or type declarations for side\-effect import of '\./globals\.css'\.**

*TypeScript with moduleResolution "bundler" reports TS2882 when side-effect importing "./globals.css" due to missing module or type declarations.*

 * created by **NMinhNguyen**
 * [today](https://github.com/microsoft/TypeScript/issues/63181#issuecomment-3941328969) **NMinhNguyen** said "Never mind, I think this is expected and caused by https://github.com/microsoft/TypeScript/issues/62421."
 * (today) **NMinhNguyen** closed the issue

### [PR microsoft/TypeScript#63182](https://github.com/microsoft/TypeScript/pull/63182) (Open, `For Backlog Bug`)

**Fixed a crash related to computed enum member keys**

*Fix crash from computed enum member keys by checking non-dynamic names instead of bindable names*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63182#issuecomment-3942796818) **jakebailey** said "Can you explain the fix?"
 * [later](https://github.com/microsoft/TypeScript/pull/63182#issuecomment-3943375100) **Andarist** said "@jakebailey sure, edited the PR summary"

### [PR microsoft/TypeScript#63183](https://github.com/microsoft/TypeScript/pull/63183) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**DOM update**

*Optimize the DOM update process to ensure efficient and accurate rendering of dynamic content changes.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63183#issuecomment-3942021195) **jakebailey** requested the typescript-bot to run dt, test top400, and user test this
 * [today](https://github.com/microsoft/TypeScript/pull/63183#issuecomment-3942021305) **typescript-bot** updated build status table for the commands `run dt`, `test top400`, and `user test this` with start and result links
 * [today](https://github.com/microsoft/TypeScript/pull/63183#issuecomment-3942054688) **typescript-bot** announced that the DT test results were ready and that everything looked the same, providing a link to the log
 * [today](https://github.com/microsoft/TypeScript/pull/63183#issuecomment-3942063967) **typescript-bot** reported test results comparing main and refs/pull/63183/merge, noted a Git clone failure, and indicated everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63183#issuecomment-3942149269) **typescript-bot** reported that compiling the top 400 repos with tsc on main and the pull request merge yielded no issues

### [PR microsoft/TypeScript#63184](https://github.com/microsoft/TypeScript/pull/63184) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.3 to 4\.32\.4 in the github\-actions group**

*Update github/codeql-action from v4.32.3 to v4.32.4 to use the latest CodeQL bundle and improved proxy certificates*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63185](https://github.com/microsoft/TypeScript/issues/63185) (Open, `Bug`, `Domain: Source Maps`, **weswigham**)

**tsgo producing source maps that cause functions to appear uncovered in tests**

*tsgo 7.0.0-dev’s generated source maps unexpectedly include inline sources, causing code coverage tools to misreport covered functions as uncovered.*

 * created by **isaacs**

