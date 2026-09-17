# Report for 2026-09-11 (Friday, September 11th, 2026)

16 different users commented on 22 different issues.

## Recommended Actions

 * Response Recommended
    * @victorafael26 provided repro steps as requested in [microsoft/TypeScript#31146](https://github.com/microsoft/TypeScript/issues/31146#issuecomment-5639488166)
    * @victorafael26 provided a detailed repro example in [microsoft/TypeScript#47599](https://github.com/microsoft/TypeScript/issues/47599#issuecomment-5639488754)
    * @typescript-automation[bot] reported user test results with infrastructure failures in [microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5639086368)
    * @typescript-automation[bot] reported TypeScript comparison results and requested review of failures in [microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5639720336)
    * @typescript-automation[bot] reported user test results with infrastructure failures in [microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642382933)
    * @typescript-automation[bot] reported build failures for triggerdotdev/trigger.dev that require review in [microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642708165)
    * @SetTrend suggested adding a link to the TS FAQ in lib to clarify usage of isFinite in [microsoft/TypeScript#64244](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5640638046)
    * @SetTrend asked whether maintainers should consider MDN users in JsDoc documentation in [microsoft/TypeScript#64244](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5645885126)

## Activity Summary

### [Issue microsoft/TypeScript#16597](https://github.com/microsoft/TypeScript/issues/16597) (Open, `Suggestion`, `In Discussion`)

**Allow specifying only a subset of generic type parameters explicitly instead of all vs none**

*Allow partial generic parameter specification so TypeScript infers remaining type arguments when only some are provided*

 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/16597#issuecomment-996203502) **bliddicott-scottlogic** mentioned another use case for specifying the first type parameter in Object.assign to enable excess property checks
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/16597#issuecomment-1226676069) **shicks** suggested using an opt-in inference syntax and provided examples for an assertExactType utility to test type inference
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/16597#issuecomment-1230849820) **shicks** suggested preventing explicit specification of inferred parameters by using a syntax with 'infer'
 * [today](https://github.com/microsoft/TypeScript/issues/16597#issuecomment-5639955238) **jedwards1211** described currying’s type correctness and runtime overhead and suggested that implementing the feature would eliminate the overhead

### [Issue microsoft/TypeScript#31146](https://github.com/microsoft/TypeScript/issues/31146) (Open, `Bug`, `Domain: check: Type Inference`, `Cursed?`)

**Cannot infer generic argument type from passed callback**

*TypeScript cannot infer a generic type from a callback using destructured default parameters, causing missing type errors for invalid arguments.*

 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/31146#issuecomment-696104041) **lxsmnsyc** mentioned that using test required explicitly defining T and attached a screenshot
 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/31146#issuecomment-696398719) **theonlypwner** described a TypeScript type inference regression in TS 3.7–4.0 when inferring nested callback types and contrasted it with C# behavior
 * **RyanCavanaugh** added label `Cursed?`
 * [today](https://github.com/microsoft/TypeScript/issues/31146#issuecomment-5639488166) **victorafael26** reported that the bug still persisted in TypeScript 5.9.3 and the new Go-based compiler 7.0.2 and provided a minimal repro

### [Issue microsoft/TypeScript#47599](https://github.com/microsoft/TypeScript/issues/47599) (Open, `Suggestion`, `Help Wanted`, `Experimentation Needed`)

**Improve inference in the presence of context\-sensitive expressions**

*Improve generic inference by allowing context-sensitive expressions in object literals to contribute to type parameter inference*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/47599#issuecomment-3161522727) **geleto** explained how `as const` isolates the object from context-sensitive inference, preventing type widening and aligning with the const T proposal
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/47599#issuecomment-3163512048) **geleto** performed an AI analysis of related issues and categorized them into three groups, concluding that adding a <const T> modifier would resolve most cases and suggested opening a feature request
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/47599#issuecomment-3163821898) **Andarist** disputed the perception of const context, noted existing fixes, and shared his bug report, proposed fix link, and ongoing algorithm improvement work
 * [today](https://github.com/microsoft/TypeScript/issues/47599#issuecomment-5639488754) **victorafael26** provided a real-world example illustrating a TypeScript generic inference bug with inline callbacks in a lazyLoad helper

### [PR microsoft/TypeScript#64172](https://github.com/microsoft/TypeScript/pull/64172) (Closed, `For Backlog Bug`)

**Infer recursive types through object literal getters**

*Fix recursive type inference in object getters by adding a recursion-depth sentinel to avoid circular resolution errors*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5594267273) **colinhacks** thanked and described a feature request for improved recursive inference support and input constraints in z.object
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5595011378) **jakebailey** said "Pushed even more code to my branch, which seems to get rid of all errors from your "Zod with every workaround removed" checkout."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5623908121) **colinhacks** confirmed that commit e707147a48 compiled Zod without workarounds, validated that the getter shape worked, proposed supporting additional syntax patterns via separate commits, and asked whether to create a combined PR or defer to @RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5638879151) **colinhacks** said "Superseded by #64248."
 * (today) **colinhacks** closed the issue

### [Issue microsoft/TypeScript#64203](https://github.com/microsoft/TypeScript/issues/64203) (Closed, `Unactionable`)

**\`\-\-stableTypeOrdering\` defects: compiler hang \(NaN in \`compareNodes\`\), missing \`BigIntLiteral\`, primitive alias bypass, and mapper omissions**

*The --stableTypeOrdering compiler option hangs due to NaN in compareNodes and misorders BigIntLiteral, primitive aliases, and type mappers.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64203#issuecomment-5592506665) **trevorade** apologized and described a fix to compareNodes that safely handled missing fileIndexMap entries and undefined node positions to avoid NaN and infinite hangs
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64203#issuecomment-5592602239) **RyanCavanaugh** said "It sounds like maybe your createProgram call and/or host made some conflicting statements about what files exist? Regardless, this doesn't sound like something we'd patch 6.0 for."
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64203#issuecomment-5597512492) **jakebailey** said "I noticed a few of these originally but avoided sending a PR to not have 6.0 differ, so 7.1 is definitely the right time to fix this class of problem "
 * [today](https://github.com/microsoft/TypeScript/issues/64203#issuecomment-5642490940) **typescript-automation[bot]** said "This issue has been marked as "Unactionable" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64231](https://github.com/microsoft/TypeScript/issues/64231) (Open, `Bug`)

**Parser misinterprets async\(\) calls in conditional expressions as async arrow functions**

*TypeScript parser misinterprets calls to a function named async in ternary expressions as async arrow functions, causing syntax errors.*

 * created by **camc314**
 * (today) **DanielRosenwasser** added label `Bug`, and set milestone to `TypeScript 7.1.0 Beta`

### [PR microsoft/TypeScript#64233](https://github.com/microsoft/TypeScript/pull/64233) (Open, `For Milestone Bug`)

**fix\(64231\): avoid parsing async\(\) calls as typed arrows in conditionals**

*Prevent parser from misinterpreting async() calls in conditionals as typed arrow functions.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64233#issuecomment-5625472509) **DanielRosenwasser** said "@typescript-bot test top800"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64233#issuecomment-5625473438) **typescript-automation[bot]** reported that the test top800 build job started and results links were provided
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64233#issuecomment-5626219351) **typescript-automation[bot]** reported comparison results for the top 800 repos with tsc and stated everything looked good
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64234](https://github.com/microsoft/TypeScript/pull/64234) (Closed, `For Milestone Bug`)

**Fix parsing of async\(\) calls in conditional expressions**

*Parser misinterprets async() in conditional expressions as arrow functions, causing syntax errors in .ts and .js files.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64234#issuecomment-5623464092) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Distinguish between non\-distributed and distributed type parameters**

*TypeScript now differentiates distributed and non-distributed type parameters in conditional types, reports constraint violations accordingly, and marks distributed parameters with a (distributed) hover indicator.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626093306) **typescript-automation[bot]** reported CI jobs starting and posted initial build status
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626345370) **typescript-automation[bot]** reported user test results comparing main and refs/pull/64237/merge, noted two package install failures and one git clone failure likely unrelated to the change, and confirmed everything else looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5626870537) **typescript-automation[bot]** reported build failures in Dokploy/dokploy when comparing main and pull request merge
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5638513963) **DanielRosenwasser** said "Jeez - I think we need to close the coverage gap between RWC and our own test suite. Probably worth adding tests for things like the Exact pattern here (both the original and a corrected one)."
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5638622283) **Andarist** noted that homomorphic mapped types also distribute and suffer the same issue, linked to a comparison branch with a proposed fix, and questioned whether the resulting breakages are correct, illustrating with a code example
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5638786582) **ahejlsberg** requested the typescript-bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5638787600) **typescript-automation[bot]** reported CI job statuses and results for 'user test this' and 'test top1000'
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5639086368) **typescript-automation[bot]** reported user test results comparing main and refs/pull/64237/merge, noted two package install failures and one git clone failure likely unrelated to the change, and confirmed everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5639720336) **typescript-automation[bot]** reported the results of running the top 1000 repos with tsc comparing main and the PR merge and highlighted unexpected build failures in Dokploy
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5639970587) **ahejlsberg** reported tests as clean except for three failures, two expected, and requested help chasing down new dokploy errors involving Zod and custom types
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5640957517) **DanielRosenwasser** mentioned that getActualTypeVariable shouldn't always call getNonDistributedTypeParameter and asked if it could be omitted in the branch
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5641061220) **Andarist** explained the reasoning for expanding getActualTypeVariable to handle reverse mapped types, described the need for recursive unwrapping, and shared an experimental patch
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642031478) **ahejlsberg** examined all uses of getActualTypeVariable and confirmed it should only return non-distributed type parameters, verifying it fixes the dokploy issue without causing other changes
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642107290) **ahejlsberg** said "@Andarist Borrowed your regression test, thanks for researching."
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642209691) **ahejlsberg** requested the typescript-bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642210141) **typescript-automation[bot]** posted build status updates for the ‘user test this’ and ‘test top1000’ jobs
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642382933) **typescript-automation[bot]** reported user test results comparing main and refs/pull/64237/merge, noted two package install failures and one git clone failure likely unrelated to the change, and confirmed everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642708165) **typescript-automation[bot]** reported build comparison results for the top 1000 repos between main and pull/64237/merge and highlighted failures in triggerdotdev/trigger.dev

### [PR microsoft/TypeScript#64243](https://github.com/microsoft/TypeScript/pull/64243) (Open, `For Uncommitted Bug`)

**fix: disallow NoSubstitutionTemplate in module import attribute types**

*Enforce rejecting empty template literals in module import attribute types by requiring quoted string literals.*

 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5633219206) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64243#issuecomment-5638319287) **DanielRosenwasser** appreciated test coverage and asked if there are tests for template string types with interpolations, requesting their addition if missing

### [Issue microsoft/TypeScript#64244](https://github.com/microsoft/TypeScript/issues/64244) (Closed, `Working as Intended`)

**The isFinite\(\) type declaration doesn't specify the right type**

*The TypeScript declaration for global isFinite incorrectly specifies its parameter as number instead of any.*

 * [today](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5636239350) **MartinJohns** said "This is intentional. Duplicate of #4002."
 * [today](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5636529014) **RyanCavanaugh** said "https://github.com/Microsoft/TypeScript/wiki/FAQ#numberisfinite-and-numberisnan-are-typed-correctly"
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5640638046) **SetTrend** suggested adding a link to the TypeScript FAQ in the lib declaration to reduce confusion about isFinite usage
 * [today](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5640766744) **RyanCavanaugh** noted that the library typing was intentional and cited MDN's warning against using isFinite due to coercion
 * [later](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5645885126) **SetTrend** suggested considering MDN documentation users in the JsDoc docs for isFinite instead of expecting them to refer to the wiki

### [PR microsoft/TypeScript#64245](https://github.com/microsoft/TypeScript/pull/64245) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Generate optional protocol properties with \`\| undefined\` so we can stop doing silly spreads to satisfy \`exactOptionalPropertyTypes\`**

*Generate optional protocol properties with `| undefined` in the API to avoid unnecessary spreads for exactOptionalPropertyTypes*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64245#issuecomment-5637669569) **mrazauskas** thanked and suggested reinstating readonly arrays for all response objects due to inconsistent readonly usage in Diagnostic properties
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64246](https://github.com/microsoft/TypeScript/pull/64246) (Closed, `For Milestone Bug`, **andrewbranch**)

**fix\(syncChannel\): give child process time to exit before kill in close\(\)**

*Modify the syncChannel close() method to wait briefly for child processes to exit gracefully before force-killing them.*

 * created by **biisal**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64247](https://github.com/microsoft/TypeScript/pull/64247) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add program\.getResolvedModule and similar**

*Add program.getResolvedModule and other API methods to expose module resolution functionality and allow resolution overrides.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64248](https://github.com/microsoft/TypeScript/pull/64248) (Open, `For Backlog Bug`)

**Infer recursive types through self\-referential object literals**

*Enable correct recursive type inference in self-referential object literals by deferring type constraint checks.*

 * created by **colinhacks**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#64249](https://github.com/microsoft/TypeScript/issues/64249) (Open, `Needs Investigation`, **weswigham**)

**Spurious TS4094 "exported anonymous class type may not be private" error after upgrading from TS6 to TS7**

*Upgrading from TypeScript 6 to 7 causes TS4094 errors on exported anonymous ZodRoute instances due to private class properties.*

 * created by **jedwards1211**

### [PR microsoft/TypeScript#64250](https://github.com/microsoft/TypeScript/pull/64250) (Open, `For Uncommitted Bug`)

**Remove duplicated comments on legacy decorators**

*Remove duplicated comments from legacy decorators to avoid redundant documentation*

 * created by **user454322**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64250#issuecomment-5644421936) **microsoft-github-policy-service[bot]** provided instructions to sign the Contributor License Agreement by replying with an 'agree' command

### [Issue microsoft/TypeScript#64251](https://github.com/microsoft/TypeScript/issues/64251) (Open, `Possible Improvement`)

**Object with all context\-sensitive properties requires at least one non\-context\-sensitive property for inference to work**

*createMachine type inference for context and state fails when all state properties are context-sensitive unless a dummy property is added*

 * created by **devanshj**

### [PR microsoft/TypeScript#64252](https://github.com/microsoft/TypeScript/pull/64252) (Open, `For Backlog Bug`)

**Fix reverse mapped type inference when all properties are context\-sensitive**

*Improve reverse mapped type inference to correctly handle scenarios where every property is context-sensitive.*

 * created by **devanshj**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5646221240) **devanshj** thanked the catch and noted that they tweaked userland types to fix the issue, mentioning the compiler was already good

### [Issue microsoft/TypeScript#64253](https://github.com/microsoft/TypeScript/issues/64253) (Open, `Suggestion`)

**Anonymous Symbol Properties**

*Allow inline declaration of unique symbol keys on object types to define anonymous single-use phantom properties without separate declarations*

 * created by **RonaldBunk**

