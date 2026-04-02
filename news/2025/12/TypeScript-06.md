# Report for 2025-12-06 (Saturday, December 6th, 2025)

8 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @Mindaugas3 asked whether it was possible with existing TypeScript decorators in [microsoft/TypeScript#62820](https://github.com/microsoft/TypeScript/issues/62820#issuecomment-3621065252)
    * @Scalahansolo asked whether the implementation handles multiple file extensions such as .ts and .tsx in [microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3621281581)

## Activity Summary

### [PR microsoft/TypeScript#60005](https://github.com/microsoft/TypeScript/pull/60005) (Open, `For Backlog Bug`)

**Add source mappings for serialized properties with available declaration**

*Enable generating source mappings for serialized properties in output files when their declarations exist*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3547407768) **prometx11** asked if the change could be merged soon because it was blocking go-to navigation in monorepos and degrading developer experience
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3554914218) **jakebailey** requested merging main and inquired about porting to the Go codebase
 * [today](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3620601531) **dbrxnds** said "Should there be an issue opened in the native repo to track this for the go port? We recently switched to go but would like for this to stick. "
 * [today](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3620721369) **Andarist** synced the branch with main, noted no issues porting to the Go codebase, offered to prepare a porting PR, and asked about existing test infrastructure

### [Issue microsoft/TypeScript#62820](https://github.com/microsoft/TypeScript/issues/62820) (Closed, `Suggestion`, `Out of Scope`)

**@Concurrent decorator**

*Add a @Concurrent decorator to iterate loops concurrently with optional batching and Promise.all or Promise.allSettled logic.*

 * **RyanCavanaugh** added label `Out of Scope`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62820#issuecomment-3609567547) **typescript-bot** said "This issue has been marked as "Out of Scope" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (3 days ago) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/62820#issuecomment-3621065252) **Mindaugas3** said "is it maybe possible to do with existing typescript decorators?"

### [Issue microsoft/TypeScript#62838](https://github.com/microsoft/TypeScript/issues/62838) (Closed, `Duplicate`)

**\`JSON\.stringify\(undefined\)\` incorrectly types the return value as \`string\`**

*JSON.stringify(undefined) is typed as returning string in TypeScript instead of undefined.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62838#issuecomment-3612897786) **afgomez** said "Oh! sorry for the noise. I only searched for JSON.stringify() in the open issues and I didn't find anything 😅."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62838#issuecomment-3612938075) **MartinJohns** said "Searching with parentheses won't yield any result either way. Best results are with an added search modifier: JSON.stringify in:title"
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62838#issuecomment-3621467112) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844) (Closed, `For Milestone Bug`)

**Allow subpath imports that start with \`\#/\`**

*Allow subpath imports starting with '#/' in package.json imports to mirror matching exports entries.*

 * created by **magic-akari**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3621281581) **Scalahansolo** said "Does this implementation handle multiple file extensions? I.e. if a project contains both .ts and .tsx files?"
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3621362730) **jakebailey** assumed it would require a new module resolution mode

### [Issue microsoft/TypeScript#62859](https://github.com/microsoft/TypeScript/issues/62859) (Closed)

**Incorrect conversion to async function**

*VS Code’s async conversion quick fix wrongly injects a parameter into a callback that takes none.*

 * created by **johndoknjas**
 * [later](https://github.com/microsoft/TypeScript/issues/62859#issuecomment-3629145632) **vs-code-engineering[bot]** suggested upgrading to the latest stable VS Code version and verifying if the issue persists
 * **vs-code-engineering[bot]** assigned to **mjbvz**

### [Issue microsoft/TypeScript#62869](https://github.com/microsoft/TypeScript/issues/62869) (Closed, `Needs More Info`)

**\`tsserver\` checks stop updating when encountering certain \(perfectly valid\) code, basically error checking freezes**

*tsserver on a remote VS Code SSH setup freezes and stops reporting errors when encountering certain valid Remix TypeScript code.*

 * created by **Semmu**
 * **vs-code-engineering[bot]** assigned to **mjbvz**

