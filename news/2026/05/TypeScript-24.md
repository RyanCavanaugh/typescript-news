# Report for 2026-05-24 (Sunday, May 24th, 2026)

7 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @XIshArkIX asked if there were any plans to solve the problem in [microsoft/TypeScript#17592](https://github.com/microsoft/TypeScript/issues/17592#issuecomment-4531208759)

## Activity Summary

### [Issue microsoft/TypeScript#17592](https://github.com/microsoft/TypeScript/issues/17592) (Open, `Suggestion`, `Waiting for TC39`)

**Extending string\-based enums**

*Support extending string-based TypeScript enums using an extends keyword or spread syntax to avoid redefining existing enums.*

 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/17592#issuecomment-1357009982) **masak** explained why using 'extends' on enums contradicts closed-world assumptions and opposed the proposed syntax
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/17592#issuecomment-1605675427) **alita-moore** asked about plans to implement enum inclusion functionality and provided a TypeScript code example
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/17592#issuecomment-1605947288) **masak** explained that using extends for enums breaks the closed-world assumption and exhaustiveness checks
 * [today](https://github.com/microsoft/TypeScript/issues/17592#issuecomment-4531208759) **XIshArkIX** said "Hey guys, it's been a long time since there has been no activity here. I don't want to stir up a hornet's nest, but the problem is still relevant. Are there any plans to solve it?"
 * [today](https://github.com/microsoft/TypeScript/issues/17592#issuecomment-4532120182) **masak** explained that a tc39 enum proposal exists and that TypeScript enum changes depend on it, then recommended a workaround using const assertions and object spread

### [Issue microsoft/TypeScript#56235](https://github.com/microsoft/TypeScript/issues/56235) (Open, `Suggestion`, `Awaiting More Feedback`)

**Safe type assertion \(upcast / widening\) operator**

*Introduce a safe `as!` type assertion operator that only permits casting to a wider type without altering runtime behavior.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-2025651824) **saltman424** requested syntactic sugar for 'satisfies' expressions to avoid duplicating type parameters and linked the related issue
 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-3141256372) **jcalz** cross-linked `satisfiesas`, `satisfias`, and `sassafras` with two issue comments
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-4145657649) **5cover** asked whether the operator model type annotation would mirror standard type annotation semantics including assignability and excess property checks, and suggested syntax variants like 'ascribe', 'be', and 'to'.
 * [later](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-4533848101) **mkantor** suggested using 'x satisfies as T' syntax and explained its benefits

### [PR microsoft/TypeScript#63443](https://github.com/microsoft/TypeScript/pull/63443) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 5 updates**

*Update actions/setup-node, upload-artifact, cache, codeql-action, and github-script to their latest versions in the root directory.*

 * **dependabot[bot]** added label `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63443#issuecomment-4342434504) **G-11-P** said "Merge approval granted"
 * [today](https://github.com/microsoft/TypeScript/pull/63443#issuecomment-4530790284) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63481](https://github.com/microsoft/TypeScript/issues/63481) (Open, `Help Wanted`, `Domain: lib.d.ts`, `Possible Improvement`)

**\`ReadonlySet\` lacks documentation for \`has\`, \`forEach\` and \`size\`**

*ReadonlySet<T> in lib.es2015.collection.d.ts lacks documentation for its has, forEach, and size members.*

 * (1 week ago) **RyanCavanaugh** added labels `Domain: lib.d.ts`, `Possible Improvement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63481#issuecomment-4531194717) **vitalysinitsin** said "I'd like to do that!"

### [PR microsoft/TypeScript#63502](https://github.com/microsoft/TypeScript/pull/63502) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 6 updates**

*Update six GitHub Actions in the repository root to their latest patch and minor versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63503](https://github.com/microsoft/TypeScript/issues/63503) (Open)

**Name of \`String\.padStart\`'s \`maxLength\` parameter is misleading**

*String.padStart and padEnd’s ‘maxLength’ parameter name misleads by implying maximum output length instead of the actual minimum length.*

 * created by **youngspe**

### [PR microsoft/TypeScript#63504](https://github.com/microsoft/TypeScript/pull/63504) (Open, `For Uncommitted Bug`)

**lib: fix misleading \`maxLength\` param on string pad\* methods**

*Rename the maxLength parameter in String.padStart and padEnd to targetLength and update their documentation to match MDN.*

 * created by **youngspe**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63504#issuecomment-4531146841) **youngspe** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#63505](https://github.com/microsoft/TypeScript/pull/63505) (Closed, `For Backlog Bug`)

**Fix narrowing of destructured discriminated union parameters with defaults**

*Removed initializer guards in checker predicates to restore type narrowing for destructured discriminated union parameters with default values.*

 * created by **wolfe8105**
 * (later) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63505#issuecomment-4535358692) **wolfe8105** said "@microsoft-github-policy-service agree"

