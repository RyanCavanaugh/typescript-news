# Report for 2026-07-05 (Sunday, July 5th, 2026)

8 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @guest271314 provided correction about nullability in the specification in [microsoft/TypeScript#62224](https://github.com/microsoft/TypeScript/issues/62224#issuecomment-4892501637)

## Activity Summary

### [Issue microsoft/TypeScript#62224](https://github.com/microsoft/TypeScript/issues/62224) (Open, `Suggestion`, `Awaiting More Feedback`)

**\`controller\.byobRequest\` type incorrectly says value is possibly null while \`autoAllocateChunkSize\` is present\.**

*TypeScript mistakenly treats controller.byobRequest as possibly null when autoAllocateChunkSize is specified on a ReadableStream.*

 * (45 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [45 weeks ago](https://github.com/microsoft/TypeScript/issues/62224#issuecomment-3213000720) **BlackAsLight** said "It would just be a nice typing to have and I don't really see any reason somebody wouldn't want to use the property when making a byob stream."
 * [later](https://github.com/microsoft/TypeScript/issues/62224#issuecomment-4892501637) **guest271314** noted that the property could still be null even with autoAllocateChunkSize set

### [PR microsoft/TypeScript#63596](https://github.com/microsoft/TypeScript/pull/63596) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump actions/cache from 5\.0\.5 to 6\.1\.0 in the github\-actions group**

*Upgrade actions/cache in the GitHub Actions group from v5.0.5 to v6.1.0 to add read-only cache access support.*

 * (1 week ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63596#issuecomment-4888254828) **dependabot[bot]** said "Looks like actions/cache is updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63597](https://github.com/microsoft/TypeScript/issues/63597) (Open, `Suggestion`, `Awaiting More Feedback`)

**add an option to report an error when \`Symbol\.dispose\`/\`Symbol\.asyncDispose\` objects are used without the \`using\` keyword**

*Add a TypeScript compiler option to error when objects with Symbol.dispose or Symbol.asyncDispose are used without the using keyword.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63597#issuecomment-4832681103) **DetachHead** questioned whether objects with Symbol.dispose should require using and suggested documentation mention this behavior
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63597#issuecomment-4833162597) **MartinJohns** explained that implementing Symbol.dispose indicates intent to provide explicit resource release and compared it to C#'s IDisposable, then asked how to prevent errors when not using a using statement intentionally
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63597#issuecomment-4838772087) **Renegade334** referred to typescript-eslint/typescript-eslint#8255 to agree that it’s a linter job
 * (later) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63598](https://github.com/microsoft/TypeScript/issues/63598) (Open, `Bug`, `Domain: Formatter`, `Fix Available`, **gabritto**)

**"Token end is child end" when '= ${id}id' is used in a property annotation**

*Formatting a property annotation using a malformed template literal triggers a 'Token end is child end' debug failure in TypeScript.*

 * created by **DanielRosenwasser**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63598#issuecomment-4846219140) **DanielRosenwasser** shared a Copilot suggestion patch and said he would revisit it post 7.0
 * (later) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **gabritto**
 * **typescript-automation[bot]** added label `Fix Available`

### [Issue microsoft/TypeScript#63601](https://github.com/microsoft/TypeScript/issues/63601) (Closed, `Needs Investigation`, **jakebailey**)

**@typescript/typescript6 does not have all versions that regular v6 branch has**

*The @typescript/typescript6 npm package lags behind the regular typescript v6 branch, missing versions like 6.0.3.*

 * created by **ZuBB**
 * (later) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**
 * [later](https://github.com/microsoft/TypeScript/issues/63601#issuecomment-4894812442) **jakebailey** said "Why? The version you place there will have no impact on what version of TS your package manager selects to be reexported."

### [Issue microsoft/TypeScript#63605](https://github.com/microsoft/TypeScript/issues/63605) (Closed)

**Is developing interpreter on top of Node\.js good?**

*Developing an interpreter on Node.js enables rapid prototyping and cross-platform deployment but sacrifices performance and memory efficiency versus native implementations.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63605#issuecomment-4869918188) **dominexmacedon-docs** denied being AI spam and suggested learning the Node.js-based language for its critical features
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63605#issuecomment-4869947662) **MartinJohns** called the issue spam, said it was AI generated and unrelated to the repository
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63605#issuecomment-4870009171) **dominexmacedon-docs** acknowledged the content was AI-generated spam, explained they used Copilot to generate markdown, and clarified that the language is real and built on Node.js
 * (later) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63605#issuecomment-4894749621) **RyanCavanaugh** said "Issues are not for advertising your project."

### [Issue microsoft/TypeScript#63607](https://github.com/microsoft/TypeScript/issues/63607) (Closed)

**Why can't we build a VM on the top of Node\.js? Is it because of not being Native?**

*Building a VM on Node.js supports basic features but fails to handle advanced capabilities like object iteration and control flow, so most implementations use C.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63607#issuecomment-4872986822) **MartinJohns** said "This issue tracker is meant for bug reports and feature requests regarding TypeScript. It's not suited for your ChatGPT questions."
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63607#issuecomment-4873016141) **dominexmacedon-docs** replied defensively accusing the commenter of jealousy
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63607#issuecomment-4873037523) **dominexmacedon-docs** insulted the maintainer and asserted their right to post ChatGPT questions
 * [later](https://github.com/microsoft/TypeScript/issues/63607#issuecomment-4894761556) **RyanCavanaugh** said "User was blocked for this."
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63610](https://github.com/microsoft/TypeScript/pull/63610) (Closed, `For Uncommitted Bug`)

**feat\(checker\): add Object\.hasOwn\(\) type narrowing**

*Support type narrowing of object properties in Object.hasOwn() calls by leveraging existing in-operator logic.*

 * [today](https://github.com/microsoft/TypeScript/pull/63610#issuecomment-4885475416) **daishuge** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63610#issuecomment-4885496751) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #44253. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/63610#issuecomment-4885496820) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #44253. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/63610#issuecomment-4887234053) **MartinJohns** said "@daishuge You should read this: https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md"
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63611](https://github.com/microsoft/TypeScript/pull/63611) (Closed, `For Uncommitted Bug`)

**Update codecov\.yml**

*Update the codecov.yml configuration file to implement changes required by TZAHAL 1165.*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63611#issuecomment-4887064701) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63611#issuecomment-4887064702) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63612](https://github.com/microsoft/TypeScript/pull/63612) (Closed, `For Uncommitted Bug`)

**gh pr checkout 63612 \- Atualização **

*Use gh pr checkout 63612 to update the TZAHAL component to version 165.*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63612#issuecomment-4887096971) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63613](https://github.com/microsoft/TypeScript/pull/63613) (Closed, `For Uncommitted Bug`)

**gh pr checkout 63613 \- Revert "Fix infinite loop"**

*Reverts the infinite loop fix introduced in Pull Request #63581 for the TypeScript repository.*

 * created by **liu-idf18**
 * [today](https://github.com/microsoft/TypeScript/pull/63613#issuecomment-4887174326) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63613#issuecomment-4887174329) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63614](https://github.com/microsoft/TypeScript/pull/63614) (Closed, `For Uncommitted Bug`)

**gh pr checkout 63614 \- Atualização **

*Use GitHub CLI to check out and update pull request 63614 for the TZAHAL/FOIA repository.*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63614#issuecomment-4887529635) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63614#issuecomment-4887529656) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **liu-idf18** closed the issue

### [PR microsoft/TypeScript#63615](https://github.com/microsoft/TypeScript/pull/63615) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 5 updates**

*Updates actions/cache from 5.0.5 to 6.1.0 and all CodeQL GitHub Action steps from 4.36.2 to 4.36.3 in the root directory.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63616](https://github.com/microsoft/TypeScript/issues/63616) (Open, `Bug`, `Domain: This-Typing`)

**Inconsistent \`typeof this\` when the \`this\` parameter declared in the signature of a function parameter**

*Declaring a this parameter for callback functions leads to inconsistent inferred types for typeof this depending on whether this is used in the function body.*

 * created by **mpal9000**

### [PR microsoft/TypeScript#63617](https://github.com/microsoft/TypeScript/pull/63617) (Closed, `For Uncommitted Bug`)

**Revert "Fix infinite loop"**

*Revert the infinite loop fix introduced in microsoft/TypeScript#63581.*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63617#issuecomment-4889181542) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63618](https://github.com/microsoft/TypeScript/pull/63618) (Closed, `For Uncommitted Bug`)

**gh pr checkout 63618 \- **

*Support checking out pull request 63618 (TZAHAL 1165) via the gh pr checkout command.*

 * created by **liu-idf18**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63618#issuecomment-4893510792) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63618#issuecomment-4893510900) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **liu-idf18** closed the issue

