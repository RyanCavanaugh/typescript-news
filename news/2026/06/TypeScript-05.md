# Report for 2026-06-05 (Friday, June 5th, 2026)

10 different users commented on 56 different issues.

## Recommended Actions

 * Response Recommended
    * @xsourabhsharma asked whether the approach should be adjusted for consistency across helpers or in a broader follow-up in [microsoft/TypeScript#63522](https://github.com/microsoft/TypeScript/issues/63522#issuecomment-4637435413)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript#63539](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4637526646)
    * @loynoir reported a server crash due to missing linter checks and requested feature enhancements for resource management naming in [microsoft/TypeScript#63540](https://github.com/microsoft/TypeScript/issues/63540#issuecomment-4638114882)

## Activity Summary

### [Issue microsoft/TypeScript#16148](https://github.com/microsoft/TypeScript/issues/16148) (Open, `Suggestion`, `Awaiting More Feedback`)

**Affine types / ownership system**

*Proposal to introduce Rust-inspired ownership types in TypeScript to enforce move semantics and prevent mutations.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/16148#issuecomment-2614658818) **Rudxain** noticed a problem with using `never` as a `moved` type and demonstrated that a function f(_: never) can be called with a `never` value without error, raising concerns about unsafe never-to-never assignments
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/16148#issuecomment-2614666326) **Rudxain** highlighted the type-state pattern as a key reason for move semantics, cited a personal refactor example, and shared links to a TC39 proposal, an article on potential flaws, and inspiration from Mojo
 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/16148#issuecomment-3206971823) **sjcjoosten** proposed using affine types for delete operations in TypeScript, illustrated with examples, and asked if existing special-casing could be leveraged for other cases
 * [later](https://github.com/microsoft/TypeScript/issues/16148#issuecomment-4638291995) **loynoir** said "Stricter ownership type definitely good for audit AI generated code."

### [Issue microsoft/TypeScript#63522](https://github.com/microsoft/TypeScript/issues/63522) (Open, `Bug`, `Domain: JS Emit`)

**Declarations that shadow global \`Symbol\`  break emit for \`using\` declarations**

*Declaring a local Symbol class that shadows the global Symbol breaks using declaration emissions and leads to runtime Symbol.dispose errors.*

 * (3 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: JS Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63522#issuecomment-4637243666) **xsourabhsharma** offered to work on a fix by reproducing the issue locally, adjusting the emit to target the correct global Symbol in the presence of a shadowing declaration, and adding a regression test before opening a PR
 * [today](https://github.com/microsoft/TypeScript/issues/63522#issuecomment-4637377997) **jakebailey** said "No other helper checks this, no?"
 * [today](https://github.com/microsoft/TypeScript/issues/63522#issuecomment-4637435413) **xsourabhsharma** checked emitHelpers.ts and found other helpers still reference lexical Symbol, scoped the PR to __addDisposableResource, and offered to adjust the approach for consistency or a broader follow-up

### [PR microsoft/TypeScript#63525](https://github.com/microsoft/TypeScript/pull/63525) (Closed, `For Uncommitted Bug`)

**Fix JSDoc grammar typo: 'returns a undefined' → 'returns undefined'**

*Grammar typo corrected in JSDoc for SymbolConstructor.keyFor by changing '@returns a undefined' to '@returns undefined'*

 * (3 days ago) **RyanCavanaugh** closed the issue
 * (3 days ago) **RyanCavanaugh** reopened the issue
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4625580688) **RyanCavanaugh** said "@driphtyio need CLA sign before we can merge this"
 * [today](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4636178514) **driphtyio** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63533](https://github.com/microsoft/TypeScript/issues/63533) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-06\-04**

*Ban unparenthesized type assertions and satisfies with binary operators under erasableSyntaxOnly to preserve source maps and prevent ambiguous precedence.*

 * created by **RyanCavanaugh**
 * **RyanCavanaugh** added label `Design Notes`
 * [today](https://github.com/microsoft/TypeScript/issues/63533#issuecomment-4633821401) **jcalz** suggested that issue #34692 might mitigate a possible downside with template literals and Unicode
 * [today](https://github.com/microsoft/TypeScript/issues/63533#issuecomment-4634309789) **RyanCavanaugh** said "This didn't make it into the notes, but I'm actually very glad we didn't add length as a property. It's not really clear what you would even do with it under the proposed 7.0 behavior."

### [PR microsoft/TypeScript#63535](https://github.com/microsoft/TypeScript/pull/63535) (Closed, `For Backlog Bug`)

**Allow lone ampersands in Unicode sets regex classes**

*Enable lone ampersands in Unicode set regex character classes while retaining && as the intersection operator.*

 * created by **Ijtihed**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63535#issuecomment-4629413532) **Ijtihed** agreed to the Contributor License Agreement using the microsoft-github-policy-service command
 * [today](https://github.com/microsoft/TypeScript/pull/63535#issuecomment-4633539867) **RyanCavanaugh** said "This should go in the typescript-go repo as this doesn't meet the 6.0 patch bar. See #62963"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63536](https://github.com/microsoft/TypeScript/pull/63536) (Closed, `For Uncommitted Bug`, `Voight-Kampff Anomaly`)

**fix catastrophic backtracking in jquery typesMap rule**

*Replace the nested digit quantifier in the jQuery typesMap regex with a linear pattern to prevent catastrophic backtracking.*

 * [today](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4631652211) **dxbjavid** acknowledged that the Go server uses RE2, agreed there was no backtracking issue, and consented to leave the JS language service as-is
 * [today](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4633060366) **jakebailey** said "It's not that, but that it doesn't uses regexes for this at all"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [today](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4633487445) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4633506371) **RyanCavanaugh** said "This is a bot posing as a human. Reported as abuse."
 * [today](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4633663575) **dxbjavid** confirmed manual code review and local reproduction, acknowledged decision not to accept the change, and thanked maintainers
 * [today](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4633700579) **dxbjavid** acknowledged the clarification and expressed thanks
 * [today](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4633706595) **RyanCavanaugh** asked for an explanation and detailed timestamp analysis showing rapid multi-language PR submissions

### [PR microsoft/TypeScript#63537](https://github.com/microsoft/TypeScript/pull/63537) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Pull off full code points in template literal inference**

*Implement full-code-point awareness in TypeScript's template literal inference to ensure correct handling of Unicode characters*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63537#issuecomment-4634118880) **jakebailey** requested multiple CI test runs from the typescript-bot
 * [today](https://github.com/microsoft/TypeScript/pull/63537#issuecomment-4634119589) **typescript-bot** posted automated build status updates
 * [today](https://github.com/microsoft/TypeScript/pull/63537#issuecomment-4634311008) **typescript-bot** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63537#issuecomment-4634365704) **typescript-bot** reported that running user tests comparison against main had two infrastructure failures but otherwise passed
 * [today](https://github.com/microsoft/TypeScript/pull/63537#issuecomment-4634549910) **typescript-bot** provided the requested performance run results with a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/63537#issuecomment-4635011329) **typescript-bot** reported that everything looked good when running the top 800 repos with tsc comparing main and the PR merge
 * [today](https://github.com/microsoft/TypeScript/pull/63537#issuecomment-4635776575) **jakebailey** tested the new bot infrastructure
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63538](https://github.com/microsoft/TypeScript/pull/63538) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Switch from bot PAT to GitHub App token via Azure Key Vault**

*Configure authentication to use a GitHub App token stored in Azure Key Vault instead of a bot PAT.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63539](https://github.com/microsoft/TypeScript/pull/63539) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**ignore me, testing bot**

*A placeholder issue created to test the bot’s functionality and can be ignored.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4635793925) **jakebailey** said "@typescript-bot user test this"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4635942636) **jakebailey** said "@typescript-bot user test this"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4635943354) **typescript-automation[bot]** started automated build jobs and updated statuses with results links
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4636129942) **typescript-bot** reported user test results comparing main and the pull request merge, noted 1 Git clone failure and 1 package install failure, and confirmed everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4636322629) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4636322857) **typescript-automation[bot]** reported that performance test jobs had started and the build was in progress
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4636408694) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4636409070) **typescript-automation[bot]** started jobs and posted a build status table for the `run dt` command
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4636629717) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4636630078) **typescript-automation[bot]** posted a build status update indicating that jobs had started and the comment would be updated as builds progressed
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4637387224) **jakebailey** requested the TypeScript bot to run dt and perf test faster
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4637387520) **typescript-automation[bot]** reported starting jobs and provided CI status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4637449383) **typescript-automation[bot]** reported that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4637526646) **typescript-automation[bot]** provided the requested performance run results

### [Issue microsoft/TypeScript#63540](https://github.com/microsoft/TypeScript/issues/63540) (Open, `Suggestion`, `Needs Proposal`)

**Better ownership lint to eliminate ownership chaos for generated code**

*Add a TypeScript ownership lint enforcing explicit resource management to avoid disposal-related crashes in generated code.*

 * created by **loynoir**
 * [later](https://github.com/microsoft/TypeScript/issues/63540#issuecomment-4638055013) **MartinJohns** said "Sounds like a duplicate of #16148. And no idea what the reference to AI is there for."
 * [later](https://github.com/microsoft/TypeScript/issues/63540#issuecomment-4638114882) **loynoir** described that using file and file.readable together led to server crashes, noted the absence of linter errors, recommended using a simple open-and-return pattern, and requested feature enhancements for clearer resource management naming conventions
 * [later](https://github.com/microsoft/TypeScript/issues/63540#issuecomment-4638502645) **MartinJohns** said "This has absolutely nothing to do with AI. Same code can be written by humans. Better Code can be written by AI."
 * [later](https://github.com/microsoft/TypeScript/issues/63540#issuecomment-4638663487) **loynoir** noted that AI could write better code but might introduce double free issues and suggested adopting a stricter type system like Rust's

### [PR microsoft/TypeScript#63541](https://github.com/microsoft/TypeScript/pull/63541) (Closed, `For Backlog Bug`)

**Fix using declarations when Symbol is shadowed**

*Fix using and await using emit to reference the global Symbol constructor via globalThis when local Symbols shadow it*

 * created by **xsourabhsharma**
 * (today) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63541#issuecomment-4637418778) **xsourabhsharma** said "@microsoft-github-policy-service agree"

