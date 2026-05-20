# Report for 2026-05-19 (Tuesday, May 19th, 2026)

8 different users commented on 11 different issues.

## Recommended Actions

 * Response Recommended
    * @matthewbordas reported documentation discrepancies and asked for clarification in [microsoft/TypeScript#63330](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4491058453)

## Activity Summary

### [Issue microsoft/TypeScript#63330](https://github.com/microsoft/TypeScript/issues/63330) (Open, `Docs`, **DanielRosenwasser**)

**\[V6\] \`module\` defaults is not \`esnext\`**

*TypeScript 6.0 incorrectly defaults the module option to ES2015 instead of ESNext, causing import attributes errors.*

 * (6 weeks ago) **RyanCavanaugh** added label `Docs`, and assigned to **DanielRosenwasser**
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4245384683) **mkantor** pointed out that the announcement post incorrectly stated that --outFile was removed in TypeScript 6.0 instead of deprecated and suggested it should reference 7.0
 * [today](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4491058453) **matthewbordas** reported seeing related compiler behavior issues, linked detailed notes, and noted that documentation defaults appear unsynchronized across core pages
 * [today](https://github.com/microsoft/TypeScript/issues/63330#issuecomment-4491128744) **mkantor** said "Yeah,  is in need of updates (perhaps other documentation pages too). See #63392."

### [Issue microsoft/TypeScript#63480](https://github.com/microsoft/TypeScript/issues/63480) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**\`Set\#size\` has grammar typo in \`lib\.es2015\.collection\.d\.ts\`**

*Fix grammar typo in Set#size documentation and standardize @returns capitalization in lib.es2015.collection.d.ts*

 * (4 days ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63480#issuecomment-4491680718) **RyanCavanaugh** said "Fixed in #63491"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63491](https://github.com/microsoft/TypeScript/pull/63491) (Closed, `For Uncommitted Bug`)

**63480**

*Corrects a grammar typo in the JSDoc for the Set#size method by changing 'the Set' to 'in the Set'. *

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63491#issuecomment-4483689354) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63491#issuecomment-4483689362) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63491#issuecomment-4487784135) **MartinJohns** said "Duplicate of #63482."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63492](https://github.com/microsoft/TypeScript/pull/63492) (Closed, `For Uncommitted Bug`)

**Fix typo in README: behavorial \-\> behavioral**

*Correct the misspelled word “behavorial” to “behavioral” in the README file.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63492#issuecomment-4484937242) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63492#issuecomment-4484937258) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63492#issuecomment-4487776201) **MartinJohns** quoted the pull request template warning against sending typo-fix-only PRs
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63493](https://github.com/microsoft/TypeScript/issues/63493) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: LS: Auto-import`)

**Configuration to auto\-import with inline type specifiers**

*Implement a config option to auto-import types using inline specifiers or top-level import syntax.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4489509337) **RyanCavanaugh** asked what the goal of the lint rule preferring type-only imports was
 * **RyanCavanaugh** added label `Domain: LS: Auto-import`
 * [today](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4489668508) **angrybacon** explained that the lint rule existed to prevent mixed import styles and to group imports consistently to reduce diff noise
 * [today](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4491115237) **guillaumebrunerie** explained the origin of the rule and referenced another rule forbidding inline type-only imports

### [Issue microsoft/TypeScript#63494](https://github.com/microsoft/TypeScript/issues/63494) (Closed)

**Typo in README: 'behavorial' should be 'behavioral'**

*The README incorrectly spells 'behavioral' as 'behavorial'.*

 * created by **Lefgk**
 * [today](https://github.com/microsoft/TypeScript/issues/63494#issuecomment-4489346219) **RyanCavanaugh** said "🤖 This is an automated response. I looked for things that might help (duplicates, FAQ entries, etc) but didn't find anything. A human will take a look!"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63495](https://github.com/microsoft/TypeScript/pull/63495) (Closed, `For Backlog Bug`)

**fix\(lib\): add missing article in Set\#size JSDoc**

*Adds the missing definite article 'the' in the Set#size JSDoc comment to correct grammar.*

 * created by **algojogacor**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63495#issuecomment-4491672976) **RyanCavanaugh** said "This was fixed in #63491. Why are so many people eager to fix this?"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63496](https://github.com/microsoft/TypeScript/pull/63496) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Update AI assistance guidelines in CONTRIBUTING\.md**

*Updated CONTRIBUTING.md to expand AI coding tool guidelines and ban bulk, agent-driven contributions.*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**

### [Issue microsoft/TypeScript#63497](https://github.com/microsoft/TypeScript/issues/63497) (Open)

**DOM: \`Element\#matches\(\)\` incorrectly narrows types**

*Using Element.matches with a specific tag name inside a negated condition incorrectly narrows the element's type to never.*

 * created by **Derugon**
 * [later](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4497649609) **MartinJohns** explained the issue was due to a specific change and suggested a workaround using the string overload

