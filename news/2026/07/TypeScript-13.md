# Report for 2026-07-13 (Monday, July 13th, 2026)

5 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @denis-migdal clarified that their issue was not a duplicate and asked for guidance on obscure TypeScript type patterns in [microsoft/TypeScript#63643](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4962860894)

## Activity Summary

### [Issue microsoft/TypeScript#63632](https://github.com/microsoft/TypeScript/issues/63632) (Open, `Suggestion`, `Awaiting More Feedback`)

**Feature request: machine\-readable \(JSONL\) diagnostics output**

*Add a JSONL output flag to the TypeScript compiler to provide machine-readable diagnostics in watch and noEmit modes.*

 * (6 days ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63632#issuecomment-4948211325) **MartinJohns** said "Related: #31566"
 * [today](https://github.com/microsoft/TypeScript/issues/63632#issuecomment-4962053869) **Alex-Bond** suggested allowing an outputAdapter option for tsc to convert internal events to custom outputs while acknowledging complexity

### [Issue microsoft/TypeScript#63640](https://github.com/microsoft/TypeScript/issues/63640) (Open, `Bug`, `Help Wanted`, `Domain: LS: Quick Info`)

**JSDoc for properties of intersected types is no longer merged**

*TypeScript 7.0.2 no longer merges JSDoc comments for identical properties in intersected types.*

 * created by **theblueplum**
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, `Domain: LS: Quick Info`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63642](https://github.com/microsoft/TypeScript/issues/63642) (Open, `Bug`, `Domain: check: Control Flow`)

**TS2871 'always nullish' false positive on binding destructured from \.map over spread\-of\-union \(regression 5\.9\.3 → 6\.0\.3; also in 7\.0\.2\)**

*TypeScript 6.0.3 and 7.0.2 incorrectly report a map-destructured ternary over a spread union as always nullish.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63642#issuecomment-4937170024) **RyanCavanaugh** provided a smaller repro with a concise TypeScript snippet
 * (3 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: check: Control Flow`
 * **RyanCavanaugh** added to milestone `Backlog`

### [Issue microsoft/TypeScript#63643](https://github.com/microsoft/TypeScript/issues/63643) (Closed, `Duplicate`)

**Reusable callbacks: When destructuring, missing properties should be excluded from the infered type\.**

*TypeScript should infer destructured callback parameters using only the referenced properties instead of requiring the entire type.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4960899332) **RyanCavanaugh** compared this issue to #42419 and argued that presupposing lack of destructuring implies disregard isn't universally valid, noting counterexamples outlined in those comments
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4962860894) **denis-migdal** disagreed that the issue was a duplicate and explained their inference-level callback typing context

### [Issue microsoft/TypeScript#63644](https://github.com/microsoft/TypeScript/issues/63644) (Open, `Needs More Info`)

**In a class, an unique symbol attribute is sometime lost during incremental build**

*Incremental builds with interface declaration merging sometimes lose a class's unique symbol property, leading to TS7053 errors.*

 * created by **denis-migdal**

### [Issue microsoft/TypeScript#63645](https://github.com/microsoft/TypeScript/issues/63645) (Closed, `Duplicate`)

**Narrowing union types requires at least 2 members**

*TypeScript fails to recognize exhaustive narrowing for a discriminated union when only one variant remains after an earlier filter.*

 * created by **500-internal-server-error**
 * [later](https://github.com/microsoft/TypeScript/issues/63645#issuecomment-4970481686) **MartinJohns** said "Duplicate of #38963."

