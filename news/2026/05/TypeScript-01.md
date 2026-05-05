# Report for 2026-05-01 (Friday, May 1st, 2026)

8 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @FunctionDJ asked how to replicate VSCode's language server interactions in [microsoft/TypeScript#63452](https://github.com/microsoft/TypeScript/issues/63452#issuecomment-4362048572)

## Activity Summary

### [Issue microsoft/TypeScript#52999](https://github.com/microsoft/TypeScript/issues/52999) (Open, `Suggestion`, `Awaiting More Feedback`)

**Make \`satisfies\` configurable to allow excess properties in nested values**

*Make TypeScript’s satisfies operator configurable to accept extra properties in nested objects*

 * [30 weeks ago](https://github.com/microsoft/TypeScript/issues/52999#issuecomment-3353869598) **RyanCavanaugh** said "@nzakas / @bradzacher can you explain the above? I don't understand the interaction - it doesn't seem like the EPC behavior of satisfies is relevant in that context"
 * [30 weeks ago](https://github.com/microsoft/TypeScript/issues/52999#issuecomment-3353981017) **bradzacher** explained that typescript-eslint's config function originated as an identity function for type support in .ts files, evolved with runtime enhancements, and that ESLint core later adopted a similar defineConfig with runtime features while now supporting .ts config extensions
 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/52999#issuecomment-3425688100) **pqnet** explained how to enforce and preserve strict typing for configuration objects using a generic enforceType function
 * [today](https://github.com/microsoft/TypeScript/issues/52999#issuecomment-4362705729) **daveycodez** said "Welp I just added"

### [Issue microsoft/TypeScript#63447](https://github.com/microsoft/TypeScript/issues/63447) (Closed, `Duplicate`)

**5\.9 regression: Union types served by mutually exclusive function overloads not working**

*TypeScript 5.9 fails to apply mutually exclusive overloads for functions accepting ArrayBuffer or Uint8Array.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63447#issuecomment-4337372133) **RyanCavanaugh** provided an automated list of similar issues
 * **RyanCavanaugh** added label `Duplicate`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63447#issuecomment-4342003676) **hyperair** thanked MartinJohns for explaining that the change in lib.d.ts narrowed types and broke the usecase, and noted that modifying the Buffer.from signature in @types/node is difficult
 * [today](https://github.com/microsoft/TypeScript/issues/63447#issuecomment-4362557182) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63451](https://github.com/microsoft/TypeScript/issues/63451) (Open, `Bug`, `Fix Available`)

**\`new super\(\)\` in static method does not cause error**

*TypeScript 6.0 incorrectly allows new super() in static blocks and methods without error.*

 * (yesterday) **RyanCavanaugh** set milestone to `Dormant`, and removed from milestone `Backlog`
 * **typescript-bot** added label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/63451#issuecomment-4361516140) **mkantor** asked why the bot added the "Fix Available" label and noted it happened on issue #63391 as well

### [Issue microsoft/TypeScript#63452](https://github.com/microsoft/TypeScript/issues/63452) (Open, `Needs Investigation`)

**TS IntelliSense is very slow or loads endlessly on simple ArkType wrapper**

*VSCode’s TypeScript IntelliSense hangs indefinitely and exhibits extremely slow error detection in a simple ArkType wrapper project*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63452#issuecomment-4354134744) **RyanCavanaugh** noted that the video showed insertion at the log end, reported his own local responsiveness, suggested @ssalbdivad for clues, and concluded it likely didn't meet the 6.0 LS patch bar
 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63452#issuecomment-4362048572) **FunctionDJ** suggested creating an independent reproduction repository and asked how to replicate VSCode's language server interactions

### [PR microsoft/TypeScript#63453](https://github.com/microsoft/TypeScript/pull/63453) (Closed, `For Uncommitted Bug`)

**fix: detected calls to child\_process from a function\.\.\. in\.\.\.**

*Sanitized child_process usage in scripts/find-unused-diganostic-messages.mjs to prevent command injection*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4351194517) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4354624555) **jakebailey** noted that this was not a security problem, suggested the author hadn't tested locally, pointed out formatting issues, and asked if the author was a bot and how they determined the issue needed fixing
 * [today](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4359360882) **ritschwumm** asked why the change modified every line of the diagnostic script and whether the line endings were switched
 * [today](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4363011723) **orbisai0security** acknowledged the review, clarified that diagName was repo-controlled and not attacker-controlled, refocused the PR on security hardening and cleaned up line-ending noise

### [Issue microsoft/TypeScript#63455](https://github.com/microsoft/TypeScript/issues/63455) (Closed)

**tsserver does not load \`@types/node\` from nested project \`typeRoots\` unless \`types\` is explicit**

*VS Code's TypeScript service does not load @types/node from a nested project's typeRoots unless types are explicitly included*

 * created by **garysassano**
 * [today](https://github.com/microsoft/TypeScript/issues/63455#issuecomment-4361466846) **mkantor** asked if the user had configured VS Code to use the project's TypeScript version and explained how to check or change it and why defaults changed in TypeScript 6.0
 * [today](https://github.com/microsoft/TypeScript/issues/63455#issuecomment-4362839179) **garysassano** thanked mkantor and explained that updating VS Code to TypeScript 6.0.2 resolved the discrepancy between tsc and VS Code errors
 * (today) **garysassano** closed the issue

### [Issue microsoft/TypeScript#63456](https://github.com/microsoft/TypeScript/issues/63456) (Open, `Suggestion`, `Awaiting More Feedback`)

**String\.split\(\) method's separator argument should allow undefined**

*Allow undefined as separator in String.split to return the full string array per spec.*

 * created by **JohanRonnblom**
 * [today](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4362960471) **MartinJohns** noted that the issue duplicated #38331, argued that optional parameters and undefined are equivalent, and suggested providing types locally

