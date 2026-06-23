# Report for 2026-06-21 (Sunday, June 21st, 2026)

4 different users commented on 5 different issues.

## Recommended Actions

 * Response Recommended
    * @hesprs asked whether they should open a new issue or report to the TypeScript issue #47599 in [microsoft/TypeScript#62995](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-4768241891)

## Activity Summary

### [Issue microsoft/TypeScript#62995](https://github.com/microsoft/TypeScript/issues/62995) (Closed, `Fixed`)

**Bug with type argument inference if it has default value \`= undefined\` and actual value is object with non\-arrow function**

*TypeScript incorrectly infers generic type arguments defaulting to undefined when given an inline object with non-arrow functions.*

 * **RyanCavanaugh** added label `Fixed`
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3761049019) **RyanCavanaugh** said "Confirmed in nightly playground"
 * (22 weeks ago) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-4768241891) **hesprs** asked whether they needed to open a new issue or report to the linked TypeScript issue after still encountering errors

### [Issue microsoft/TypeScript#63565](https://github.com/microsoft/TypeScript/issues/63565) (Open)

**\`export\` modifier on \`enum\` disables \`This condition will always return \* ts2845\`**

*Adding the export modifier to an enum prevents TypeScript from reporting a ts2845 error on an always-true condition.*

 * created by **eps1lon**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63565#issuecomment-4751644133) **mkantor** explained that enums can be declaration-merged and that external modules might define the same enum, causing pessimistic analysis
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63565#issuecomment-4751672793) **mkantor** clarified that they misread the condition and that the second part only checks the truthiness of AdapterOutputType.PAGES
 * [later](https://github.com/microsoft/TypeScript/issues/63565#issuecomment-4768133967) **eps1lon** said "The program would know all the values after declaration merging. How would more values in AdapterOutputType change AdapterOutputType.PAGES === 1"

### [Issue microsoft/TypeScript#63566](https://github.com/microsoft/TypeScript/issues/63566) (Open)

**TypeScript doesn't consider contravariance in member functions even with strictFunctionTypes**

*TypeScript ignores contravariance in function-typed object members, allowing unsafe assignments even with strictFunctionTypes.*

 * created by **alecov**
 * [today](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4763077695) **guillaumebrunerie** explained that Example<T> is contravariant, that the suggested fix would make it covariant and thus incorrect, and that mutation of the argument causes the observed type inconsistency

### [PR microsoft/TypeScript#63571](https://github.com/microsoft/TypeScript/pull/63571) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump actions/checkout from 6\.0\.3 to 7\.0\.0 in the github\-actions group**

*Upgrade actions/checkout in the github-actions group from version 6.0.3 to 7.0.0*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

