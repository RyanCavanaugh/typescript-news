# Report for 2026-04-16 (Thursday, April 16th, 2026)

9 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @GageSorrell asked if the type-directed emit performance issue remains in version 7 in [microsoft/TypeScript#62584](https://github.com/microsoft/TypeScript/issues/62584#issuecomment-4264758521)

## Activity Summary

### [Issue microsoft/TypeScript#32392](https://github.com/microsoft/TypeScript/issues/32392) (Open, `Suggestion`, `Awaiting More Feedback`)

**Preserve comments with object destructuring assignment**

*Preserve and display JSDoc comments for properties when using object destructuring assignments in TypeScript*

 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-1211297650) **ab-pm** requested a way to document destructured variables so JsDoc comments appear in IntelliSense hovers
 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-1640633376) **yolilufei** said "is there any progress, please?"
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-2211007664) **nathanchase** expressed frustration about missing IntelliSense on destructured composable properties
 * [today](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-4263114003) **zoltanium** noted the issue had lingered for seven years, speculated about it gaining traction, and volunteered to investigate specific code segments

### [Issue microsoft/TypeScript#62584](https://github.com/microsoft/TypeScript/issues/62584) (Closed, `Discussion`)

**Experimental TypeScript fork with operator overloading and overload dispatch—documenting a working implementation**

*Documenting a proof-of-concept TypeScript fork enabling operator overloading and type-based function overload dispatch.*

 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/62584#issuecomment-3397762840) **snarbles2** described the proposal as an exploratory implementation rather than a feature request, lamented TypeScript’s limited scope and expressed a desire for more innovation, acknowledged upstream inclusion was unlikely but welcomed discussion, and suggested consulting the withdrawn TC39 operator overloading proposal
 * **RyanCavanaugh** added label `Discussion`
 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/62584#issuecomment-3398424206) **RyanCavanaugh** clarified that type-directed emit is not a good idea despite its feasibility, citing slow emit, broken single-file transpile, non-working generics, runtime surprises, as-any failures, and TC39 alignment issues
 * [today](https://github.com/microsoft/TypeScript/issues/62584#issuecomment-4264758521) **GageSorrell** asked if the type-directed emit performance issue remained in version 7, questioned whether the generics limitation warranted avoiding operator overloading, and wondered if the native TS release brought operator overloading closer to feasibility
 * [today](https://github.com/microsoft/TypeScript/issues/62584#issuecomment-4264811910) **jakebailey** said "No, type-directed emit continues to be a non-goal. Note the date on that comment, long after we announced the port."

### [Issue microsoft/TypeScript#63346](https://github.com/microsoft/TypeScript/issues/63346) (Closed, `Question`)

**Experimental \(deprecated\) decorators are included by default**

*The ESNext library includes legacy experimental decorator types by default, causing conflicts with new decorator definitions.*

 * (1 week ago) **typescript-bot** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4257328096) **OldStarchy** clarified that '*.d.ts' files are included globally without imports and that adding an export does not address the default inclusion of legacy decorators, and pointed out the specific type name conflict
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4257346566) **OldStarchy** identified issue 29828 as the closest match and suggested removing types instead of fixing, noting that replacing legacy decorator types could invert the problem for projects relying on the legacy syntax
 * [today](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4261818948) **RyanCavanaugh** explained that a global type-name invariant doesn't exist and recommended exporting types in modules to avoid conflicts

### [Issue microsoft/TypeScript#63373](https://github.com/microsoft/TypeScript/issues/63373) (Closed, `External`)

**tsserver hangs in Yarn PnP projects — incorrect directory watcher due to unchecked indexOf returning \-1**

*tsserver in Yarn PnP projects hangs because unchecked indexOf on non-node_modules paths produces incorrect directory watcher paths.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63373#issuecomment-4208290436) **RyanCavanaugh** provided an auto-generated analysis listing similar issues to help get started
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63373#issuecomment-4217077271) **jakebailey** said "This is out of our control; this is a patch and we do not maintain it."
 * **RyanCavanaugh** added label `External`
 * [today](https://github.com/microsoft/TypeScript/issues/63373#issuecomment-4264683509) **typescript-bot** said "This issue has been marked as "External" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63385](https://github.com/microsoft/TypeScript/issues/63385) (Closed, `Design Limitation`)

**\`null\`/\`undefined\` guards sometimes adds \`& \({} \| undefined\`/\`& \({} \| null\` \(out of nowhere\) to the tested variable\.**

*Null guards in generic functions introduce an unintended intersection with {} | null or undefined into the variable's type.*

 * (2 days ago) **RyanCavanaugh** added label `Design Limitation`, and removed label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4246755155) **RyanCavanaugh** said "I don't really see a way to fix this without breaking other CFA scenarios at the moment."
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4264683687) **typescript-bot** said "This issue has been marked as "Design Limitation" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63391](https://github.com/microsoft/TypeScript/issues/63391) (Open, `Bug`, `Domain: JS Emit`, `Fix Available`)

**The module namespace object returned by \_\_importStar is not the same when import the same module multiple times**

*TypeScript’s compiled CommonJS __importStar helper creates separate namespace objects for repeated imports of the same module.*

 * **RyanCavanaugh** added to milestone `Dormant`
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: JS Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/63391#issuecomment-4262359520) **nmain** suggested providing a singular globalThis.__importStar in the environment with the required semantics and storage for reusable module objects

### [Issue microsoft/TypeScript#63398](https://github.com/microsoft/TypeScript/issues/63398) (Closed, `Unactionable`)

**Two ExpressionStatements allowed on one line with no semicolon\!**

*TypeScript incorrectly accepts two expression statements on a single line without a semicolon instead of throwing a parse error.*

 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4260319722) **conartist6** argued that TypeScript treats all character sequences as valid programs and relies on ESLint and Prettier to catch syntax errors, otherwise it would legalize any syntax
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4260408230) **snarbles2** pointed out that TypeScript is producing syntax errors for the invalid class syntax and asked what the user would expect to happen differently
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4260722010) **mkantor** suggested using the noEmitOnError option and clarified that the discussion pertained to code emission rather than error reporting
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4262036080) **conartist6** explained their computational linguist perspective and argued that the sanitized syntax formed a new programming language rather than a communication failure
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4262258094) **RyanCavanaugh** said "Again, it seems like you're looking for noEmitOnError"
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4262298293) **mkantor** stated that a language implementation’s diagnostics should be treated as errors, provided a Bash syntax example, and offered to continue the discussion privately on Discord

### [Issue microsoft/TypeScript#63399](https://github.com/microsoft/TypeScript/issues/63399) (Closed, `Duplicate`)

**Make object type indexable**

*Enable expressions like obj !== null && typeof obj === 'object' to narrow unknown to an indexable Record<string, unknown>.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63399#issuecomment-4240396586) **MartinJohns** said "Essentially you want #38801."
 * **RyanCavanaugh** added label `Duplicate`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63399#issuecomment-4244967183) **RyanCavanaugh** said "This is obviously fine on the read side but it's pretty dangerous if you have a write inside the if, since Record is basically any in terms of obj.prop = value"
 * [today](https://github.com/microsoft/TypeScript/issues/63399#issuecomment-4264683391) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63409](https://github.com/microsoft/TypeScript/issues/63409) (Closed, `Duplicate`)

**Abstarct members of abstarct mixin is allowed to call**

*Calling an abstract method on a class returned by an abstract mixin does not trigger a compiler error.*

 * [today](https://github.com/microsoft/TypeScript/issues/63409#issuecomment-4259894246) **snarbles2** clarified that the error should be on `const u = new UL;` and that `u.log()` should succeed because abstract classes cannot be instantiated
 * [today](https://github.com/microsoft/TypeScript/issues/63409#issuecomment-4260085807) **MartinJohns** said "Essentially a duplicate of #32122. Mixins and abstract classes don't mix well."
 * **RyanCavanaugh** added label `Duplicate`
 * (today) **olegdunkan** closed the issue

### [PR microsoft/TypeScript#63410](https://github.com/microsoft/TypeScript/pull/63410) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Speculative fix for array compat issue \(ignore\)**

*Proposed speculative fix for array compatibility issue seeking confirmation of its correctness.*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/63410#issuecomment-4263038687) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63410#issuecomment-4263039181) **typescript-bot** reported CI job statuses and provided status and result links for each command
 * [today](https://github.com/microsoft/TypeScript/pull/63410#issuecomment-4263130323) **typescript-bot** said "@RyanCavanaugh, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/63410#issuecomment-4263176114) **typescript-bot** reported the DT tests results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63410#issuecomment-4263482689) **typescript-bot** reported tsc comparison results for top 400 repos between main and the pull request merge, highlighting type errors in amruthpillai/reactive-resume
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63411](https://github.com/microsoft/TypeScript/issues/63411) (Closed)

**\+93792401535**

*The issue is titled with a phone number and links to TypeScript’s es2015.symbol.wellknown.d.ts without context*

 * created by **jalalijawid47-dot**
 * (later) **RyanCavanaugh** closed the issue

