# Report for 2026-05-13 (Wednesday, May 13th, 2026)

10 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @danon asked how to write the function to accept arbitrary string in f2() in [microsoft/TypeScript#63474](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448069111)
    * @danon asked how to narrow unknown to Record<> using type guards in [microsoft/TypeScript#63474](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448332825)
    * @danon asked how to generalize their TypeScript casting functions to work with arbitrary string fields in [microsoft/TypeScript#63474](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448669897)
    * @danon provided repro steps showing unexpected behavior in [microsoft/TypeScript#63474](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4450943690)
    * @microsoft-github-policy-service asked the contributor to agree to the CLA in [microsoft/TypeScript#63475](https://github.com/microsoft/TypeScript/pull/63475#issuecomment-4448613248)
    * @microsoft-github-policy-service asked the contributor to agree to the CLA in [microsoft/TypeScript#63475](https://github.com/microsoft/TypeScript/pull/63475#issuecomment-4448613282)
    * @Hamzaa6296 asked whether the team would accept a PR to fix the issue in [microsoft/TypeScript#63476](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4449294554)

## Activity Summary

### [Issue microsoft/TypeScript#63463](https://github.com/microsoft/TypeScript/issues/63463) (Open, `Bug`, `Domain: LS: Completion Lists`)

**\`default\` keyword is offered in expression\-bodied arrow function completions**

*TypeScript’s completion engine incorrectly suggests ‘default’ in expression-bodied arrow function contexts despite it being invalid.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4435004904) **DhineshPonnarasan** asked how to test the bug in TS 7 language service and whether to use a local build, wait for the Playground, or other methods
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4438556963) **MartinJohns** said "@DhineshPonnarasan See: https://github.com/microsoft/typescript-go#preview"
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4440108994) **DhineshPonnarasan** confirmed reproduction in TS 7 language service preview and showed that invalid statement-oriented keywords like default appeared in expression-bodied arrow function completions
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Completion Lists`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63473](https://github.com/microsoft/TypeScript/issues/63473) (Closed)

**\`default\` keyword is incorrectly offered in expression\-bodied arrow function completions**

*TypeScript completion list incorrectly offers ‘default’ in expression-bodied arrow function contexts.*

 * created by **ArshVermaGit**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63473#issuecomment-4428107346) **MartinJohns** said "Duplicate of #63463."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63473#issuecomment-4432297625) **RyanCavanaugh** provided automated analysis suggesting the behavior is a genuine completion bug, referenced a similar issue, and explained why default completions are inappropriate in expression-bodied arrow functions
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63474](https://github.com/microsoft/TypeScript/issues/63474) (Open, `Design Limitation`)

**Simple inversion of \`&&\` causes types to stop being valid, even though the js execution is the same**

*Swapping 'field === "start"' and 'field in obj' in an && expression breaks TypeScript type narrowing despite identical runtime logic.*

 * created by **danon**
 * [today](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4445298756) **RyanCavanaugh** explained that narrowing doesn't reapply new information backward through the control flow graph and that fixing it would require invasive restructuring with serious performance and circularity implications
 * **RyanCavanaugh** added label `Design Limitation`
 * [today](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4447913950) **danon** said "@RyanCavanaugh it doesn't need to reach earlier. The error happens inside the condition block, so in both cases it's later, not earlier."
 * [today](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448039364) **MartinJohns** explained that f1 narrows obj to object & Record<"start", unknown> because field is narrowed before the in check, whereas f2 does not narrow obj since field isn't narrowed prior to the in obj check
 * [today](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448069111) **danon** asked how to write a type-safe function to return a field from an object or throw an error for arbitrary string fields without using type assertions or user-defined type guards
 * [today](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448109986) **MartinJohns** said "Use Record instead of object."
 * [today](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448332825) **danon** said "@MartinJohns how do I narrow unknown to Record using type guards? (I don't want to use type assertions such as as or is, because they aren't checked by ts."
 * [later](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448480310) **MartinJohns** said "You don't. You use a type assertion, that's what they're there for."
 * [later](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448492456) **danon** explained that they wanted dynamic type checking to throw errors immediately instead of using type assertions that might propagate invalid values
 * [later](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448524038) **danon** demonstrated a working example with a single field without type assertions and noted that the term 'assertion' is misleading, suggesting 'type silencers'
 * [later](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448534652) **MartinJohns** explained that type assertions complement runtime checks and that type assertion isn’t misleading, then said the repo isn’t suitable for basic language support questions and left the discussion
 * [later](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4448669897) **danon** demonstrated a TypeScript implementation for safe runtime checks without type assertions and asked how to generalize it to arbitrary string field names
 * [later](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4450482265) **mkantor** pointed out that general language discussions belong in the TypeScript Community Chat, provided an example generic cast function implementation, suggested using established validation libraries, and clarified the safe use and risks of type assertions
 * [later](https://github.com/microsoft/TypeScript/issues/63474#issuecomment-4450943690) **danon** demonstrated that cast returned undefined instead of throwing when given a string and property key

### [PR microsoft/TypeScript#63475](https://github.com/microsoft/TypeScript/pull/63475) (Open, `For Uncommitted Bug`)

**Fix minor typos in protocol\.ts **

*Correct spelling errors in protocol.ts JSDoc comments without affecting runtime behavior*

 * created by **iamdaven**
 * [later](https://github.com/microsoft/TypeScript/pull/63475#issuecomment-4448612020) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63475#issuecomment-4448612041) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63475#issuecomment-4448613123) **typescript-bot** thanked the author for the PR, cautioned to preserve TSServer API compatibility, and pinged reviewers for extra review
 * [later](https://github.com/microsoft/TypeScript/pull/63475#issuecomment-4448613248) **microsoft-github-policy-service[bot]** requested the contributor to agree to the CLA by replying with the appropriate template
 * [later](https://github.com/microsoft/TypeScript/pull/63475#issuecomment-4448613282) **microsoft-github-policy-service[bot]** requested the contributor to agree to the CLA by replying with the appropriate template

### [Issue microsoft/TypeScript#63476](https://github.com/microsoft/TypeScript/issues/63476) (Open)

**\`===\` is not strong enough to narrow equal values to the same type**

*TypeScript's strict equality check doesn't narrow an unknown input to a specific string literal union type.*

 * created by **danon**
 * [later](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4449294554) **Hamzaa6296** reproduced the issue, proposed updating the type narrowing logic for === between unknown and a generic type T, and asked if the team would accept a PR
 * [later](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4451293547) **jcalz** marked the issue as a duplicate of #36772

### [Issue microsoft/TypeScript#63477](https://github.com/microsoft/TypeScript/issues/63477) (Open)

**\`NoInfer\` on second generic parameter doesn't pick up inference from sibling methods**

*Using NoInfer on the second generic parameter prevents B from being inferred from the b() return type, defaulting to object.*

 * created by **paoloricciuti**

