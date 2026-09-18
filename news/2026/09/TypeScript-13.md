# Report for 2026-09-13 (Sunday, September 13th, 2026)

7 different users commented on 25 different issues.

## Recommended Actions

 * Response Recommended
    * @anbv29 asked to be assigned the issue in [microsoft/TypeScript#30408](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-5661952649)
    * @anbv29 asked to be assigned to the issue in [microsoft/TypeScript#62915](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-5661966799)
    * @anbv29 asked for permission to work on the issue in [microsoft/TypeScript#63603](https://github.com/microsoft/TypeScript/issues/63603#issuecomment-5662383909)
    * @anbv29 asked if they could work on the issue in [microsoft/TypeScript#64231](https://github.com/microsoft/TypeScript/issues/64231#issuecomment-5662369126)

## Activity Summary

### [Issue microsoft/TypeScript#30408](https://github.com/microsoft/TypeScript/issues/30408) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Effort: Moderate`, `Domain: Error Messages`, `Experience Enhancement`)

**Confusing error message for labels used before definition**

*A continue to a label defined after a for loop incorrectly triggers a confusing TS1007 error.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-4254816118) **staticvariablejames** reported encountering a similar issue with a typo in the label and still getting TS1107 error in version 7.0.0-dev.20260415.1
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-5490013799) **LeonxLJX** said "I'd like to take this one — I'll follow up with a PR. (claiming via @LeonxLJX)"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-5492442687) **LeonxLJX** said "Hi! I'd like to improve the 'label used before definition' error message. Plan: reproduce, refine the message, add tests. May I be assigned?"
 * [later](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-5661952649) **anbv29** said "Hey, i would like to work on this. Can i be assigned this issue?"

### [Issue microsoft/TypeScript#62915](https://github.com/microsoft/TypeScript/issues/62915) (Open, `Help Wanted`, `Docs`)

**Document that compiler\.extends can be an array**

*Update tsconfig.json documentation to indicate that the compiler.extends option can accept an array of configurations.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [35 weeks ago](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-3723285450) **aaron-seq** announced intent to create a PR updating the TypeScript-Website documentation to clarify that `extends` can accept an array of configuration files
 * [34 weeks ago](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-3745705505) **saksham-sankhla04** said "Hi, I would Like to work on this"
 * [later](https://github.com/microsoft/TypeScript/issues/62915#issuecomment-5661966799) **anbv29** said "hey, can i be assigned this issue? I would love to work on it."

### [Issue microsoft/TypeScript#63603](https://github.com/microsoft/TypeScript/issues/63603) (Open, `Bug`, `Domain: LS: Completion Lists`)

**Issue: TypeScript autocomplete for template literal types ignores user's Quote Style preference**

*Autocomplete suggestions for template literal type keys always use double quotes, ignoring the user's configured quote style preference.*

 * (9 weeks ago) **RyanCavanaugh** added label `Domain: LS: Completion Lists`, and set milestone to `Backlog`
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63603#issuecomment-4977767143) **cooperbuilds** analyzed the hover implementation, identified that only one declaration's JSDoc is used, and asked if a PR to use merged documentation would be welcome
 * [later](https://github.com/microsoft/TypeScript/issues/63603#issuecomment-5662383909) **anbv29** asked to work on the issue

### [Issue microsoft/TypeScript#64213](https://github.com/microsoft/TypeScript/issues/64213) (Open, `Suggestion`)

**The \`strict\` option is confusing since TypeScript 6**

*TypeScript 6 makes strict true by default and false disables multiple strict checks, reversing its original purpose and confusing users.*

 * created by **remcohaszing**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64213#issuecomment-5603937116) **RyanCavanaugh** questioned who benefits from the proposal and asked for evidence of confusion around strict
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#64220](https://github.com/microsoft/TypeScript/pull/64220) (Open, `For Milestone Bug`, **johnfav03**)

**Schedule tsc \-b projects by dependency depth so builders do not idle on upstream projects**

*Sort tsc -b build tasks by dependency depth instead of depth-first references to reduce idle time and speed up parallel builds.*

 * created by **christianvuerings**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (later) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#64222](https://github.com/microsoft/TypeScript/issues/64222) (Open, `Needs Investigation`, **johnfav03**)

**tsc \-b: builders idle on upstream projects because projects are scheduled in depth\-first reference order**

*The build orchestrator's depth-first scheduling of project references in tsc -b leads to builder idle time and slower parallel builds.*

 * created by **christianvuerings**
 * (later) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Backlog`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#64227](https://github.com/microsoft/TypeScript/issues/64227) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**The \`options\` arg of \`Temporal\.ZonedDateTime\.prototype\.toLocaleString\(\)\` currently accepts "illegal" option \`timeZone\`**

*TypeScript’s lib.esnext.temporal.d.ts incorrectly allows a timeZone option for Temporal.ZonedDateTime.prototype.toLocaleString despite the specification forbidding it.*

 * created by **Sector6759**
 * (later) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64228](https://github.com/microsoft/TypeScript/issues/64228) (Open, `Needs More Info`)

**Incorrect TS1111 when using private generator function in JS**

*VSCode erroneously raises TS1111 error when invoking a private generator method on another instance within a class.*

 * created by **Ecco**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5622172507) **nmain** said "Could you make sure your example is complete?  When I copy your code to a playground I get a few TS2339 but no TS1111."
 * **RyanCavanaugh** added label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/64228#issuecomment-5666596178) **RyanCavanaugh** said "Same, please fill in the definitions of child and its #iterate"

### [Issue microsoft/TypeScript#64229](https://github.com/microsoft/TypeScript/issues/64229) (Closed, `Design Limitation`)

**nullish types not narrowed in if block**

*Optional chaining and nullish coalescing conditions do not narrow nullish types within if blocks in TypeScript.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5621832263) **snarbles2** provided a simplified conditional using optional chaining and noted that a comparison operator made the expression too complex for the control flow analysis
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5636684265) **errorx666** updated code per suggestion but preferred original approach and requested further feedback
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5636716584) **errorx666** asked whether the issue was related to using optional chaining in a comparison, noting that nullish values can't be greater than zero so it behaves as intended
 * **RyanCavanaugh** added label `Design Limitation`
 * [later](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5666272111) **RyanCavanaugh** observed no generalizable pattern and illustrated with an alternative example

### [Issue microsoft/TypeScript#64231](https://github.com/microsoft/TypeScript/issues/64231) (Open, `Bug`)

**Parser misinterprets async\(\) calls in conditional expressions as async arrow functions**

*TypeScript parser misinterprets calls to a function named async in ternary expressions as async arrow functions, causing syntax errors.*

 * created by **camc314**
 * (2 days ago) **DanielRosenwasser** added label `Bug`, and set milestone to `TypeScript 7.1.0 Beta`
 * [later](https://github.com/microsoft/TypeScript/issues/64231#issuecomment-5662369126) **anbv29** asked if they could work on the issue

### [Issue microsoft/TypeScript#64240](https://github.com/microsoft/TypeScript/issues/64240) (Closed, `Bug`, **andrewbranch**)

**API panics when serializing number literal types with \`\+Infinity\` and \`\-Infinity\`**

*TypeScript’s unstable sync API panics when serializing number literal types representing +Infinity or -Infinity.*

 * created by **auvred**
 * [later](https://github.com/microsoft/TypeScript/issues/64240#issuecomment-5666202157) **RyanCavanaugh** said "Seems like we'd have the same issue if a type resolved to NaN, but AFAIK that isn't possible - anyone want to try?"
 * (later) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64241](https://github.com/microsoft/TypeScript/pull/64241) (Closed, `For Milestone Bug`, **andrewbranch**)

**Properly serialize \`\+Infinity\`, \`\-Infinity\`, and \`NaN\` number literal type values in API**

*Implement correct serialization of +Infinity, -Infinity, and NaN number literals in the API.*

 * created by **auvred**
 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (later) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64242](https://github.com/microsoft/TypeScript/issues/64242) (Closed, `Needs Investigation`, **andrewbranch**)

**Sporadic \`context canceled\` in \`stderr\` when running TypeScript API in subprocess tests**

*Intermittent 'context canceled' output appears in stderr instead of empty when testing a CLI using TypeScript's API on Ubuntu CI.*

 * created by **mrazauskas**
 * (later) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64244](https://github.com/microsoft/TypeScript/issues/64244) (Closed, `Working as Intended`)

**The isFinite\(\) type declaration doesn't specify the right type**

*The TypeScript declaration for global isFinite incorrectly specifies its parameter as number instead of any.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5640766744) **RyanCavanaugh** noted that the library typing was intentional and cited MDN's warning against using isFinite due to coercion
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5645885126) **SetTrend** suggested considering MDN documentation users in the JsDoc docs for isFinite instead of expecting them to refer to the wiki
 * [today](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5652715247) **MartinJohns** said "See his StackOverflow response: https://stackoverflow.com/a/41750391"
 * [later](https://github.com/microsoft/TypeScript/issues/64244#issuecomment-5666002285) **RyanCavanaugh** explained that TypeScript’s type system prevents type coercion, disallowing operations like "8" * 3
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64246](https://github.com/microsoft/TypeScript/pull/64246) (Closed, `For Milestone Bug`, **andrewbranch**)

**fix\(syncChannel\): give child process time to exit before kill in close\(\)**

*Modify the syncChannel close() method to wait briefly for child processes to exit gracefully before force-killing them.*

 * created by **biisal**
 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (later) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64253](https://github.com/microsoft/TypeScript/issues/64253) (Open, `Suggestion`)

**Anonymous Symbol Properties**

*Allow inline declaration of unique symbol keys on object types to define anonymous single-use phantom properties without separate declarations*

 * created by **RonaldBunk**
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#64256](https://github.com/microsoft/TypeScript/pull/64256) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 5 updates**

*Upgrade five GitHub Actions packages: azure/login to 3.1.0, download-artifact to 8.0.1, and CodeQL actions to 4.38.0.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64257](https://github.com/microsoft/TypeScript/pull/64257) (Open, `For Backlog Bug`)

**Fix non\-null discriminant narrowing consistency**

*Ensure discriminant narrowing consistently preserves nullable constituents for both small and large unions under strictNullChecks.*

 * created by **z0rimo**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5657958944) **z0rimo** agreed with microsoft-github-policy-service
 * [later](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5662956364) **z0rimo** addressed both #62511 and #64260 by reworking mutation analysis around invocation sites and adding tests for union-size inconsistency and stale-fact cases

### [PR microsoft/TypeScript#64258](https://github.com/microsoft/TypeScript/pull/64258) (Closed, `For Uncommitted Bug`)

**Fix spelling of occurred in cross\-project panic handling**

*Renames incorrectly spelled panicsOccured and panicOccured identifiers to panicsOccurred and panicOccurred in crossproject.go.*

 * created by **tanvir-ux**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64258#issuecomment-5660152614) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64258#issuecomment-5660166165) **tanvir-ux** said "Linked issue: #64259."

### [Issue microsoft/TypeScript#64259](https://github.com/microsoft/TypeScript/issues/64259) (Closed)

**Misspelling: panicsOccured / panicOccured in crossproject\.go**

*Correct misspelled identifiers panicsOccured and panicOccured to panicsOccurred and panicOccurred in tsc/internal/ls/crossproject.go*

 * created by **tanvir-ux**

### [Issue microsoft/TypeScript#64260](https://github.com/microsoft/TypeScript/issues/64260) (Closed, `Needs More Info`)

**Non\-null discriminant narrowing can use a stale fact after a later assignment**

*Discriminant narrowing with non-null assertions can incorrectly rely on stale facts when assignments occur in comparison or switch expressions, causing missing undefined errors.*

 * created by **z0rimo**

### [Issue microsoft/TypeScript#64261](https://github.com/microsoft/TypeScript/issues/64261) (Closed, `Unactionable`)

**Windows 11, Node v26\.8\.2, typescript@7\.0\.2 \(@typescript/native global\), ts7\-eslint@0\.2\.0, ESLint 10\.x\.**

*A writeAllBuf race condition causes intermittent EPIPE broken pipe errors in @typescript-eslint on Windows.*

 * created by **Artyomkun**
 * **RyanCavanaugh** added label `Unactionable`
 * (later) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/64261#issuecomment-5666663441) **Artyomkun** noted that the error lay in the experimental dependencies for version 7, encountered a rare edge case, and advised caution when upgrading to 7.1

