# Report for 2026-08-07 (Friday, August 7th, 2026)

6 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @denis-migdal asked if there's a way to avoid `UnionToIntersection` in [microsoft/TypeScript#63733](https://github.com/microsoft/TypeScript/issues/63733#issuecomment-5224681687)

## Activity Summary

### [Issue microsoft/TypeScript#61577](https://github.com/microsoft/TypeScript/issues/61577) (Closed, `Not a Defect`)

**Confusing error message when there is an accidental circular reference in monorepo**

*TypeScript’s uninformative overwrite error hides accidental circular project references in monorepos, complicating debugging.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/61577#issuecomment-2869530619) **Jack-Works** reported their TypeScript, VSCode, and plugin versions
 * [yesterday](https://github.com/microsoft/TypeScript/issues/61577#issuecomment-5213091224) **Jack-Works** mentioned that updating to TypeScript 7.0.2 did not resolve the issue and provided reproduction steps including running pnpm install and inspecting files in VS Code
 * [today](https://github.com/microsoft/TypeScript/issues/61577#issuecomment-5219811100) **RyanCavanaugh** said "I can understand how that might be confusing, because the situation itself is confusing, but the error message really does describe reality"
 * (today) **RyanCavanaugh** added label `Not a Defect`, and removed label `Needs More Info`

### [Issue microsoft/TypeScript#63644](https://github.com/microsoft/TypeScript/issues/63644) (Open, `Needs More Info`)

**In a class, an unique symbol attribute is sometime lost during incremental build**

*Incremental builds with interface declaration merging sometimes lose a class's unique symbol property, leading to TS7053 errors.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-4995302238) **denis-migdal** said "Note: If you want to explore it, theses are the types from chart.js@4.5.1."
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-5056436448) **denis-migdal** reported similar errors in watch mode and asked if concurrent builds could corrupt the build cache
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-5207562513) **denis-migdal** asked if more specific information was needed
 * [today](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-5219776471) **RyanCavanaugh** said "@denis-migdal I need this reported in a way that is specific (refers to exactly one defect) and actionable (a concrete reproduction of that defect)."
 * [today](https://github.com/microsoft/TypeScript/issues/63644#issuecomment-5220587937) **denis-migdal** failed to reproduce the defect and hypothesized TS build file corruption due to VSCode concurrency; noted a commit mistake; reproduced the second issue and promised to open a separate issue and return if the first reoccurred

### [Issue microsoft/TypeScript#63731](https://github.com/microsoft/TypeScript/issues/63731) (Open, `Needs Investigation`, `Fix Available`, **johnfav03**)

**\-\-incremental: after a pnpm dependency version change, the cached run is slower than a cold run and most of the time is unattributed**

*pnpm's versioned module paths on dependency updates invalidate TypeScript incremental cache, causing cached builds to be slower with unaccounted time.*

 * created by **mushan0x0**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**
 * **typescript-automation[bot]** added label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/63731#issuecomment-5219905839) **RyanCavanaugh** said "What's the behavior in TypeScript 7.0?"

### [PR microsoft/TypeScript#63732](https://github.com/microsoft/TypeScript/pull/63732) (Closed, `For Backlog Bug`)

**fix: allow destructured require under module preserve \+ verbatimModuleSyntax**

*Fix false-positive TS1293 errors on destructured require in CommonJS modules with module preserve and verbatimModuleSyntax.*

 * created by **sankalpsthakur**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63732#issuecomment-5220645334) **jakebailey** informed that the TypeScript repo is closed for development and directed PRs to the typescript-go repo
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63733](https://github.com/microsoft/TypeScript/issues/63733) (Closed, `Not a Defect`)

**\[REGRESSION 6\.0\.2\-\>7\.0\.2\] Type \`T\<A\>\` not assignable to \`T\<A\|B\>\`**

*ChartDataset<'scatter'> is no longer assignable to ChartDataset<keyof ChartTypeRegistry> due to a TypeScript 7.0.2 regression.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63733#issuecomment-5221000005) **MartinJohns** stated that the same error occurred in TS 6.0 with stable types ordering and pointed out that their types used UnionToIntersection, which the TypeScript team declared unsupported
 * [today](https://github.com/microsoft/TypeScript/issues/63733#issuecomment-5224681687) **denis-migdal** thanked maintainers and asked if there was a way to avoid `UnionToIntersection`

### [Issue microsoft/TypeScript#63734](https://github.com/microsoft/TypeScript/issues/63734) (Closed)

**Add example for satisfies operator with dynamic object keys**

*Add a documentation example illustrating how to use the satisfies operator to validate dynamically constructed object keys.*

 * created by **rexblade58**
 * [later](https://github.com/microsoft/TypeScript/issues/63734#issuecomment-5226793379) **rexblade58** said "Thanks for the feedback! I found the answer I was looking for. Closing this to keep the issue tracker clean."
 * (later) **rexblade58** closed the issue

