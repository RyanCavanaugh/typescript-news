# Report for 2025-12-29 (Monday, December 29th, 2025)

3 different users commented on 3 different issues.

## Recommended Actions

 * Response Recommended
    * @thromel asked if the updated behavior met expectations in [microsoft/TypeScript#62931](https://github.com/microsoft/TypeScript/pull/62931#issuecomment-3698968776)

## Activity Summary

### [Issue microsoft/TypeScript#43326](https://github.com/microsoft/TypeScript/issues/43326) (Open, `Suggestion`, `Needs Proposal`, **weswigham**)

**Support import maps and bare import specifiers**

*Enable import maps and bare import specifiers in TypeScript to map package names to file paths via HTML import maps*

 * **RyanCavanaugh** assigned to **weswigham**
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/43326#issuecomment-1324167022) **matthew-dean** asked if TypeScript could pick up Node.js import key resolution
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/43326#issuecomment-1674747582) **CMCDragonkai** said "It seems that at the moment one has to still specify paths mapping in tsconfig.json to get tsc to understand the #internal paths that now exists in package.json for NodeJS packages."
 * [later](https://github.com/microsoft/TypeScript/issues/43326#issuecomment-3698641039) **HolgerJeromin** critiqued making importmap support part of TypeScript due to diverse data sources and questioned its practicality

### [Issue microsoft/TypeScript#62030](https://github.com/microsoft/TypeScript/issues/62030) (Closed, `Needs More Info`)

**VS Code removes trailing comma in export statement**

*VS Code with Format on Save enabled removes the trailing comma in ES module export statements in .mjs files.*

 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3608365001) **craxal** confirmed reproduction of the issue, ran a bisect that did not identify an extension cause, and attached a screenshot
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3662802948) **craxal** said "@RyanCavanaugh Can you reopen this issue, please? As I said above, it still reproduces, and the bisect found nothing."
 * [today](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3697678468) **craxal** said "@RyanCavanaugh Can you please reopen the issue?"

### [PR microsoft/TypeScript#62931](https://github.com/microsoft/TypeScript/pull/62931) (Open, `For Backlog Bug`)

**Fix type parameter leak when using 'this' in reverse mapped types**

*Ensure methods using this in reverse mapped types correctly see each other’s inferred property types instead of leaking generic parameters.*

 * created by **thromel**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62931#issuecomment-3698968776) **thromel** thanked for feedback, updated the fix to check for mapped types in both intersection and union cases, and asked if the behavior met expectations

