# Report for 2026-04-24 (Friday, April 24th, 2026)

9 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @ryadaladyb45-blip offered to submit a fix for the misleading Chinese translation of TS2561 in [microsoft/TypeScript#63274](https://github.com/microsoft/TypeScript/issues/63274#issuecomment-4315442451)

## Activity Summary

### [Issue microsoft/TypeScript#49489](https://github.com/microsoft/TypeScript/issues/49489) (Closed, `Discussion`)

**Reference Thread: Correctness Improvement in Unconstrained Type Parameters**

*TypeScript 4.8 now errors when unconstrained type parameters propagate null or undefined to non-nullable positions, requiring constraints or checks.*

 * **RyanCavanaugh** added label `Discussion`
 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/49489#issuecomment-1152846529) **jcalz** suggested disabling the lint rule and lamented with a link to issue #21732
 * (2.1 years ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/49489#issuecomment-4315167296) **sin-strokes** said "Yes"

### [Issue microsoft/TypeScript#63274](https://github.com/microsoft/TypeScript/issues/63274) (Open, `Bug`, `Domain: Error Messages`, `i18n`)

**\[Localization\] Misleading Chinese translation for TS2561 error message**

*The Chinese translation for TS2561 error message incorrectly swaps the property and type relationship, causing confusion and requiring correction.*

 * (5 weeks ago) **RyanCavanaugh** added labels `i18n`, `Domain: Error Messages`
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63274#issuecomment-4115353850) **BillionClaw** said "I've been looking into the Chinese translation for TS2561 — happy to submit a fix for the misleading text."
 * [today](https://github.com/microsoft/TypeScript/issues/63274#issuecomment-4315442451) **ryadaladyb45-blip** offered to submit a fix for the misleading Chinese translation of TS2561

### [Issue microsoft/TypeScript#63425](https://github.com/microsoft/TypeScript/issues/63425) (Open, `Suggestion`, `Experimentation Needed`)

**Hover display for non\-homomorphic mapped types renders numeric\-string keys indistinguishably from numeric keys**

*TypeScript's hover display omits quotes for numeric-string keys in non-homomorphic mapped types, making them appear as numeric keys.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63425#issuecomment-4304393568) **mkantor** rephrased the issue by explaining that B is displayed as a valid but observably-distinct type, which may confuse users copying it
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63425#issuecomment-4304396986) **codpro2005** acknowledged the oversight and explained scoping the issue to the hover inconsistency
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63425#issuecomment-4305918025) **RyanCavanaugh** provided a list of similar issues
 * [today](https://github.com/microsoft/TypeScript/issues/63425#issuecomment-4315518448) **jcalz** proposed considering this a feature request rather than a bug and argued for choosing valid key spellings in displayed object types
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Experimentation Needed`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63425#issuecomment-4316899276) **RyanCavanaugh** said "@jcalz I remember the last time we poked at this, an enormous cloud of bees emerged, but I don't recall exactly what flavor. Worth poking again though"

### [Issue microsoft/TypeScript#63427](https://github.com/microsoft/TypeScript/issues/63427) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Add type definition for Math\.sumPrecise \(ES2025 / TC39 proposal\)**

*Add missing TypeScript declaration for the ES2026 Math.sumPrecise method to prevent compile errors.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4306545660) **snakefood3232** offered to create type augmentations for Math.sumPrecise and submit a PR in two days
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4306994771) **RyanCavanaugh** said "@snakefood3232 actually what I need is a risotto recipe added to README.md, can you put up a PR right away?"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4310859954) **827652549** offered to fix the issue, corrected the ES version and placement in the issue description, opened PR #63429 with necessary changes, and asked about adding a Backlog milestone and for guidance on PR conventions
 * **RyanCavanaugh** added to milestone `Backlog`

### [PR microsoft/TypeScript#63429](https://github.com/microsoft/TypeScript/pull/63429) (Open, `For Backlog Bug`)

**lib: add Math\.sumPrecise type definition \(ES2025\)**

*Add type definition for the Stage 4 TC39 Math.sumPrecise method to TypeScript’s esnext standard library definitions.*

 * created by **827652549**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63429#issuecomment-4310683342) **827652549** said "@microsoft-github-policy-service agree"
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63430](https://github.com/microsoft/TypeScript/issues/63430) (Open)

**Paths from tsconfig are not used if declaration is on a different partition**

*TypeScript ignores tsconfig path mappings for imports on a different drive when emitting declaration files, producing absolute paths.*

 * created by **dragomirtitian**
 * [today](https://github.com/microsoft/TypeScript/issues/63430#issuecomment-4314787953) **RyanCavanaugh** provided an automated list of similar issues to the report

### [Issue microsoft/TypeScript#63432](https://github.com/microsoft/TypeScript/issues/63432) (Open)

**\`Math\.sign\` JSDoc comment has grammatical typo**

*Fix JSDoc comment in Math.sign for grammar by changing “the x” to “x”.*

 * created by **Bertie690**

### [PR microsoft/TypeScript#63433](https://github.com/microsoft/TypeScript/pull/63433) (Open, `For Uncommitted Bug`)

**docs: improve Math\.sign JSDoc grammar and clarity**

*Updated Math.sign JSDoc in es2015.core.d.ts to correct phrasing and add missing comma for consistency.*

 * created by **SkyCoderAakash**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63433#issuecomment-4318410016) **MartinJohns** cited the pull request template discouraging typo-only fixes

### [PR microsoft/TypeScript#63434](https://github.com/microsoft/TypeScript/pull/63434) (Open, `For Backlog Bug`)

**fix: allow bracket\-notation enum access as computed property name in type positions**

*Extend binding logic to allow bracket-notation enum access with literal keys as computed property names in type declarations*

 * created by **Scolliq**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63434#issuecomment-4319067419) **Scolliq** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63434#issuecomment-4319842552) **jakebailey** said "Can you please tell me what tool you used to send this PR, and how you chose this issue to fix?"

