# Report for 2026-03-15 (Sunday, March 15th, 2026)

7 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @sspencer-canva asked if there was anything they could do to help move this forward in [microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-4065010535)
    * @no-yan suggested tracking best candidates and only sorting the tie set to improve performance in [microsoft/TypeScript-go#3100](https://github.com/microsoft/TypeScript-go/pull/3100#issuecomment-4067227675)

## Activity Summary

### [PR microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020) (Open)

**Support for custom configurations**

*Enable passing custom tsconfig file names to the tsgo LSP to support solution-style repository configurations.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3963841180) **johnnycheng0210** asked jakebailey for feedback on requiring a window reload between custom config file name changes to avoid edge cases
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3963848279) **jakebailey** rejected restarting the client and asked Andrew Branch for insight
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3963951469) **andrewbranch** said "I'm not sure off the top of my head, I'd have to debug and step through."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-4065010535) **sspencer-canva** mentioned that the issue had been on hold for three weeks and asked if there was anything they could do to help

### [Issue microsoft/TypeScript-go#3094](https://github.com/microsoft/TypeScript-go/issues/3094) (Open, `bug`, **weswigham**)

**Declaration emit proceeds in the presence of TS7056**

*TypeScript emits declarations despite TS7056 errors caused by deeply nested conditional and tag-branded utility types.*

 * created by **RyanCavanaugh**
 * (2 days ago) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4068324272) **hkleungai** noted that the TS4053 error resembled a previously reported issue, argued that ts6 and ts7 should resolve the type reference without error, and referenced related issues #2504 and #3027

### [Issue microsoft/TypeScript-go#3099](https://github.com/microsoft/TypeScript-go/issues/3099) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch error-delta pipeline processed 300 repos, encountering server errors, analyzing 220 and reporting interesting changes, failures, timeouts.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180218) **typescript-bot** reported a panic failure in handling textDocument/diagnostic request with a debug assertion and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180236) **typescript-bot** reported a debug failure panic when handling textDocument/formatting request
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180253) **typescript-bot** reported a panic handling a textDocument/formatting request due to a debug failure false expression
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180276) **typescript-bot** reported a panic when handling textDocument/signatureHelp due to a debug failure expecting 2 < 1 and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180306) **typescript-bot** reported a panic during textDocument/documentHighlight request due to unexpected KindTypeParameter trivia
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180326) **typescript-bot** reported a premature server connection closure error with raw error text, replay commands, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180345) **typescript-bot** reported server connection closed prematurely and provided error details, affected repositories, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180366) **typescript-bot** reported a server connection closed prematurely error and provided affected repos, last few requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180394) **typescript-bot** reported that the server connection closed prematurely and provided affected repos, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180414) **typescript-bot** reported server connection closed prematurely on colinhacks/zod with error logs
 * [today](https://github.com/microsoft/TypeScript-go/issues/3099#issuecomment-4064180435) **typescript-bot** reported server connection closed prematurely and provided repro steps

### [PR microsoft/TypeScript-go#3100](https://github.com/microsoft/TypeScript-go/pull/3100) (Closed)

**Preallocate symbols in getSuggestionForSymbolNameLookup**

*Proposes preallocating the allSymbols array in getSuggestionForSymbolNameLookup to reduce reallocations and improve performance by about 3%.*

 * created by **camchenry**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3100#issuecomment-4067227675) **no-yan** suggested reducing sorting work by first tracking the best candidates for minimum Levenshtein distance and only sorting the final tie set to preserve determinism

### [PR microsoft/TypeScript-go#3101](https://github.com/microsoft/TypeScript-go/pull/3101) (Closed, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.6 to 4\.33\.0 in the github\-actions group across 1 directory**

*Bump the GitHub CodeQL Action dependency from version 4.32.6 to 4.33.0 in the main workflow directory.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [PR microsoft/TypeScript-go#3102](https://github.com/microsoft/TypeScript-go/pull/3102) (Open)

**Fix a formatting crash caused by template literal in parser\-recovered property signature**

*Fix formatting crash by ensuring grammar error nodes are processed to prevent misinterpreting template literals in recovered property signatures.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3103](https://github.com/microsoft/TypeScript-go/pull/3103) (Closed)

**Fixed a signature help crash related to tagged template calls**

*Fixed a crash in signature help that occurred when processing tagged template calls.*

 * created by **Andarist**

