# Report for 2026-05-16 (Saturday, May 16th, 2026)

5 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @lppedd asked if the TypeScript path resolution error should have been resolved in version 6.x in [microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4470071879)

## Activity Summary

### [Issue microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**, **Copilot**)

**Deprecate, remove support for \`baseUrl\`**

*TypeScript 6.0 will deprecate baseUrl support and require explicit prefixes in paths mappings.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4288080930) **ruizmarc** confirmed experiencing the same issue where autoimports start with node_modules/ instead of the library name
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4293131060) **li-zck** affirmed encountering the issue and asked for a workaround
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4298121028) **RyanCavanaugh** requested posting a new issue with a reproduction so the team could investigate
 * [later](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4470071879) **lppedd** reported a TS5090 error regarding non-relative paths and asked if it was resolved in version 6.x

### [Issue microsoft/TypeScript#63463](https://github.com/microsoft/TypeScript/issues/63463) (Open, `Bug`, `Domain: LS: Completion Lists`)

**\`default\` keyword is offered in expression\-bodied arrow function completions**

*TypeScript’s completion engine incorrectly suggests ‘default’ in expression-bodied arrow function contexts despite it being invalid.*

 * (3 days ago) **RyanCavanaugh** added label `Domain: LS: Completion Lists`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4466304630) **puneetdixit200** requested assignment to add a fourslash completion test for expression-bodied arrow functions, investigate default keyword inclusion, and refine completion list logic
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4467790103) **DhineshPonnarasan** opened a draft PR containing a keyword-only, localized fix for concise arrow expression-body completions and focused fourslash coverage
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4468082728) **MartinJohns** directed the PR opener to open the PR in the correct repository and to disclose AI usage
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4468427446) **DhineshPonnarasan** thanked for the clarification, closed PR #63485, noted they would continue the fix in microsoft/typescript-go, and disclosed using AI assistance

### [Issue microsoft/TypeScript#63474](https://github.com/microsoft/TypeScript/issues/63474) (Closed, `Design Limitation`)

**Simple inversion of \`&&\` causes types to stop being valid, even though the js execution is the same**

*Swapping 'field === "start"' and 'field in obj' in an && expression breaks TypeScript type narrowing despite identical runtime logic.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448669897) **danon** demonstrated a TypeScript implementation for safe runtime checks without type assertions and asked how to generalize it to arbitrary string field names
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4450482265) **mkantor** pointed out that general language discussions belong in the TypeScript Community Chat, provided an example generic cast function implementation, suggested using established validation libraries, and clarified the safe use and risks of type assertions
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4450943690) **danon** demonstrated that cast returned undefined instead of throwing when given a string and property key
 * [today](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4468797191) **typescript-bot** said "This issue has been marked as "Design Limitation" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63477](https://github.com/microsoft/TypeScript/issues/63477) (Closed, `Duplicate`)

**\`NoInfer\` on second generic parameter doesn't pick up inference from sibling methods**

*Using NoInfer on the second generic parameter prevents B from being inferred from the b() return type, defaulting to object.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63477#issuecomment-4452751445) **paoloricciuti** questioned why it could infer `a()` before its declaration and suggested it might be a bug
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63477#issuecomment-4453104326) **jcalz** said "Because a() isn't context-sensitive.  It has no parameters to infer. Please read #47599 and #48538 "
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63477#issuecomment-4468796992) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63485](https://github.com/microsoft/TypeScript/pull/63485) (Closed, `For Uncommitted Bug`)

**Narrow keyword completions for concise arrow expression bodies**

*Restrict keyword completions in concise arrow function expression bodies to only valid expression keywords.*

 * created by **DhineshPonnarasan**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63485#issuecomment-4468427264) **DhineshPonnarasan** thanked for the guidance, closed the PR in favor of microsoft/typescript-go, and disclosed use of AI assistance
 * (today) **DhineshPonnarasan** closed the issue

### [Issue microsoft/TypeScript#63486](https://github.com/microsoft/TypeScript/issues/63486) (Open)

**\[Feature Request\] Official native AOT binary compiler**

*Propose Microsoft develop an official TypeScript native AOT compiler to generate cross-platform binaries with native library linking and UI/GPU support.*

 * created by **adevart**
 * [today](https://github.com/microsoft/TypeScript/issues/63486#issuecomment-4468699394) **MartinJohns** said "This is out of scope. Check the Viability Checklist again."

