# Report for 2026-01-29 (Thursday, January 29th, 2026)

9 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @wjaspers asked RyanCavanaugh to elaborate on fidian's questions in [microsoft/TypeScript#52601](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3821534993)
    * @fisker asked if the two class definitions were equivalent in [microsoft/TypeScript#63065](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818645780)

## Activity Summary

### [Issue microsoft/TypeScript#52601](https://github.com/microsoft/TypeScript/issues/52601) (Closed, `Not a Defect`)

**Promise\.all sometimes infers incorrect types**

*Promise.all sometimes fails to unwrap async function results, causing the returned array items to be typed as Promise<Response> instead of Response.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3806611522) **RyanCavanaugh** denied that the example was a bug and suggested using 'as const' to fix it, providing a code example
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3807160968) **wjaspers** explained that they simplified the reproduction to reduce noise, described encountering multiple async calls with mixed return types, and asked when one would naturally use `Promise.all([...]) as const` in day-to-day work
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3807404862) **fidian** asked why TS5.9.3 lost tuple typing with Promise.all for Promise<string[]> and why workarounds like .then, as const, or extracting to a var restored the correct types
 * [today](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3821340468) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3821534993) **wjaspers** asked RyanCavanaugh to elaborate on fidian's questions and noted that type widening made the order of Promise.all arguments in then misleading

### [PR microsoft/TypeScript#61534](https://github.com/microsoft/TypeScript/pull/61534) (Open, `For Milestone Bug`, **weswigham**)

**fix\(jsx\): correct source location when react\-jsx and whitespace before jsx**

*Use getStart instead of getFullStart to correct JSX source locations and align outputs with Babel*

 * (5 weeks ago) **typescript-bot** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/61534#issuecomment-3819132470) **AviVahl** rebased to latest main, accepted new baselines, and rebased again after additional baseline changes

### [Issue microsoft/TypeScript#61613](https://github.com/microsoft/TypeScript/issues/61613) (Closed, `Suggestion`, `Declined`)

**Allow \.ts extension when importing from a private mapping?**

*Allow using .ts extensions in custom import mappings (e.g. #root) without triggering the TypeScript rewrite-during-emit error.*

 * [39 weeks ago](https://github.com/microsoft/TypeScript/issues/61613#issuecomment-2836222424) **RyanCavanaugh** said "If you're not transpiling, then turn off "rewriteRelativeImportExtensions": true, and you won't see this error"
 * [39 weeks ago](https://github.com/microsoft/TypeScript/issues/61613#issuecomment-2843881469) **typescript-bot** said "This issue has been marked as "Declined" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (39 weeks ago) **typescript-bot** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/61613#issuecomment-3822453143) **piotr-cz** shared a workaround for keeping rewriteRelativeImportExtensions enabled and importing .ts files by adding an imports mapping

### [Issue microsoft/TypeScript#62196](https://github.com/microsoft/TypeScript/issues/62196) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **jakebailey**)

**Deprecate \`\-\-target es5\`, make lowest target \`es2015\`**

*Deprecate --target es5 in TypeScript 6.0, raise the minimum target to ES2015, and update library inclusion and downlevel iteration handling.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3795462617) **EliasVal** challenged the claim that ES5 environments are vanishingly rare by listing devices that only support ES5 and then noted that some statistics might be outdated
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3795468983) **EliasVal** mentioned that 96.23% of internet users support ES6 and that maintaining ES5 support for the remaining 3% is not worth the cost
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3807001264) **guilhermesimoes** criticized the suggestion that PS4 browser usage is rare as ignorant, noted apps on PS4/PS5 have millions of users in Europe and Africa but declined to share exact figures, and deferred the ES5 support cost decision to the TypeScript team
 * **typescript-bot** added label `Fix Available`

### [Issue microsoft/TypeScript#62198](https://github.com/microsoft/TypeScript/issues/62198) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **jakebailey**)

**Change default \`\-\-target\` to latest ECMAScript version**

*Change TypeScript’s default target from ES5 to the latest ECMAScript version to promote modern runtime support.*

 * (1 week ago) **RyanCavanaugh** assigned to **jakebailey**, and unassigned **Copilot**, **RyanCavanaugh**
 * **typescript-bot** added label `Fix Available`

### [Issue microsoft/TypeScript#63062](https://github.com/microsoft/TypeScript/issues/63062) (Closed)

**Request to Participate and Share Academic Survey on Code Review in OSS Security**

*Request permission to share an anonymous academic survey on how developers identify security issues during OSS code reviews.*

 * created by **morshedniaz**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63065](https://github.com/microsoft/TypeScript/issues/63065) (Closed, `Question`)

**Is \`\`class A extends \(B\<T\>\)\<T\> {}\`\` valid code?**

*Asking whether the syntax `class A extends (B<T>)<T> {}` is valid TypeScript code without errors.*

 * [today](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818110721) **fisker** asked if extending (B<T>) and B<T> produced the same behavior
 * [today](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818424016) **mkantor** observed multiple errors in the linked playground and noted that some remained after defining B and T
 * [today](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818446531) **mkantor** clarified that the two cases weren't equivalent and explained that parentheses likely create an instantiation expression
 * [today](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818619126) **fisker** clarified that the playground didn't refuse to parse despite showing multiple errors
 * [today](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818645780) **fisker** asked if the two class definitions were equivalent
 * [today](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3819291024) **RyanCavanaugh** asked for clarification on what was being requested, noting it was already a semantic error

### [PR microsoft/TypeScript#63066](https://github.com/microsoft/TypeScript/pull/63066) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update tests in prep for ES5 deprecation, target default change**

*Add explicit @target and @module annotations to tests to avoid errors when ES5 support is deprecated and the default ECMAScript target changes.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63067](https://github.com/microsoft/TypeScript/pull/63067) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Default \`target\` to "latest standard", deprecate ES5**

*Set the default compilation target to the latest standardized ECMAScript version and deprecate ES5, updating tests accordingly.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821629541) **typescript-bot** thanked the author for the PR, cautioned to preserve TSServer API compatibility, and pinged reviewers for extra review
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821629644) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821630296) **jakebailey** requested the TypeScript bot to test and pack
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821630542) **typescript-bot** reported CI job status updates in a table
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821641816) **typescript-bot** provided an installable tgz link and testing instructions, plus playground and npm module links
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821681248) **typescript-bot** notified jakebailey that the DT test results were ready and provided links to the logs
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821685715) **jakebailey** said "Looks like DT has a load of ES5s. Those have to be fixed first."
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821696885) **typescript-bot** reported user test comparison results between main and the PR merge, noted infrastructure failures and new TS1202 errors across several projects, and asked to review
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821751658) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821751811) **typescript-bot** posted an automated build status update with job start and results links
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821769199) **typescript-bot** reported the requested performance run results to @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821801870) **typescript-bot** reported DT test results including branch-only errors in activex-wia package
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821818337) **typescript-bot** reported results of running the top 400 repos with tsc comparing main and pull request merge and noted an interesting change

### [Issue microsoft/TypeScript#63068](https://github.com/microsoft/TypeScript/issues/63068) (Closed, `Working as Intended`)

**"translate" property is yes/no not boolean**

*The dom.lib.d.ts file incorrectly defines the HTML translate attribute as boolean rather than string 'yes' or 'no'.*

 * created by **kkmuffme**
 * [later](https://github.com/microsoft/TypeScript/issues/63068#issuecomment-3824110965) **IllusionMH** clarified that the link referred to an HTML attribute rather than the JS DOM API, referenced the MDN HTMLElement.translate page, and provided example code

