# Report for 2025-12-04 (Thursday, December 4th, 2025)

16 different users commented on 33 different issues.

## Recommended Actions

 * Response Recommended
    * @jedwards1211 asked whether transitive module exports could be prevented from being added to the auto import index and suggested limiting scanning to explicit dependencies in [microsoft/TypeScript#60704](https://github.com/microsoft/TypeScript/issues/60704#issuecomment-3613577715)
    * @jedwards1211 asked for logging where and why the process bailed out in [microsoft/TypeScript#62829](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3613631406)
    * @jedwards1211 asked whether auto imports would dynamically look things up and have an OOM bail-out to prevent memory issues in [microsoft/TypeScript#62829](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3614138523)
    * @hjonasson asked where tool-specific code should live in [microsoft/TypeScript#62834](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3615636887)

## Activity Summary

### [Issue microsoft/TypeScript#37619](https://github.com/microsoft/TypeScript/issues/37619) (Closed, `Bug`, `Domain: JS Emit`)

**"export class" does not compile with outfile=foo \(module=none, es6\)**

*Using outFile with module none on an exported class produces no output file and no error message*

 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/37619#issuecomment-669870706) **HolgerJeromin** reported that code with an exported interface did not compile without error messages but worked when removing the export
 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/37619#issuecomment-799441995) **HolgerJeromin** provided an easier reproduction example with a ServiceWorkerGlobalScope declaration and compilerOptions
 * **RyanCavanaugh** added label `Domain: JS Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/37619#issuecomment-3613088586) **HolgerJeromin** said "probably duplicate of or related to #39603"
 * [today](https://github.com/microsoft/TypeScript/issues/37619#issuecomment-3613516010) **RyanCavanaugh** said "module=none and outFile are both being deprecated in 6.0."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#3841](https://github.com/microsoft/TypeScript/issues/3841) (Open, `Suggestion`, `In Discussion`)

**T\.constructor should be of type T**

*Suggest typing instance.constructor as the class type rather than Function to enable direct static property access without casting.*

 * [today](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3611367593) **alvaro-cuesta** asked if they were missing something when `typeof this` didn’t work, noting that explicitly specifying each constructor worked
 * [today](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3612212409) **snarbles2** clarified that `this` and `typeof this` yield the same instance type and that `typeof this` does not refer to the constructor
 * [today](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3612606091) **FrameMuse** apologized for confusion and clarified that typeof this does not refer to the constructor inside the class body but does in static methods
 * [today](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3613012288) **ExE-Boss** corrected the type of C.constructor by explaining it’s globalThis.Function and provided a correct TypeScript definition

### [Issue microsoft/TypeScript#51612](https://github.com/microsoft/TypeScript/issues/51612) (Open, `Suggestion`, `Experimentation Needed`)

**Improve reverse mapped types inference by creating candidates from concrete index types**

*Improve TypeScript's reverse mapped types inference by using concrete index types to avoid circularity when inferring constrained properties.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-1369117038) **phryneas** provided a real-life example from Redux Toolkit illustrating wonky type inference, mentioned a TS PR rollback, and shared a Playground link
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-1375431039) **Andarist** described experimenting with TypeScript PR #52062 and RTK types and provided a proof-of-concept implementation
 * **RyanCavanaugh** added to milestone `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-3614423612) **RyanCavanaugh** shared a Copilot-generated summary of reverse mapped types in TypeScript, including definitions, examples, and a historical timeline of related issues and PRs
 * [today](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-3614455161) **RyanCavanaugh** provided a comprehensive list of demonstrative before/after samples for reverse mapped type PRs, illustrating fixes in PR #28494 and PR #31221

### [Issue microsoft/TypeScript#51789](https://github.com/microsoft/TypeScript/issues/51789) (Closed, `Bug`, `Won't Fix`, `ES6`, `Domain: JS Emit`)

**Downlevel TemplateStringsArray for tagged templates should be frozen**

*TypeScript should freeze TemplateStringsArray and its raw property for ES5-downleveled tagged templates to match the ES2015 spec.*

 * (1.7 years ago) **RyanCavanaugh** added label `Domain: JS Emit`, set milestone to `Backlog`, and removed from milestone `TypeScript 5.3.0`
 * (today) **DanielRosenwasser** added label `Out of Scope`, and unassigned **rbuckton**
 * [today](https://github.com/microsoft/TypeScript/issues/51789#issuecomment-3614688907) **DanielRosenwasser** said "We won't be addressing this - lowest supported ES target for TypeScript 6 is ES2015."
 * (today) **DanielRosenwasser** closed the issue
 * (today) **DanielRosenwasser** added label `Won't Fix`, and removed label `Out of Scope`

### [PR microsoft/TypeScript#51806](https://github.com/microsoft/TypeScript/pull/51806) (Closed, `Author: Team`, `For Backlog Bug`, **DanielRosenwasser**)

**Freeze Template Objects in \`\_\_makeTemplateObject\`**

*Update the __makeTemplateObject helper to deeply freeze template arrays for ES5 tagged template spec compliance and make raw non-enumerable*

 * (3 years ago) **typescript-bot** added labels `Author: Team`, `For Backlog Bug`
 * [51 weeks ago](https://github.com/microsoft/TypeScript/pull/51806#issuecomment-2529626011) **antongolub** recommended making the raw property non-enumerable per the spec and quoted the relevant spec section
 * [today](https://github.com/microsoft/TypeScript/pull/51806#issuecomment-3614687314) **DanielRosenwasser** said "We just no longer support ES5 as an output target starting with TS6."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#53017](https://github.com/microsoft/TypeScript/pull/53017) (Open, `For Backlog Bug`, **ahejlsberg**)

**Infer type parameters from indexes on those parameters**

*Infer generic type parameters in TypeScript based on index accesses of those parameters.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3603330533) **typescript-bot** reported user test results comparing main and merge, noted infrastructure failures and new TS2345 errors in webpack configs
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3603416171) **typescript-bot** provided performance run results for the requested perf tests
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3603562038) **typescript-bot** reported that running the top 400 repos with tsc on main versus the pull request produced no issues
 * [later](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3616509136) **Andarist** stated that the webpack break was acceptable and linked to a detailed write-up

### [PR microsoft/TypeScript#55222](https://github.com/microsoft/TypeScript/pull/55222) (Open, `Experiment`, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**Remove reportErrors check in relateVariances**

*Remove the reportErrors check in relateVariances to prevent inconsistent relation behavior in error and non-error modes.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-2248978424) **jakebailey** questioned whether retries would eventually prevent performance break and requested faster perf testing from the bot
 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-2248978489) **typescript-bot** reported that performance tests had started and provided status and results links
 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-2249022127) **typescript-bot** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3613507020) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3613507592) **typescript-bot** posted automated build status updates with links to started jobs and results
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3613632655) **typescript-bot** noted that the DT test results were ready and unchanged and provided a log link
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3613665151) **typescript-bot** reported user test results indicating a Git clone failure but otherwise no issues
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3613801361) **typescript-bot** provided the performance run results for tsc including comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3613929898) **typescript-bot** reported results of running tsc on top 400 repos comparing main and PR merge and noted everything looked good

### [PR microsoft/TypeScript#59745](https://github.com/microsoft/TypeScript/pull/59745) (Open, `For Backlog Bug`)

**Narrow destructured variables based on initializer's analysis result**

*Enhance destructured object variable type narrowing by using initializer control flow analysis instead of discriminant properties.*

 * created by **nekolab**
 * **typescript-bot** added label `For Backlog Bug`
 * [1.2 years ago](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-2308674849) **nekolab** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3615354334) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3615354460) **typescript-bot** reported CI build statuses and updated the results table
 * [today](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3615399170) **typescript-bot** reported that the DT test results were ready and everything looked the same
 * [today](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3615417612) **typescript-bot** reported test results and noted unrelated infrastructure failures
 * [today](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3615468257) **typescript-bot** provided requested performance run results with detailed comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3615530759) **typescript-bot** reported that tests on the top 400 repos comparing main and the PR merge all passed

### [Issue microsoft/TypeScript#60704](https://github.com/microsoft/TypeScript/issues/60704) (Open, `Needs Investigation`, **andrewbranch**)

**Rethink AutoImportProvider automatic limits**

*Propose replacing the ten-entrypoint cap on auto-import provider with depth-based module resolution limits to accommodate multi-export packages.*

 * (51 weeks ago) **andrewbranch** set milestones to `TypeScript 5.8.0`, `TypeScript 5.9.0`, and removed from milestone `TypeScript 5.8.0`
 * [today](https://github.com/microsoft/TypeScript/issues/60704#issuecomment-3613577715) **jedwards1211** questioned whether transitive module exports were being added to the auto import index and suggested limiting scans to only explicit dependencies' exposed modules

### [PR microsoft/TypeScript#61560](https://github.com/microsoft/TypeScript/pull/61560) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't set parent on non\-transient symbols in mergeSymbolTable**

*Avoid setting parent on non-transient symbols in mergeSymbolTable to prevent overwriting binder-created AST symbols*

 * [34 weeks ago](https://github.com/microsoft/TypeScript/pull/61560#issuecomment-2791009471) **typescript-bot** reported that running the user tests with tsc comparing main and the PR merge looked good
 * [34 weeks ago](https://github.com/microsoft/TypeScript/pull/61560#issuecomment-2791034280) **typescript-bot** reported the performance run results requested by @jakebailey
 * [34 weeks ago](https://github.com/microsoft/TypeScript/pull/61560#issuecomment-2791098122) **typescript-bot** reported that comparing tsc across the top 400 repos between main and the pull request showed everything looked good
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62388](https://github.com/microsoft/TypeScript/pull/62388) (Closed, **DanielRosenwasser**, **Copilot**)

**Change default target from ES5 to ESNext**

*TypeScript now defaults compilation target to ESNext instead of ES5, preserving modern syntax unless otherwise specified.*

 * created by **Copilot**
 * (13 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62389](https://github.com/microsoft/TypeScript/pull/62389) (Closed, **DanielRosenwasser**, **Copilot**)

**Deprecate \`baseUrl\` compiler option in TypeScript 6\.0**

*TypeScript 6.0 deprecates the baseUrl compiler option, emitting warnings and recommending explicit path mappings ahead of its TypeScript 7.0 removal.*

 * created by **Copilot**
 * (13 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62597](https://github.com/microsoft/TypeScript/pull/62597) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20251014202756512 to main**

*Merge of branch lego/hb_5378966c-b857-470a-8675-daebef4a6da1_20251014202756512 into main to include localized lcls.*

 * created by **csigs**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62640](https://github.com/microsoft/TypeScript/pull/62640) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove StyleMedia from DOM**

*Remove StyleMedia from DOM definitions in the TypeScript-DOM-lib-generator as tested in PR 2199.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/62640#issuecomment-3482066762) **jakebailey** said "@typescript-bot run dt"
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/62640#issuecomment-3482067167) **typescript-bot** reported CI build status for run dt with links to start and results
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/62640#issuecomment-3482157880) **typescript-bot** notified that the DT test results were ready and unchanged
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62764](https://github.com/microsoft/TypeScript/pull/62764) (Open, `For Backlog Bug`)

**Fix import path completions for wildcard patterns with extensions**

*Fix import path completions for package.json exports using wildcard patterns with extensions by broadening detection and appending suffixes.*

 * created by **PaulyBearCoding**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62764#issuecomment-3613586528) **jakebailey** said "this PR contains random unrelated changes from another PR"

### [PR microsoft/TypeScript#62801](https://github.com/microsoft/TypeScript/pull/62801) (Closed, `For Uncommitted Bug`)

**Add failing test for reverse mapped \`this\` leak \(\#62779\)**

*Add a failing compiler test demonstrating a reverse-mapped `this` leak that causes incorrect generic key inference.*

 * created by **priyankagnana**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/62801#issuecomment-3572665541) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62801#issuecomment-3613425259) **jakebailey** said "We don't need a PR for the failing test alone. The issue already has it, so we should add this when the issue is fixed."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62805](https://github.com/microsoft/TypeScript/pull/62805) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20251125204230298 to main**

*Merge localized lcls updates from branch lego/hb_5378966c-b857-470a-8675-daebef4a6da1 into the main branch.*

 * created by **csigs**
 * (1 week ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62810](https://github.com/microsoft/TypeScript/pull/62810) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20251126202423451 to main**

*A pull request merging localized lcls changes from branch lego/hb_5378966c-b857-470a-8675-daebef4a6da1_20251126202423451 into the main branch.*

 * created by **csigs**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62826](https://github.com/microsoft/TypeScript/pull/62826) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20251202202837239 to main**

*Pull request merges branch lego/hb_5378966c-b857-470a-8675-daebef4a6da1_20251202202837239 into main with localized lcls changes.*

 * created by **csigs**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62829](https://github.com/microsoft/TypeScript/issues/62829) (Open, `Needs Investigation`, **andrewbranch**)

**How to trace/debug auto import suggestions?**

*Enable tsserver debug logging to diagnose why auto-import suggestions are missing for an ESM package*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3608828162) **jedwards1211** thanked for the tip, described having more than 10 entry points for utilities, reported that enabling 'Include package json auto imports' had no effect, noted the same issue with es-toolkit, referenced MUI's guidance to avoid barrel imports, and suggested limiting suggestions based on package size rather than entry point count
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3608950076) **RyanCavanaugh** offered that they were rewriting auto-imports in TS7 with smarter bail-out heuristics and asked the user to publish their package or include it in tsgo for investigation
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3610454675) **jedwards1211** shared a link to their npm package, described including CJS, ESM, source, declaration maps, and original source files, questioned if that trips tsserver, and mentioned needing to try tsgo
 * (today) **RyanCavanaugh** added label `Needs Investigation`, removed label `Needs More Info`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3613259577) **andrewbranch** mentioned a related TypeScript issue and said he was reworking the backend of tsgo auto-imports to avoid the mentioned issues
 * [today](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3613631406) **jedwards1211** said "@andrewbranch if it still bails out anywhere after your changes, could you at least make it log where and why it bailed out?  (if tsgo doesn't already, I haven't tried tsgo yet)"
 * [today](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3613881151) **andrewbranch** said "There's no bail-out in my new version; the design is totally different such that that wouldn’t make sense / be possible."
 * [today](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3614138523) **jedwards1211** asked whether auto imports would dynamically look things up and include an OOM bail-out when too many dependencies exceed memory
 * [today](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3614193302) **andrewbranch** explained why the rewrite’s auto-imports system uses separate buckets for project and node_modules files, avoids retaining ASTs for memory efficiency, and aligns with user expectations
 * [today](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3614579761) **jedwards1211** mentioned building an auto import server for Flow that indexed import statements and exports, which led to high memory usage while offering advanced sorting and suggestion features

### [Issue microsoft/TypeScript#62831](https://github.com/microsoft/TypeScript/issues/62831) (Closed, `Duplicate`)

**Overriding fields of a generic object using spread operator results in incorrect types**

*Using spread to override generic object properties yields incorrect intersection types instead of properly omitting and replacing original fields.*

 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62831#issuecomment-3612714470) **wnadurski** asked to keep the issue open for clearer reference and communication of the bug until it’s fixed
 * [today](https://github.com/microsoft/TypeScript/issues/62831#issuecomment-3612864462) **jcalz** said "#42690 is open 🤷‍♂️"
 * [today](https://github.com/microsoft/TypeScript/issues/62831#issuecomment-3613150839) **wnadurski** said "Oh, true then I agree we can close this issue"
 * (today) **wnadurski** closed the issue

### [PR microsoft/TypeScript#62832](https://github.com/microsoft/TypeScript/pull/62832) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20251203202848732 to main**

*Pull request merging localized LCLS changes from lego/hb_5378966c-b857-470a-8675-daebef4a6da1_20251203202848732 into main.*

 * created by **csigs**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62834](https://github.com/microsoft/TypeScript/pull/62834) (Closed, `For Uncommitted Bug`)

**Rename mock and require file references**

*Automatically update jest.mock, vitest.mock, require, and import file references when files are renamed*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3609308696) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3609308990) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3609364793) **hjonasson** quoted the Contributor License Agreement instructions and full agreement text
 * [today](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3614780976) **DanielRosenwasser** explained that contributors should wait for issues to be triaged, noted that new language service PRs are not being accepted, and referenced ongoing work in typescript-go
 * [today](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3615636887) **hjonasson** appreciated feedback and asked where to place tool-specific code outside the language server

### [Issue microsoft/TypeScript#62835](https://github.com/microsoft/TypeScript/issues/62835) (Open, `Suggestion`, `Awaiting More Feedback`)

**Update test framework mock paths during file rename operations**

*Automatically update string literal paths in jest.mock and vitest.mock during TypeScript file rename or move to avoid broken tests.*

 * created by **hjonasson**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62835#issuecomment-3610365760) **MartinJohns** questioned how the compiler would distinguish paths from strings and noted it would require a change like #42054 or specific test frameworks
 * [today](https://github.com/microsoft/TypeScript/issues/62835#issuecomment-3612334286) **jcalz** asked if 'hardcore' was a typo for 'hardcode'
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#62838](https://github.com/microsoft/TypeScript/issues/62838) (Closed, `Duplicate`)

**\`JSON\.stringify\(undefined\)\` incorrectly types the return value as \`string\`**

*JSON.stringify(undefined) is typed as returning string in TypeScript instead of undefined.*

 * [today](https://github.com/microsoft/TypeScript/issues/62838#issuecomment-3612849310) **MartinJohns** said "Duplicate of #18879."
 * [today](https://github.com/microsoft/TypeScript/issues/62838#issuecomment-3612897786) **afgomez** said "Oh! sorry for the noise. I only searched for JSON.stringify() in the open issues and I didn't find anything 😅."
 * [today](https://github.com/microsoft/TypeScript/issues/62838#issuecomment-3612938075) **MartinJohns** said "Searching with parentheses won't yield any result either way. Best results are with an added search modifier: JSON.stringify in:title"
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#62839](https://github.com/microsoft/TypeScript/pull/62839) (Closed, `For Backlog Bug`)

**Fix reverse mapped contextual this inference leak**

*Skip reverse-mapped apparent types when computing contextual “this” to fix inference leaks and add a regression test for reverseMappedTypeParameterLeak.*

 * created by **learn-dumboo24**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62839#issuecomment-3612953132) **learn-dumboo24** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/62839#issuecomment-3613421629) **jakebailey** said "You completely broke checker.ts; I'm not sure what this PR is."
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/62839#issuecomment-3613573056) **learn-dumboo24** said "I am extremely sorry, day before yesterday I pulled for latest changes and tested on local it I thought it worked but again sorry sir @jakebailey  "

### [PR microsoft/TypeScript#62840](https://github.com/microsoft/TypeScript/pull/62840) (Open, `For Uncommitted Bug`)

**Enhance isJS check in getNewImportFixes function**

*Prioritize scriptKind over file extension in getNewImportFixes to ensure consistent JsdocTypeImport behavior for files added via LS plugins.*

 * created by **johnsoncodehk**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62840#issuecomment-3614219786) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62840#issuecomment-3614219802) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#62841](https://github.com/microsoft/TypeScript/issues/62841) (Closed, `Suggestion`, `Committed`, `Fix Available`)

**Module Resolution: allow subpath imports that start with \`\#/\`**

*Allow `#/`-prefixed subpath imports in TypeScript’s module resolution to support matching `imports` and `exports` fields in package.json.*

 * created by **Boshen**

### [Issue microsoft/TypeScript#62842](https://github.com/microsoft/TypeScript/issues/62842) (Open, `Suggestion`, `Awaiting More Feedback`)

**Consider deprecating \`\<prefix\>\` type assertions**

*Deprecate legacy `<type>value` assertions in TypeScript in favor of modern `value as type` syntax for improved compatibility and consistency.*

 * created by **robpalme**

### [PR microsoft/TypeScript#62843](https://github.com/microsoft/TypeScript/pull/62843) (Open, `For Uncommitted Bug`)

**Fix TS2742 false positive for self\-imports in declaration files**

*Update module resolution to redirect self-imports in .d.ts files to emitted declaration files, preventing false TS2742 errors during project builds.*

 * created by **976520**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62843#issuecomment-3617345262) **976520** said "@microsoft-github-policy-service agree"

