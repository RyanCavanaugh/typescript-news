# Report for 2026-07-14 (Tuesday, July 14th, 2026)

5 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @coopjyoung asked whether a PR to update hover to use merged documentation would be welcome in [microsoft/TypeScript#63603](https://github.com/microsoft/TypeScript/issues/63603#issuecomment-4977767143)
    * @denis-migdal asked how proposed inference increases type problems in [microsoft/TypeScript#63643](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4971877503)

## Activity Summary

### [Issue microsoft/TypeScript#63603](https://github.com/microsoft/TypeScript/issues/63603) (Open, `Bug`, `Domain: LS: Completion Lists`)

**Issue: TypeScript autocomplete for template literal types ignores user's Quote Style preference**

*Autocomplete suggestions for template literal type keys always use double quotes, ignoring the user's configured quote style preference.*

 * (1 week ago) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Completion Lists`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63603#issuecomment-4977767143) **coopjyoung** asked whether a PR to update hover to use merged documentation would be welcome

### [Issue microsoft/TypeScript#63643](https://github.com/microsoft/TypeScript/issues/63643) (Closed, `Duplicate`)

**Reusable callbacks: When destructuring, missing properties should be excluded from the infered type\.**

*TypeScript should infer destructured callback parameters using only the referenced properties instead of requiring the entire type.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4960899332) **RyanCavanaugh** compared this issue to #42419 and argued that presupposing lack of destructuring implies disregard isn't universally valid, noting counterexamples outlined in those comments
 * **RyanCavanaugh** added label `Duplicate`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4962860894) **denis-migdal** disagreed that the issue was a duplicate and explained their inference-level callback typing context
 * [today](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4971700937) **RyanCavanaugh** stated that the proposed inference would accept more input values and increase the risk of type problems
 * [today](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4971877503) **denis-migdal** questioned how the proposed inference would increase type problems, explained that it would solve type issues when reusing callbacks, and illustrated how to force type parameters with alternative generic definitions
 * [today](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4972289232) **RyanCavanaugh** provided a code snippet demonstrating a unit mismatch that crashed the Mars probe
 * [today](https://github.com/microsoft/TypeScript/issues/63643#issuecomment-4972686606) **denis-migdal** argued that the type definition of bindings, not the suggestion, caused the issue and illustrated with example code

### [Issue microsoft/TypeScript#63645](https://github.com/microsoft/TypeScript/issues/63645) (Closed, `Duplicate`)

**Narrowing union types requires at least 2 members**

*TypeScript fails to recognize exhaustive narrowing for a discriminated union when only one variant remains after an earlier filter.*

 * created by **500-internal-server-error**
 * [today](https://github.com/microsoft/TypeScript/issues/63645#issuecomment-4970481686) **MartinJohns** said "Duplicate of #38963."
 * [today](https://github.com/microsoft/TypeScript/issues/63645#issuecomment-4971716637) **RyanCavanaugh** said "Better match is #23572"
 * **RyanCavanaugh** added label `Duplicate`
 * (later) **500-internal-server-error** closed the issue

### [Issue microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646) (Open, `Needs Investigation`, **johnfav03**)

**tsc \-\-watch does not work in docker**

*tsc --watch fails to detect file changes in Docker bind-mounted workspaces on macOS after upgrading to version 7.0.2.*

 * created by **laverdet**

### [Issue microsoft/TypeScript#63647](https://github.com/microsoft/TypeScript/issues/63647) (Closed)

**Can basic type inference be provided on promise fulfillment/rejected values**

*Request for TypeScript to infer the string type of a promise’s fulfillment value instead of defaulting to unknown.*

 * created by **arka-prat-juno**
 * [later](https://github.com/microsoft/TypeScript/issues/63647#issuecomment-4978494682) **arka-prat-juno** apologized and closed the issue after noting it was addressed previously
 * (later) **arka-prat-juno** closed the issue

