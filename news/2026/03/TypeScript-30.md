# Report for 2026-03-30 (Monday, March 30th, 2026)

11 different users commented on 8 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#60591](https://github.com/microsoft/TypeScript/issues/60591) (Closed, `Bug`, `Help Wanted`, `Domain: Declaration Emit`)

**JSDoc implements with imported types**

*JSDoc @implements of an imported type in JS causes a private name error during declaration emit, unlike TypeScript files.*

 * (1.3 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/60591#issuecomment-4158335455) **apendua** said "FYI, it looks like this issue is now resolved in typescript-go."

### [Issue microsoft/TypeScript#63309](https://github.com/microsoft/TypeScript/issues/63309) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Regression in 6\.0: type inferred from const with broader type is too narrow**

*TypeScript 6.0 mistakenly narrows a class property initialized from a union-typed constant to a single literal value.*

 * (3 days ago) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63310](https://github.com/microsoft/TypeScript/pull/63310) (Closed, **RyanCavanaugh**, **Copilot**)

**Mark class property initializers as outside of CFA containers**

*Restore PropertyDeclaration as a control flow container to isolate class property initializer type inference and prevent module-level narrowing leaks*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148456905) **typescript-bot** reported successful test results from running the top 400 repos with tsc comparing main and PR merge
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148850455) **typescript-bot** posted performance run results as requested
 * **RyanCavanaugh** added to milestone `TypeScript 6.0.2`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63323](https://github.com/microsoft/TypeScript/issues/63323) (Closed, `Suggestion`, `Out of Scope`)

**Support pipe \`\|\>\` operator**

*Support the TC39 pipeline operator |> in TypeScript to simplify nested function calls.*

 * created by **reesericci**
 * [today](https://github.com/microsoft/TypeScript/issues/63323#issuecomment-4156951747) **olivermrose** noted that the issue duplicates #17718 and stated that TypeScript only implements Stage 3 proposals and is not accepting feature requests
 * [today](https://github.com/microsoft/TypeScript/issues/63323#issuecomment-4157002617) **MartinJohns** refuted the claim that TypeScript isn't accepting feature requests currently
 * [today](https://github.com/microsoft/TypeScript/issues/63323#issuecomment-4157112790) **olivermrose** quoted that feature additions and behavioral changes were paused until TypeScript 7.0 was completed and linked the TypeScript contribution guide
 * [today](https://github.com/microsoft/TypeScript/issues/63323#issuecomment-4157182185) **MartinJohns** clarified that no new features would be added until version 7.0 was complete but suggestions remained welcome, though unlikely to be implemented immediately
 * [today](https://github.com/microsoft/TypeScript/issues/63323#issuecomment-4157249685) **snarbles2** said "Pipeline proposal is very far from stage 3, and probably as good as dead (for rather silly reasons, but all the same)."
 * [today](https://github.com/microsoft/TypeScript/issues/63323#issuecomment-4157360016) **reesericci** clarified that the referenced issue was closed and proposed adding it under a feature flag as a discrete 'lib' option
 * [today](https://github.com/microsoft/TypeScript/issues/63323#issuecomment-4157425594) **MartinJohns** rejected the proposal to add the closed issue under a feature flag as a library option
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Out of Scope`
 * [today](https://github.com/microsoft/TypeScript/issues/63323#issuecomment-4157547337) **RyanCavanaugh** clarified that the item was on the checklist because it was mandatory
 * (today) **RyanCavanaugh** closed the issue
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63324](https://github.com/microsoft/TypeScript/pull/63324) (Closed)

**docs: fix typos in Herebyfile\.mjs and eslint rule comment**

*Fixes typos in Herebyfile.mjs and an ESLint rule comment by correcting ‘miscelaneous’ to ‘miscellaneous’ and ‘arugments’ to ‘arguments’.*

 * created by **ayushshukla1807**
 * [today](https://github.com/microsoft/TypeScript/pull/63324#issuecomment-4156984969) **jakebailey** stated that the repository is closed except for critical bugfixes and provided links to the contribution guidelines
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63324#issuecomment-4157697551) **MartinJohns** quoted the pull request template warning against sending typo-fix-only PRs
 * [today](https://github.com/microsoft/TypeScript/pull/63324#issuecomment-4158897299) **ayushshukla1807** acknowledged the instruction to avoid typo-only PRs and apologized

### [Issue microsoft/TypeScript#63325](https://github.com/microsoft/TypeScript/issues/63325) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**\`lib\.dom\.d\.ts\`: Keyframe interface should allow CSS Typed Object Model objects like CSSTransformValue, etc**

*The Keyframe interface in lib.dom.d.ts should accept CSS Typed Object Model types such as CSSTransformValue.*

 * created by **zardalt**

### [PR microsoft/TypeScript#63326](https://github.com/microsoft/TypeScript/pull/63326) (Closed)

**docs: fix typos in documentation**

*Corrected typos throughout the project's markdown documentation using codespell.*

 * created by **AkkiKrsingh2005**
 * [today](https://github.com/microsoft/TypeScript/pull/63326#issuecomment-4157887734) **typescript-bot** thanked the author for the PR, cautioned to preserve TSServer API compatibility, and pinged reviewers for extra review
 * [today](https://github.com/microsoft/TypeScript/pull/63326#issuecomment-4157887821) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63326#issuecomment-4157944278) **jakebailey** stated that the repository is closed except for critical bugfixes and provided links to the contribution guidelines
 * (today) **jakebailey** closed the issue

