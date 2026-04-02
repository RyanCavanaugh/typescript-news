# Report for 2026-02-04 (Wednesday, February 4th, 2026)

14 different users commented on 36 different issues.

## Recommended Actions

 * Response Recommended
    * @baymer provided the requested issue link in [microsoft/TypeScript#63099](https://github.com/microsoft/TypeScript/pull/63099#issuecomment-3850272459)
    * @Jhounx offered to test the security of the CI/CD pipelines and provided their HackerOne profile in [microsoft/TypeScript#63101](https://github.com/microsoft/TypeScript/pull/63101#issuecomment-3850398698)
    * @hgl reported that the suggested workaround isn't working due to a Typescript error in [microsoft/TypeScript#63105](https://github.com/microsoft/TypeScript/issues/63105#issuecomment-3851392739)

## Activity Summary

### [Issue microsoft/TypeScript#1108](https://github.com/microsoft/TypeScript/issues/1108) (Open, `Suggestion`, `Needs Proposal`)

**No way to type an object with null prototype**

*Provide a TypeScript type representing objects with null prototypes that disallows inherited Object members.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/1108#issuecomment-1606591573) **janickvwcotiss** said "Any updates on this? I am constantly running this problem. It's been 9 years 😢 "
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/1108#issuecomment-1783326524) **SimplyLinn** said "I made this, it's not pretty, but if you're ok with it not being pretty and a bit of a bodge... https://www.npmjs.com/package/null-proto-ts"
 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/1108#issuecomment-1849052833) **dmchurch** proposed modeling null-prototype objects as the root of the type tree and outlined assignment requirements under TypeScript’s duck-typing
 * [today](https://github.com/microsoft/TypeScript/issues/1108#issuecomment-3850151042) **valler** provided a summary of useful findings about Dict and Struct definitions, explained their runtime prototype assumptions and TypeScript limitations, replaced class snippets with comments on bad practice, retained a legacy syntax example, and shared a Playground link

### [Issue microsoft/TypeScript#61533](https://github.com/microsoft/TypeScript/issues/61533) (Closed, `Bug`, `Help Wanted`, `Domain: JSX/TSX`, `Fix Available`, **weswigham**)

**Wrong location generated for JSX with whitespace around it when react\-jsxdev**

*TypeScript's react-jsxdev transform outputs incorrect line and column numbers for JSX elements when surrounded by whitespace.*

 * (43 weeks ago) **RyanCavanaugh** added label `Domain: JSX/TSX`, and unassigned **andrewbranch**
 * **typescript-bot** added label `Fix Available`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#61534](https://github.com/microsoft/TypeScript/pull/61534) (Closed, `For Milestone Bug`, **weswigham**)

**fix\(jsx\): correct source location when react\-jsx and whitespace before jsx**

*Use getStart instead of getFullStart to correct JSX source locations and align outputs with Babel*

 * (6 weeks ago) **typescript-bot** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/61534#issuecomment-3819132470) **AviVahl** rebased to latest main, accepted new baselines, and rebased again after additional baseline changes
 * [today](https://github.com/microsoft/TypeScript/pull/61534#issuecomment-3850422595) **jakebailey** said "LGTM but I would switch to skipTrivia instead."
 * [today](https://github.com/microsoft/TypeScript/pull/61534#issuecomment-3850517913) **AviVahl** thanked the maintainers and asked if PRs would be ported to typescript-go and tracked
 * [today](https://github.com/microsoft/TypeScript/pull/61534#issuecomment-3850522223) **jakebailey** said "Yes, there's a board, and Copilot is good at porting these. We have yet to start targeting 6.0 in the Go code, though, but that will happen ~today"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62195](https://github.com/microsoft/TypeScript/issues/62195) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **RyanCavanaugh**, **Copilot**)

**Change default of \`types\` to \`\[\]\` in \`tsconfig\.json\`**

*Default tsconfig.json types now empty in TS 6.0, requiring explicit 'types' entries or imports and supporting '*' for legacy inclusion.*

 * **RyanCavanaugh** assigned to **Copilot**
 * (2 weeks ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62213](https://github.com/microsoft/TypeScript/issues/62213) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Deprecate \`\-\-useStrict\` & assume \`"use strict"\` everywhere by default**

*TypeScript 6.0 will assume strict mode everywhere by default, deprecating the alwaysStrict flag to simplify configuration and improve performance.*

 * (2 weeks ago) **typescript-bot** added labels `Fix Available`, `Fix Available`, `Fix Available`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3423494989) **typescript-bot** reported that everything looked good when comparing TypeScript compiler results on the top 400 repos between main and the pull request merge
 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3629347917) **jakebailey** said "I know there are existing polyfills for Temporal out there in TS; are these types compatible / based off of those? Or fresh?"
 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3629743678) **Renegade334** noted that definitions were de novo with no licensing issues and observed that temporal-polyfill and @js-temporal/polyfill were incompatible with lib.d.ts patterns, offering to run interoperability tests
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3850515921) **jakebailey** mentioned reviewing the PR and noted that MDN hasn't updated to reflect the removal of custom calendar support per the latest spec changes

### [PR microsoft/TypeScript#62971](https://github.com/microsoft/TypeScript/pull/62971) (Closed, `For Backlog Bug`)

**add \`collation\` to \`Intl\.CollatorOptions\`**

*Add the collation property to Intl.CollatorOptions to enable specifying string comparison rules for different locales*

 * (3 weeks ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62971#issuecomment-3849048791) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/62971#issuecomment-3849049482) **typescript-bot** reported CI job start and linked build results
 * [today](https://github.com/microsoft/TypeScript/pull/62971#issuecomment-3849162440) **typescript-bot** informed that the DT test results were ready and unchanged and linked the logs

### [PR microsoft/TypeScript#62982](https://github.com/microsoft/TypeScript/pull/62982) (Closed, `For Uncommitted Bug`)

**fix\(lib\): allow 'default' in Intl\.CollatorOptions\.collation**

*Add 'default' as a valid collation option in Intl.CollatorOptions to match runtime behavior.*

 * created by **adityavyas01**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/62982#issuecomment-3743884854) **adityavyas01** agreed with microsoft-github-policy-service
 * [today](https://github.com/microsoft/TypeScript/pull/62982#issuecomment-3849056968) **jakebailey** said "Your fixes line is just a link to another PR with the same contents"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63046](https://github.com/microsoft/TypeScript/pull/63046) (Closed, `For Backlog Bug`)

**Introduce ES2025 target & Add missing ScriptTargetFeatures**

*Introduce ES2025 compilation target and add missing type definitions for RegExp.escape and Intl.DurationFormat in TypeScript.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3813947467) **jakebailey** noted that mixing esnext and ES2025 changes in a single PR made it hard to distinguish new work from moves and suggested reviewing individual ESNext PRs and creating a dedicated ES2025 PR
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3814011569) **petamoriken** explained that only two files were added and offered to split the PR if preferred
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3830973432) **petamoriken** said "@jakebailey For now, I can remove the additions of es2025.intl.d.ts and es2025.regexp.d.ts from this PR, but should I do so? Please let me know your thoughts."
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849254662) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849255009) **typescript-bot** posted CI job status updates for various commands
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849329828) **jakebailey** noted confusion about test baseline changes and suggested merging this PR first then fixing other lib updates based on ES2025
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849344384) **typescript-bot** reported test results comparing main and PR merge, noted infrastructure failures and otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849354757) **typescript-bot** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849509461) **typescript-bot** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849594738) **typescript-bot** provided results of running the top 400 repos with tsc comparing main and PR merge and noted everything looked good

### [PR microsoft/TypeScript#63054](https://github.com/microsoft/TypeScript/pull/63054) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Set default \`types\` array to \`\[\]\`; support \`"\*"\` wildcard**

*Set the default types array to an empty list and implement '*' wildcard support.*

 * **jakebailey** added label `Breaking Change`
 * (5 days ago) **typescript-bot** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63071](https://github.com/microsoft/TypeScript/pull/63071) (Closed, `Breaking Change`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Deprecate downlevelIteration**

*Deprecate the downlevelIteration compiler flag in TypeScript 7.0 since it’s redundant for ES2015+ targets.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3843176860) **typescript-bot** started test top800 build job and provided status and results links
 * **jakebailey** added label `Breaking Change`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3843827126) **typescript-bot** reported the results of running the top 800 repositories with tsc comparing `main` and the pull request merge and noted an interesting change
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63074](https://github.com/microsoft/TypeScript/issues/63074) (Closed, `Not a Defect`)

**\`x is any\` type guard widens \`unknown\` type even after the relevant scope has been exited**

*Custom type guard isAny incorrectly widens unknown types to any beyond the guard’s scope*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63074#issuecomment-3827797037) **MartinJohns** said "Why would you ever write a x is any type guard?"
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63074#issuecomment-3836787790) **RyanCavanaugh** said "This is a sort of unavoidable consequence of how control flow works, and yeah there doesn't seem to be any reason to do this in the first place"
 * [today](https://github.com/microsoft/TypeScript/issues/63074#issuecomment-3850600190) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63084](https://github.com/microsoft/TypeScript/pull/63084) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add \-\-stableTypeOrdering for TS7 ordering compat**

*Add a hidden --stableTypeOrdering flag that enables TS7’s deterministic type, symbol, and node ordering algorithm for tsgo-port compatibility.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3843702728) **jakebailey** checked that the flag was disabled and requested a faster perf test
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3843703025) **typescript-bot** provided initial CI build status update
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3843939535) **typescript-bot** posted the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3849906953) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3849907364) **typescript-bot** posted a build status update with links for the pack this command
 * [today](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3849927246) **typescript-bot** provided an installable tgz link and instructions for testing by referencing it in package.json and running npm install

### [PR microsoft/TypeScript#63086](https://github.com/microsoft/TypeScript/pull/63086) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix some tests that should have stayed ES5**

*Several tests were inadvertently converted to newer JavaScript syntax and need to be reverted to ES5.*

 * (yesterday) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63088](https://github.com/microsoft/TypeScript/issues/63088) (Open)

**Function property in union does not get parameter type inferred from result of type narrowing**

*TypeScript does not infer a function property’s parameter type from narrowed union discriminants, defaulting to any.*

 * created by **dyantako**
 * [today](https://github.com/microsoft/TypeScript/issues/63088#issuecomment-3848949611) **jcalz** described the issue as possibly a duplicate of #53033 and #47599 and explained that Options isn’t a discriminated union so TypeScript’s narrowing doesn’t apply early enough
 * [today](https://github.com/microsoft/TypeScript/issues/63088#issuecomment-3849859741) **RyanCavanaugh** provided an automated list of similar issues

### [PR microsoft/TypeScript#63089](https://github.com/microsoft/TypeScript/pull/63089) (Closed, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Deprecate \`alwaysStrict: false\`**

*Deprecate alwaysStrict: false in TypeScript to enforce strict mode by default.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63089#issuecomment-3845658482) **jakebailey** said "@typescript-bot test top800"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63089#issuecomment-3845658727) **typescript-bot** announced that the test top800 job started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/63089#issuecomment-3846213662) **typescript-bot** reported build comparison results between main and the pull request for the top 800 repositories and flagged an interesting change
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63090](https://github.com/microsoft/TypeScript/issues/63090) (Open)

**Crash: RangeError: Maximum call stack size exceeded during type serialization of recursive distributive mapped types**

*Recursive distributive mapped types trigger a compiler stack overflow error in TypeScript 5.7.3 and later.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/63090#issuecomment-3849859776) **RyanCavanaugh** provided an automatically generated list of similar issues

### [Issue microsoft/TypeScript#63091](https://github.com/microsoft/TypeScript/issues/63091) (Closed, `Fix Available`)

**Crash: RangeError: Maximum call stack size exceeded when destructuring undefined/unknown as identifiers in parameter list**

*TypeScript crashes with a maximum call stack error when destructuring undefined and unknown in function parameters under strict mode.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/63091#issuecomment-3849664932) **Andarist** said "I believe this is a strong duplicate of https://github.com/microsoft/TypeScript/issues/63044"
 * **typescript-bot** added label `Fix Available`
 * (today) **na7ure-a** closed the issue

### [Issue microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092) (Open)

**Crash: RangeError: Maximum call stack size exceeded in isReachableFlowNodeWorker with complex for loop headers**

*TypeScript's compiler crashes with a maximum call stack size exceeded error when analyzing reachability in complex for loop headers.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-3849747076) **Andarist** provided a repro case that might point at the root cause

### [Issue microsoft/TypeScript#63093](https://github.com/microsoft/TypeScript/issues/63093) (Closed, `Fix Available`)

**Crash: RangeError: Maximum call stack size exceeded in checkExpression when resolving property access on parenthesized type assertions with generic\-like syntax**

*TypeScript compiler overflows the call stack when resolving property access on a parenthesized generic-like type assertion in strict mode.*

 * created by **na7ure-a**
 * **typescript-bot** added label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/63093#issuecomment-3849698771) **Andarist** said "This is also very close to https://github.com/microsoft/TypeScript/issues/62993"
 * (today) **na7ure-a** closed the issue

### [Issue microsoft/TypeScript#63094](https://github.com/microsoft/TypeScript/issues/63094) (Open)

**Crash: Debug Failure\. False expression in getArgumentArityError when resolving overloaded decorators with \-\-experimentalDecorators**

*TypeScript crashes with a 'Debug Failure. False expression' error in getArgumentArityError when resolving overloaded decorators under --experimentalDecorators.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/63094#issuecomment-3849859852) **RyanCavanaugh** provided an automatically generated list of similar issues to assist the user
 * [today](https://github.com/microsoft/TypeScript/issues/63094#issuecomment-3850125625) **Andarist** provided a shorter reproduction snippet

### [PR microsoft/TypeScript#63095](https://github.com/microsoft/TypeScript/pull/63095) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Update descriptions for strict\-related flags**

*Revise strict-related flag descriptions to indicate they are now enabled by default for most users.*

 * created by **DanielRosenwasser**
 * (today) **typescript-bot** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63096](https://github.com/microsoft/TypeScript/issues/63096) (Closed)

**5\.9 regression: generic type predicate inferred as never in Extract**

*Upgrading to TypeScript 5.9 causes generic type predicates in Extract to be inferred as never, breaking predicate refinements.*

 * created by **lucas-barake**
 * [today](https://github.com/microsoft/TypeScript/issues/63096#issuecomment-3850016943) **lucas-barake** said "Closing this - the behavior change appears to be intentional from PR #61668. Opened an issue on the Effect repo instead: https://github.com/Effect-TS/effect/issues/6027"
 * (today) **lucas-barake** closed the issue

### [PR microsoft/TypeScript#63097](https://github.com/microsoft/TypeScript/pull/63097) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Disable macOS in PR CI**

*Disable macOS CI builds on pull requests and restrict macOS testing to only the oldest and newest versions.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63098](https://github.com/microsoft/TypeScript/pull/63098) (Open, `For Uncommitted Bug`)

**Fix crash related to legacy method decorators and signatures with rest**

*Prevents the TypeScript compiler from crashing when using legacy method decorators on methods with rest parameters in their signatures.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63099](https://github.com/microsoft/TypeScript/pull/63099) (Open, `For Uncommitted Bug`)

**fix\(case\): apply using pnpm with store outside**

*Correct TypeScript’s file system case sensitivity detection in pnpm when using an external virtual store on macOS.*

 * created by **baymer**
 * [today](https://github.com/microsoft/TypeScript/pull/63099#issuecomment-3850232407) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63099#issuecomment-3850272459) **baymer** provided a link to the referenced issue for the PR
 * [today](https://github.com/microsoft/TypeScript/pull/63099#issuecomment-3850290586) **jakebailey** said "I don't think this is the right kind of fix; it just moves the case check to an unspecified "current directory" which we largely do not have any control over and should very much always ignore"

### [Issue microsoft/TypeScript#63100](https://github.com/microsoft/TypeScript/issues/63100) (Open)

**TS wrong calculate case sensitive repo as case insensitive filesystem**

*TypeScript incorrectly treats case-sensitive overlayfs repositories on macOS as case-insensitive, leading to ESLint file inclusion errors for capitalized filenames.*

 * created by **baymer**

### [PR microsoft/TypeScript#63101](https://github.com/microsoft/TypeScript/pull/63101) (Closed, `For Uncommitted Bug`)

**0xdeadbeeftest**

*A pull request titled "0xdeadbeeftest" was submitted with only the default template and no associated changes or issue reference.*

 * created by **Jhounx**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63101#issuecomment-3850340513) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63101#issuecomment-3850366262) **RyanCavanaugh** warned @Jhounx to self-identify as a security researcher or risk being banned and said they would notify the GitHub security team
 * [today](https://github.com/microsoft/TypeScript/pull/63101#issuecomment-3850398698) **Jhounx** introduced themselves as a security researcher and offered to test the repository's CI/CD pipelines, providing their HackerOne profile

### [PR microsoft/TypeScript#63102](https://github.com/microsoft/TypeScript/pull/63102) (Closed, `For Uncommitted Bug`)

**Feat: just a security test please dont fire me**

*A test submission aimed at validating the security of the project's TypeScript CI pipelines.*

 * created by **Jhounx**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63102#issuecomment-3850461151) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **Jhounx** closed the issue

### [PR microsoft/TypeScript#63103](https://github.com/microsoft/TypeScript/pull/63103) (Closed, `For Uncommitted Bug`)

**just another test please dont fire me**

*User performs a security test and provides a HackerOne profile link.*

 * created by **Jhounx**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63103#issuecomment-3850476365) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **Jhounx** closed the issue

### [PR microsoft/TypeScript#63104](https://github.com/microsoft/TypeScript/pull/63104) (Closed, `For Uncommitted Bug`)

**x**

*Checklist and guidelines for submitting TypeScript pull requests, including issue linking, testing, and avoiding typo-only changes.*

 * created by **LuskaBol**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63104#issuecomment-3850482262) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **LuskaBol** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63104#issuecomment-3850490718) **RyanCavanaugh** said "@LuskaBol @Jhounx can I suggest that you try this stuff on your own repo first? This is not the place for dozens of test PRs"

### [Issue microsoft/TypeScript#63105](https://github.com/microsoft/TypeScript/issues/63105) (Closed)

**Exposing local types in an ambient module's declare module fails**

*Re-exporting a local interface in a declare module leads to imported properties being typed as any instead of string.*

 * created by **hgl**
 * [today](https://github.com/microsoft/TypeScript/issues/63105#issuecomment-3851373515) **SyedAdeel00** explained that ambient .d.ts files without top-level imports or exports are treated as global ambient modules causing imported types to become any and that adding export {} converts it into a proper module preserving type information; noted the same pattern in DefinitelyTyped
 * [today](https://github.com/microsoft/TypeScript/issues/63105#issuecomment-3851392739) **hgl** explained that the export {} workaround failed due to a Typescript 'foo was also declared here' error

