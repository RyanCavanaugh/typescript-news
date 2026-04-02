# Report for 2026-03-25 (Wednesday, March 25th, 2026)

13 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @compeek suggested adding a `current-year` lib option in [microsoft/TypeScript#62536](https://github.com/microsoft/TypeScript/issues/62536#issuecomment-4128954744)

## Activity Summary

### [Issue microsoft/TypeScript#52222](https://github.com/microsoft/TypeScript/issues/52222) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support \`satisfies\` in type declaration**

*Add support for using the TypeScript `satisfies` operator in type alias declarations.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-3053526286) **bwateratmsft** mentioned intention to use this in the Container Tools extension for VSCode and to assert a Disposable interface’s compatibility with both `@types/vscode` and `vscode-jsonrpc`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-4046222921) **yandodov** demonstrated a hack to satisfy ESLint by using `void 0 as unknown as Satisfy<..., ...>` and suggested a built-in `satisfies` feature
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-4046297699) **yandodov** suggested support for type annotations in type definitions analogous to runtime variable annotations
 * [later](https://github.com/microsoft/TypeScript/issues/52222#issuecomment-4134791086) **5cover** explained that the behavior stems from excess property checks rather than the `satisfies` operator

### [PR microsoft/TypeScript#54096](https://github.com/microsoft/TypeScript/pull/54096) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**Add a failing test case with \`types: null\` condition**

*Add a failing test case for scenarios where `types` is null to address a related TypeScript bug*

 * (yesterday) **andrewbranch** closed the issue
 * (yesterday) **andrewbranch** reopened the issue
 * [yesterday](https://github.com/microsoft/TypeScript/pull/54096#issuecomment-4121979385) **andrewbranch** explained that the change would fail CI due to improved behavior introduced in a previous PR
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#57531](https://github.com/microsoft/TypeScript/issues/57531) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Improve "'await' has no effect on the type of this expression" hints in JavaScript when extending Promise**

*Improve misleading 'await has no effect on the type of this expression' hints when awaiting custom Promise subclasses.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [50 weeks ago](https://github.com/microsoft/TypeScript/issues/57531#issuecomment-2776204829) **Swimburger** asked if the quick fix hint was still present in their VS Code instance
 * [50 weeks ago](https://github.com/microsoft/TypeScript/issues/57531#issuecomment-2776728719) **dnicolson** said "Yes, it is still an issue with VS Code 1.98.2. It looks like the built-in extension is using TypeScript 5.9.0-dev.20250330."
 * (today) **dnicolson** closed the issue

### [Issue microsoft/TypeScript#62536](https://github.com/microsoft/TypeScript/issues/62536) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support lib: "baseline\-widely\-available"**

*Introduce a baseline-widely-available lib option to TypeScript that limits code to JavaScript features supported by major browsers for 30+ months.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/62536#issuecomment-3368174307) **3ru** supported migrating to TypeScript, opened a draft PR with a PoC baseline library, and invited the Baseline team to discuss feasibility, mapping granularity, and the update process
 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/62536#issuecomment-3475944070) **3ru** asked whether using an external generator to emit opt-in baseline lib files would be reasonable for TS or if a more native composition in src/lib would be preferable
 * [today](https://github.com/microsoft/TypeScript/issues/62536#issuecomment-4128954744) **compeek** suggested adding an explicit `current-year` lib option to avoid hardcoding the year

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4112022731) **RyanCavanaugh** said "https://devblogs.microsoft.com/typescript/announcing-typescript-6-0/"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4121568642) **buley** suggested that PR #63290 meets the first criterion for post-6.0 patches and asked the team for confirmation
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4121592927) **jakebailey** rejected the PR as not meeting the bar for TS 6.0 due to low usage, rare failures, and its broken state
 * [later](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4133933446) **HolgerJeromin** expressed happiness about testing with Visual Studio, requested a NuGet release referencing issue #62236, provided a package link, and noted it was done a day ago

### [Issue microsoft/TypeScript#63259](https://github.com/microsoft/TypeScript/issues/63259) (Closed, `Duplicate`)

**Type narrowing incorrect when providing some function generics when default generics present**

*Functions with default generic parameters don’t correctly narrow union-based argument types when only some generics are explicitly provided.*

 * created by **ChromeQ**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63259#issuecomment-4079131983) **MartinJohns** stated that generic type inference is all or none and marked the issue as duplicate of #26242
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63259#issuecomment-4130943572) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63281](https://github.com/microsoft/TypeScript/issues/63281) (Open, `Suggestion`, `Awaiting More Feedback`)

**RegExpIndicesArray \- Named group indices can be undefined**

*TypeScript’s RegExpIndicesArray incorrectly assumes named regex group index arrays are always defined, missing errors for undefined groups.*

 * created by **TomStrepsil**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63281#issuecomment-4113099347) **RyanCavanaugh** said "I think this falls under #32098"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63281#issuecomment-4113654374) **TomStrepsil** clarified that strong key typing for named capture groups is a larger change and unrelated to the undefined value issue
 * (later) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [PR microsoft/TypeScript#63296](https://github.com/microsoft/TypeScript/pull/63296) (Closed)

**Update deps**

*Update project dependencies to address Dependabot alerts and satisfy npm audit.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63297](https://github.com/microsoft/TypeScript/issues/63297) (Closed, `Won't Fix`)

**Declared\-but\-never\-read warning can't see through \`bind\(this\)\` construct**

*VS Code incorrectly marks private class methods as unused when invoked within a callback bound using bind(this).*

 * (today) **fweth** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63297#issuecomment-4128157844) **PrathamPeriwal** said "Hi @fweth @benibenj @TylerLeonhardt I think I might know the fix for this issue and would like to work on it. Could you please assign it to me?"
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * (today) **RyanCavanaugh** added label `Won't Fix`, and unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63297#issuecomment-4128285003) **RyanCavanaugh** said "This would be very invasive to fix and there's no reason not to use an arrow function instead."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63297#issuecomment-4128289485) **MartinJohns** explained that TypeScript can't infer 'this' inside a function and suggested explicitly typing it with a code example

### [Issue microsoft/TypeScript#63298](https://github.com/microsoft/TypeScript/issues/63298) (Closed, `7.0 LS Migration`)

**VS Code / TypeScript Issue: Auto\-import ignores minimal extension setting with imports aliases**

*VS Code TypeScript auto-import in bundler mode ignores minimal importModuleSpecifierEnding for subpath aliases and always appends extensions.*

 * created by **AndresSomadossi**
 * [today](https://github.com/microsoft/TypeScript/issues/63298#issuecomment-4128656674) **vs-code-engineering[bot]** thanked the user for creating the issue and suggested upgrading to VS Code 1.113.0 to check if the issue persists
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/63298#issuecomment-4129983154) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see https://github.com/microsoft/TypeScript/issues/62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63299](https://github.com/microsoft/TypeScript/issues/63299) (Closed, `Working as Intended`)

**AsyncDisposable should allow non\-Promise returning implementations**

*Permit AsyncDisposable implementations to return void or PromiseLike<void> from Symbol.asyncDispose.*

 * created by **mfulton26**
 * [today](https://github.com/microsoft/TypeScript/issues/63299#issuecomment-4129213929) **MartinJohns** explained that the behavior was intentional and referenced issue #54505 clarifying return type requirements for [Symbol.asyncDispose] in TypeScript
 * [today](https://github.com/microsoft/TypeScript/issues/63299#issuecomment-4129372938) **mfulton26** expressed surprise that the behavior was intentional and inquired about disabling the Promise-like return type check
 * [today](https://github.com/microsoft/TypeScript/issues/63299#issuecomment-4129413929) **MartinJohns** corrected that ts-expect-error works fine
 * [today](https://github.com/microsoft/TypeScript/issues/63299#issuecomment-4129520096) **RyanCavanaugh** said "What are real disposable objects out there that only sometimes return a Promise?"
 * [today](https://github.com/microsoft/TypeScript/issues/63299#issuecomment-4129628037) **RyanCavanaugh** showed a motivating example of a class implementing AsyncDisposable that forgot to call or await its disposer
 * **RyanCavanaugh** added label `Working as Intended`

### [PR microsoft/TypeScript#63300](https://github.com/microsoft/TypeScript/pull/63300) (Closed)

**fix\(i18n\): correct Chinese translation for TS2561**

*Corrected the Simplified Chinese translation of TypeScript error TS2561 to fix reversed logic and improve clarity.*

 * created by **hnshah**
 * [today](https://github.com/microsoft/TypeScript/pull/63300#issuecomment-4129906851) **hnshah** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63300#issuecomment-4129937998) **RyanCavanaugh** said "Localizations are sourced from our loc team, so these will get overwritten on their next merge. Unfortunately we don't have a way to directly upstream user-provided translation improvements."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63301](https://github.com/microsoft/TypeScript/pull/63301) (Closed)

**fix: pin 5 unpinned action\(s\)**

*Pins five unpinned third-party GitHub Actions to specific commit SHAs to remediate high-severity CI/CD security vulnerabilities.*

 * created by **dagecko**
 * [later](https://github.com/microsoft/TypeScript/pull/63301#issuecomment-4135951091) **jakebailey** said "Note that these are all actions owned by our team and are unpinned on purpose. I do not think we need this."
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63302](https://github.com/microsoft/TypeScript/pull/63302) (Closed)

**fix\(30408\): improve error message for labels used before definition**

*Include the label name in the 'Jump target cannot cross function boundary' error message when applicable.*

 * created by **wdskuki**
 * [later](https://github.com/microsoft/TypeScript/pull/63302#issuecomment-4135964280) **jakebailey** stated that PRs of this kind were not being accepted post-6.0, closed non-qualifying PRs, and provided criteria and next-step guidance
 * (later) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/63302#issuecomment-4135968015) **jakebailey** said "(Also, this seems to be an LLM generated PR, and clearly did not have any tests run.)"

