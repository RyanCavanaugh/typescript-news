# Report for 2026-05-15 (Friday, May 15th, 2026)

8 different users commented on 11 different issues.

## Recommended Actions

 * Response Recommended
    * @FlippingBinary provided a workaround for suppressing error 80002 in [microsoft/TypeScript#43812](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-4467331105)
    * @puneetdixit200 asked to be assigned the issue in [microsoft/TypeScript#63463](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4466304630)

## Activity Summary

### [Issue microsoft/TypeScript#43812](https://github.com/microsoft/TypeScript/issues/43812) (Open, `Suggestion`, `Awaiting More Feedback`)

**Unable to mark JS functions as not being constructors \(TS80002\)**

*Enable marking JS functions as non-constructors with JSDoc to avoid TS80002 misclassification and broken syntax coloring.*

 * [4 years ago](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-1119003904) **boneskull** reported encountering the same behavior and provided a code workaround; suggested the @this tag may be ignored
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-1849024577) **nightwing** reported that functions were still shown as classes in hover tooltips despite using @type and suggested disabling the class detection heuristic when @this or @type was set
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-3800868415) **supernovus** complained that existing suggestions for suppressing TS80002 warnings no longer worked in VSCode/Codium and asked why there was still no directive to ignore specific warnings
 * [later](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-4467331105) **FlippingBinary** provided a workaround for suppressing error 80002 by casting this with parentheses and suggested using e.currentTarget

### [PR microsoft/TypeScript#62768](https://github.com/microsoft/TypeScript/pull/62768) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Don't create substition types when extending type with infer type parameters**

*Prevent creation of substitution types when extending TypeScript types with inferred type parameters.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (25 weeks ago) **Andarist** closed the issue
 * **typescript-bot** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#63430](https://github.com/microsoft/TypeScript/issues/63430) (Open, `Needs Investigation`, `Fix Available`, **andrewbranch**)

**Paths from tsconfig are not used if declaration is on a different partition**

*TypeScript ignores tsconfig path mappings for imports on a different drive when emitting declaration files, producing absolute paths.*

 * created by **dragomirtitian**
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63430#issuecomment-4314787953) **RyanCavanaugh** provided an automated list of similar issues to the report
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Backlog`, and assigned to **andrewbranch**
 * **typescript-bot** added label `Fix Available`

### [Issue microsoft/TypeScript#63463](https://github.com/microsoft/TypeScript/issues/63463) (Open, `Bug`, `Domain: LS: Completion Lists`)

**\`default\` keyword is offered in expression\-bodied arrow function completions**

*TypeScript’s completion engine incorrectly suggests ‘default’ in expression-bodied arrow function contexts despite it being invalid.*

 * (2 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Completion Lists`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4466304630) **puneetdixit200** requested assignment to add a fourslash completion test for expression-bodied arrow functions, investigate default keyword inclusion, and refine completion list logic

### [Issue microsoft/TypeScript#63465](https://github.com/microsoft/TypeScript/issues/63465) (Closed, `Won't Fix`)

**Implement interface codefix is offered when the implemented interface type is invalid**

*Implement interface codefix is offered even when the implemented interface has invalid type arguments or unresolved symbols.*

 * created by **danyalahmed1995**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63465#issuecomment-4422368179) **RyanCavanaugh** provided an auto-generated comment listing similar issues and guidance on duplicates
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63465#issuecomment-4422977599) **danyalahmed1995** thanked RyanCavanaugh for the similarity check and explained why linked issues #36577 and #14105 were related but did not match the current report
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/63465#issuecomment-4461413095) **RyanCavanaugh** said "I don't see the point of trying to "fix" this when there's no right answer to begin with."
 * [today](https://github.com/microsoft/TypeScript/issues/63465#issuecomment-4461907364) **danyalahmed1995** said "Understandable I see your point of having no clear answer for the "fix" You already answered this on PR#63466 that this doesn't meet the bar for 6.0 patch.Feel free to close it."

### [Issue microsoft/TypeScript#63470](https://github.com/microsoft/TypeScript/issues/63470) (Closed, `Won't Fix`)

**Defined prototype properties resolve to potentially undefined type when assigned to from class method \(when using JavaScript ES5 syntax\)**

*TypeScript incorrectly infers the type of a prototype property defined with a conditional setter as number|undefined instead of the underlying number.*

 * created by **Iemand005**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63470#issuecomment-4432297503) **RyanCavanaugh** provided an auto-generated list of similar issues and guidance on potential duplicates
 * [today](https://github.com/microsoft/TypeScript/issues/63470#issuecomment-4461337843) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar and TS 7.0 will not support prototype-based classes."
 * **RyanCavanaugh** added label `Won't Fix`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63480](https://github.com/microsoft/TypeScript/issues/63480) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**\`Set\#size\` has grammar typo in \`lib\.es2015\.collection\.d\.ts\`**

*Fix grammar typo in Set#size documentation and standardize @returns capitalization in lib.es2015.collection.d.ts*

 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: lib.d.ts`

### [PR microsoft/TypeScript#63482](https://github.com/microsoft/TypeScript/pull/63482) (Closed, `For Backlog Bug`)

**Fix Set size doc comment grammar**

*Correct the Set#size doc comment by changing “in Set” to “in the Set.”*

 * created by **popsiclelmlm**
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#63483](https://github.com/microsoft/TypeScript/pull/63483) (Open, `For Backlog Bug`)

**docs: add JSDoc comments to ReadonlySet interface**

*Add JSDoc comments to the ReadonlySet interface to improve its documentation.*

 * created by **niledas**
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#63484](https://github.com/microsoft/TypeScript/pull/63484) (Closed, `For Uncommitted Bug`)

**gh pr checkout 63484 \- Remove release branch triggers from CI workflow**

*Remove release branch triggers from the continuous integration workflow configuration*

 * created by **ghost**
 * (later) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63484#issuecomment-4466949016) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63484#issuecomment-4466949018) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

