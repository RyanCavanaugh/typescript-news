# Report for 2026-09-10 (Thursday, September 10th, 2026)

20 different users commented on 26 different issues.

## Recommended Actions

 * Response Recommended
    * @LukeAbby provided detailed bug analysis and repro steps in [microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5631883925)
    * @colinhacks asked whether to create this combined PR or if @RyanCavanaugh would work on it in [microsoft/TypeScript#64172](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5623908121)
    * @nmain asked to make the example complete due to TS2339 errors and absence of TS1111 in [microsoft/TypeScript#64228](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5622172507)
    * @errorx666 asked for further feedback on the code in [microsoft/TypeScript#64229](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5636684265)
    * @errorx666 asked whether the type error was related to optional chaining logic in [microsoft/TypeScript#64229](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5636716584)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5624761102)
    * @typescript-automation[bot] asked to review the test results including failures and errors in [microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5625177862)
    * @typescript-automation[bot] asked to review build results of the top 1000 repos in [microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5625419140)
    * @typescript-automation[bot] reported user test results with infrastructure failures in [microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626345370)
    * @typescript-automation[bot] reported build failures for Dokploy/dokploy and requested review in [microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626870537)

## Activity Summary

### [Issue microsoft/TypeScript#63708](https://github.com/microsoft/TypeScript/issues/63708) (Open, `Possible Improvement`, **ahejlsberg**)

**It is possible to violate generic constraints when distributing union types**

*Distributive union types in TypeScript can bypass generic constraints, allowing invalid B extends A combinations without error.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5453841089) **ahejlsberg** agreed that assumptions made involving distributed A didn't always hold and explained that distributed A should behave as a new type variable extending the non-distributed A, noting naming confusion
 * (1 week ago) **ahejlsberg** added label `Possible Improvement`, and removed label `Design Limitation`
 * [today](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5624424809) **ahejlsberg** said "A fix is now available in #64237."
 * **ahejlsberg** added to milestone `TypeScript 7.1.0 Beta`

### [PR microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types**

*Add support for a 'not T' negated type operator with canonical simplification rules and enhanced control flow handling*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [later](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5631883925) **LukeAbby** described bugs in fresh literal type exactness logic and provided reproduction examples

### [PR microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Build Orchestrator API **

*Implement a new BuildOrchestrator API with build, buildReferences, clean, and cleanReferences methods replacing SolutionBuilder*

 * (1 week ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5621539680) **dragomirtitian** asked whether the new BuildOrchestrator supports diagnostics retrieval, file-specific checks, batched emits, and SourceFile access and inquired about plans to add these features
 * [today](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5627049841) **iisaduan** explained the PR scope for build orchestrator diagnostics, deferred watch functionality to a future PR, noted that emit output isn't returned via IPC, and asked which tool was used for per-file diagnostics
 * [today](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5630670307) **dragomirtitian** asked if the incremental program could be reinstated and noted possible misunderstanding about emit output via VFS writes

### [PR microsoft/TypeScript#64172](https://github.com/microsoft/TypeScript/pull/64172) (Closed, `For Backlog Bug`)

**Infer recursive types through object literal getters**

*Fix recursive type inference in object getters by adding a recursion-depth sentinel to avoid circular resolution errors*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5593017044) **jakebailey** provided a proof-of-concept implementation using Astra via linked branch and commit
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5594267273) **colinhacks** thanked and described a feature request for improved recursive inference support and input constraints in z.object
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5595011378) **jakebailey** said "Pushed even more code to my branch, which seems to get rid of all errors from your "Zod with every workaround removed" checkout."
 * [today](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5623908121) **colinhacks** confirmed that commit e707147a48 compiled Zod without workarounds, validated that the getter shape worked, proposed supporting additional syntax patterns via separate commits, and asked whether to create a combined PR or defer to @RyanCavanaugh

### [PR microsoft/TypeScript#64173](https://github.com/microsoft/TypeScript/pull/64173) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Port content mapper inspector extension into bundled extension**

*Port the Content Mapper Inspector extension into the bundled extension, requiring js/ts.showDebugInfo to expose its commands*

 * (6 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue
 * (today) **andrewbranch** reopened the issue

### [Issue microsoft/TypeScript#64197](https://github.com/microsoft/TypeScript/issues/64197) (Closed, `Duplicate`)

**Excess property checks silently skipped for nested object literals at reverse\-mapped\-type inference sites \(regression in 6\.0\)**

*TypeScript 6.0 regression stops flagging excess properties on nested object literals in generic reverse-mapped type inference.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64197#issuecomment-5584520796) **MartinJohns** said "Very likely a duplicate of #64006."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64197#issuecomment-5590744319) **RyanCavanaugh** confirmed that the issue also bisected to #62722 and linked to a related comment
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/64197#issuecomment-5627959346) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64228](https://github.com/microsoft/TypeScript/issues/64228) (Open, `Needs More Info`)

**Incorrect TS1111 when using private generator function in JS**

*VSCode erroneously raises TS1111 error when invoking a private generator method on another instance within a class.*

 * created by **Ecco**
 * [today](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5622172507) **nmain** said "Could you make sure your example is complete?  When I copy your code to a playground I get a few TS2339 but no TS1111."

### [Issue microsoft/TypeScript#64229](https://github.com/microsoft/TypeScript/issues/64229) (Open, `Design Limitation`)

**nullish types not narrowed in if block**

*Optional chaining and nullish coalescing conditions do not narrow nullish types within if blocks in TypeScript.*

 * created by **errorx666**
 * [today](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5621832263) **snarbles2** provided a simplified conditional using optional chaining and noted that a comparison operator made the expression too complex for the control flow analysis
 * [later](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5636684265) **errorx666** updated code per suggestion but preferred original approach and requested further feedback
 * [later](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5636716584) **errorx666** asked whether the issue was related to using optional chaining in a comparison, noting that nullish values can't be greater than zero so it behaves as intended

### [Issue microsoft/TypeScript#64231](https://github.com/microsoft/TypeScript/issues/64231) (Open, `Bug`)

**Parser misinterprets async\(\) calls in conditional expressions as async arrow functions**

*TypeScript parser misinterprets calls to a function named async in ternary expressions as async arrow functions, causing syntax errors.*

 * created by **camc314**

### [PR microsoft/TypeScript#64232](https://github.com/microsoft/TypeScript/pull/64232) (Open, `For Backlog Bug`)

**Fixed detection of optional chains containing a reference**

*Fixes detection of optional chains containing references in the TypeScript compiler.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64233](https://github.com/microsoft/TypeScript/pull/64233) (Open, `For Milestone Bug`)

**fix\(64231\): avoid parsing async\(\) calls as typed arrows in conditionals**

*Prevent parser from misinterpreting async() calls in conditionals as typed arrow functions.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64233#issuecomment-5625472509) **DanielRosenwasser** said "@typescript-bot test top800"
 * [today](https://github.com/microsoft/TypeScript/pull/64233#issuecomment-5625473438) **typescript-automation[bot]** reported that the test top800 build job started and results links were provided
 * [today](https://github.com/microsoft/TypeScript/pull/64233#issuecomment-5626219351) **typescript-automation[bot]** reported comparison results for the top 800 repos with tsc and stated everything looked good

### [PR microsoft/TypeScript#64234](https://github.com/microsoft/TypeScript/pull/64234) (Closed, `For Milestone Bug`)

**Fix parsing of async\(\) calls in conditional expressions**

*Parser misinterprets async() in conditional expressions as arrow functions, causing syntax errors in .ts and .js files.*

 * created by **mohit-nayak**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64234#issuecomment-5623464092) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64235](https://github.com/microsoft/TypeScript/issues/64235) (Open, `Suggestion`, `Domain: LS: Outlining`, `Experimentation Needed`, **gabritto**)

**Include terminating line in folding ranges when last token has no trailing non\-trivia**

*Propose enhancing lineFoldingOnly support by including closing-brace lines in folding ranges when the terminating line contains no non-trivia content.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Suggestion`, `Domain: LS: Outlining`, `Experimentation Needed`, set milestone to `TypeScript 7.1.0 Beta`, assigned to **DanielRosenwasser**, **gabritto**, and unassigned **DanielRosenwasser**

### [PR microsoft/TypeScript#64236](https://github.com/microsoft/TypeScript/pull/64236) (Closed, `For Uncommitted Bug`, **DanielRosenwasser**)

**fix\(checker\): reject exports originating from global augmentations**

*Reject exports of symbols declared within global scope augmentation modules by enhancing the export specifier check.*

 * created by **erantianantha**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/64236#issuecomment-5625544471) **DanielRosenwasser** said "Sorry, there's already a PR out at #64162."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237) (Open, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Distinguish between non\-distributed and distributed type parameters**

*TypeScript now differentiates distributed and non-distributed type parameters in conditional types, reports constraint violations accordingly, and marks distributed parameters with a (distributed) hover indicator.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5624374592) **ahejlsberg** requested the typescript-bot to run performance tests faster and to execute the top1000 test suite
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5624375539) **typescript-automation[bot]** reported CI jobs starting and provided links for status and results
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5624761102) **typescript-automation[bot]** reported the requested performance run results including comparison metrics between baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5624860374) **ahejlsberg** said "@typescript-bot user test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5624861309) **typescript-automation[bot]** posted a build status table showing the 'user test this' job started
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5625177862) **typescript-automation[bot]** reported tsc user-test results comparing main and pull request merge, noted infrastructure failures and new TS2345 errors, and asked to review the changes
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5625419140) **typescript-automation[bot]** reported build failures when comparing main and the pull request and asked to review the differences
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626085161) **ahejlsberg** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626085985) **typescript-automation[bot]** updated build status for test top1000 with links
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626092498) **ahejlsberg** said "@typescript-bot user test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626093306) **typescript-automation[bot]** reported CI jobs starting and posted initial build status
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626345370) **typescript-automation[bot]** reported user test results comparing main and refs/pull/64237/merge, noted two package install failures and one git clone failure likely unrelated to the change, and confirmed everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626870537) **typescript-automation[bot]** reported build failures in Dokploy/dokploy when comparing main and pull request merge

### [PR microsoft/TypeScript#64238](https://github.com/microsoft/TypeScript/pull/64238) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add security skill**

*Add a security skill warning that TypeScript compiler (tsc) runtime delays do not constitute a security boundary.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64239](https://github.com/microsoft/TypeScript/pull/64239) (Open, `For Uncommitted Bug`, **ahejlsberg**)

**Fixed a crash related to variadic tuple elements with intersections containing \`InstantiableNonPrimitive\`**

*Fixed a compiler crash triggered by variadic tuple elements intersecting with InstantiableNonPrimitive types.*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#64240](https://github.com/microsoft/TypeScript/issues/64240) (Open, `Bug`, **andrewbranch**)

**API panics when serializing number literal types with \`\+Infinity\` and \`\-Infinity\`**

*TypeScript’s unstable sync API panics when serializing number literal types representing +Infinity or -Infinity.*

 * created by **auvred**

### [PR microsoft/TypeScript#64241](https://github.com/microsoft/TypeScript/pull/64241) (Open, `For Milestone Bug`, **andrewbranch**)

**Properly serialize \`\+Infinity\`, \`\-Infinity\`, and \`NaN\` number literal type values in API**

*Implement correct serialization of +Infinity, -Infinity, and NaN number literals in the API.*

 * created by **auvred**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64242](https://github.com/microsoft/TypeScript/issues/64242) (Open, `Needs Investigation`, **andrewbranch**)

**Sporadic \`context canceled\` in \`stderr\` when running TypeScript API in subprocess tests**

*Intermittent 'context canceled' output appears in stderr instead of empty when testing a CLI using TypeScript's API on Ubuntu CI.*

 * created by **mrazauskas**

### [PR microsoft/TypeScript#64243](https://github.com/microsoft/TypeScript/pull/64243) (Open, `For Uncommitted Bug`)

**fix: disallow NoSubstitutionTemplate in module import attribute types**

*Enforce rejecting empty template literals in module import attribute types by requiring quoted string literals.*

 * created by **camc314**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5633219206) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64244](https://github.com/microsoft/TypeScript/issues/64244) (Closed, `Working as Intended`)

**The isFinite\(\) type declaration doesn't specify the right type**

*The TypeScript declaration for global isFinite incorrectly specifies its parameter as number instead of any.*

 * created by **SetTrend**
 * [later](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5636239350) **MartinJohns** said "This is intentional. Duplicate of #4002."
 * [later](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5636529014) **RyanCavanaugh** said "https://github.com/Microsoft/TypeScript/wiki/FAQ#numberisfinite-and-numberisnan-are-typed-correctly"
 * **RyanCavanaugh** added label `Working as Intended`

