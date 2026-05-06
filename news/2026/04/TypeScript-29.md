# Report for 2026-04-29 (Wednesday, April 29th, 2026)

9 different users commented on 18 different issues.

## Recommended Actions

 * Response Recommended
    * @MulverineX asked why the PR was not proceeding after the file removal in [microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4346296546)
    * @afurm provided CLA agreement commands as requested in [microsoft/TypeScript#63449](https://github.com/microsoft/TypeScript/pull/63449#issuecomment-4346688853)
    * @carljohnsonnewhampshire-hue provided example code reproducing the issue in [microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4353396688)

## Activity Summary

### [Issue microsoft/TypeScript#36336](https://github.com/microsoft/TypeScript/issues/36336) (Closed, `Suggestion`, `Out of Scope`)

**Syntactic sugar for Algebraic Data Types**

*Extend TypeScript enum syntax to define algebraic data types with associated values that compile to discriminated unions and constructors.*

 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/36336#issuecomment-583131894) **RyanCavanaugh** mentioned avoiding runtime-affecting constructs and shared a possible runtime-free discriminated union syntax
 * (6.2 years ago) **RyanCavanaugh** closed the issue
 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/36336#issuecomment-583179583) **jcalz** provided an example TypeScript DiscriminatedUnion type definition with implementation and Playground link
 * [today](https://github.com/microsoft/TypeScript/issues/36336#issuecomment-4349659282) **ozyman42** pointed out that TypeScript and Rust enums support nominal typing which DiscriminatedUnion lacks and expressed desire for ADT enums with nominal types

### [PR microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248) (Open, `For Backlog Bug`)

**Add lib types for JSON\.rawJSON, JSON\.isRawJSON, and reviver context**

*Add TypeScript declarations for ES2025’s JSON.rawJSON, JSON.isRawJSON, and JSON.parse reviver context*

 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`
 * **typescript-bot** added label `For Backlog Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4270116628) **RyanCavanaugh** said "@afurm future automated comments will result in a block; any automated activity we want to occur in this repo we will set up ourselves or already have"
 * [today](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4346296546) **MulverineX** said "@RyanCavanaugh the commandLineParser.ts has since been removed, is there a reason this PR is not proceeding?"

### [PR microsoft/TypeScript#63386](https://github.com/microsoft/TypeScript/pull/63386) (Closed)

**Document charAt edge case behavior**

*Document that String.charAt returns an empty string for indexes outside the valid range to ensure consistency.*

 * created by **bwalter007**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63386#issuecomment-4229758174) **afurm** acknowledged the clarification and asked whether charCodeAt, codePointAt, and substring out-of-bounds behaviors are documented and if documentation updates are needed
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63386#issuecomment-4245703846) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180847265"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63386#issuecomment-4345725075) **RyanCavanaugh** said "Closing due to inactivity. New PRs (ideally passing CI 😅) welcomed."

### [Issue microsoft/TypeScript#63445](https://github.com/microsoft/TypeScript/issues/63445) (Closed, `Duplicate`)

**TS server crashes with \`@mui/icons\-material\` v9 package**

*@mui/icons-material v9 causes the TypeScript server to crash repeatedly during tsconfig.app.json initialization in VS Code.*

 * created by **mliebold-jax**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63445#issuecomment-4328357252) **RyanCavanaugh** said "See https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4254729016"
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63445#issuecomment-4348991031) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63449](https://github.com/microsoft/TypeScript/pull/63449) (Closed, `For Backlog Bug`)

**Fix Intl\.Collator compare declaration**

*Revise Intl.Collator.compare declaration to a readonly void-this function and add compiler tests*

 * created by **afurm**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63449#issuecomment-4346677465) **jakebailey** said "I don't think we need a second PR for this: #62052"
 * [today](https://github.com/microsoft/TypeScript/pull/63449#issuecomment-4346688853) **afurm** submitted CLA agreement commands in various formats, including a malformed company entry
 * [today](https://github.com/microsoft/TypeScript/pull/63449#issuecomment-4346697088) **afurm** demonstrated correct command usage and invoked the agree command with the company parameter
 * [today](https://github.com/microsoft/TypeScript/pull/63449#issuecomment-4346721551) **afurm** said "Closing this because I noticed #62052 already covers #62048. Sorry for the duplicate."
 * (today) **afurm** closed the issue

### [Issue microsoft/TypeScript#63450](https://github.com/microsoft/TypeScript/issues/63450) (Open)

**Rename symbol renamed element declaration in node\_modules**

*Renaming a JSX tag with Rename Symbol mistakenly alters the element declaration in node_modules type definitions.*

 * created by **EvertsRozz**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [later](https://github.com/microsoft/TypeScript/issues/63450#issuecomment-4354002353) **RyanCavanaugh** generated an automated response listing similar issues to help start analysis

### [Issue microsoft/TypeScript#63451](https://github.com/microsoft/TypeScript/issues/63451) (Open, `Bug`, `Fix Available`, `Domain: classes`)

**\`new super\(\)\` in static method does not cause error**

*TypeScript 6.0 incorrectly allows new super() in static blocks and methods without error.*

 * created by **Withered-Flower-0422**
 * [later](https://github.com/microsoft/TypeScript/issues/63451#issuecomment-4354002466) **RyanCavanaugh** thanked the user, listed similar issues, and explained that 'new super()' is valid per the ECMAScript spec

### [Issue microsoft/TypeScript#63452](https://github.com/microsoft/TypeScript/issues/63452) (Open, `Needs Investigation`)

**TS IntelliSense is very slow or loads endlessly on simple ArkType wrapper**

*VSCode’s TypeScript IntelliSense hangs indefinitely and exhibits extremely slow error detection in a simple ArkType wrapper project*

 * created by **FunctionDJ**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [later](https://github.com/microsoft/TypeScript/issues/63452#issuecomment-4354002566) **RyanCavanaugh** provided an automatically generated list of similar issues with relevance percentages

### [PR microsoft/TypeScript#63453](https://github.com/microsoft/TypeScript/pull/63453) (Closed, `For Uncommitted Bug`)

**fix: detected calls to child\_process from a function\.\.\. in\.\.\.**

*Sanitized child_process usage in scripts/find-unused-diganostic-messages.mjs to prevent command injection*

 * created by **orbisai0security**
 * (later) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4351194500) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4351194517) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454) (Closed, `Design Limitation`)

**\`1 \| 2 \| 3\` can be assigned to \`1 \| 2\` when using a recursive type**

*A recursive mapped type wrapper in TypeScript unsoundly allows assignment between unions 1|2|3 and 1|2.*

 * created by **carljohnsonnewhampshire-hue**
 * [later](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4353396688) **carljohnsonnewhampshire-hue** demonstrated that the BuildType example allowed num and str to be assigned to each other without type errors
 * [later](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4353411975) **carljohnsonnewhampshire-hue** demonstrated that when object type nesting is one level shallower, both assignments fail as expected
 * [later](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4354002694) **RyanCavanaugh** provided an automatically generated analysis with links to similar issues

