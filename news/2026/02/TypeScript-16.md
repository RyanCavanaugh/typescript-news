# Report for 2026-02-16 (Monday, February 16th, 2026)

5 different users commented on 5 different issues.

## Recommended Actions

 * Response Recommended
    * @risalfajar reported that the plugin doesn't work like Webstorm in [microsoft/TypeScript#11865](https://github.com/microsoft/TypeScript/issues/11865#issuecomment-3912006964)
    * @everett1992 suggested that TypeScript should provide an option to ignore .ts files in node_modules or prefer .d.ts files in [microsoft/TypeScript#40426](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3910327930)
    * @Arlen22 reported that the issue was not fixed after upgrading to the latest version in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041819)

## Activity Summary

### [Issue microsoft/TypeScript#11865](https://github.com/microsoft/TypeScript/issues/11865) (Open, `Suggestion`, `Awaiting More Feedback`, `VS Code Tracked`)

**auto align colons in object literals, variables, and equals like WebStorm**

*Add a VSCode setting to align variable names, equals signs, and object literal colons like WebStorm.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/11865#issuecomment-2224969587) **slabcache** said "Bump"
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/11865#issuecomment-2481333667) **anasbarg** suggested using table-like formatting for object types and interfaces
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/11865#issuecomment-2619373310) **tje3d** suggested a prettier plugin for vertical alignment from HuggingFace
 * [today](https://github.com/microsoft/TypeScript/issues/11865#issuecomment-3912006964) **risalfajar** reported that the plugin didn't work like Webstorm

### [Issue microsoft/TypeScript#40426](https://github.com/microsoft/TypeScript/issues/40426) (Open, `Suggestion`, `Awaiting More Feedback`)

**Disable type checking for node\_modules entirely**

*Allow disabling TypeScript type checking for node_modules to avoid build errors caused by external libraries’ faulty type definitions.*

 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3257296565) **onyedikachi23** praised the proposed option to silence node_module type check messages while preserving type propagation
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3590991290) **sparr** encountered error checking in excluded node_modules and requested how to disable it
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3626316257) **Pentadome** said "I needed to import a .ts file from a node module and now i get typescript errors from that file. Why can't we set paths where we don't want type checking?"
 * [today](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3910327930) **everett1992** described node's limitation with loading .ts files in node_modules and advocated for a TypeScript feature to ignore .ts files or prefer .d.ts files

### [PR microsoft/TypeScript#63145](https://github.com/microsoft/TypeScript/pull/63145) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.2 to 4\.32\.3 in the github\-actions group**

*Bumps github/codeql-action from 4.32.2 to 4.32.3 to add experimental support for testing connections to private package registries.*

 * (yesterday) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63149](https://github.com/microsoft/TypeScript/issues/63149) (Open)

**\[TS\]: Incorrect handling of \`JSDoc\` description of interface property**

*VS Code incorrectly strips parentheses-enclosed JSX tags from interface property JSDoc descriptions in hover tooltips.*

 * created by **psnet**
 * **vs-code-engineering[bot]** assigned to **mjbvz**

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * created by **Arlen22**
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041807) **vs-code-engineering[bot]** suggested upgrading to the latest VS Code version and checking if the issue persisted
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041819) **Arlen22** reported that upgrading to the latest version did not fix the issue

