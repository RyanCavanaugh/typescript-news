# Report for 2026-06-22 (Monday, June 22nd, 2026)

6 different users commented on 5 different issues.

## Recommended Actions

 * Response Recommended
    * @alecov asked how to annotate Example<T> to be invariant in [microsoft/TypeScript#63566](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4771157044)
    * @nmain reported unsoundness on property writes when subtyping is involved and provided example code in [microsoft/TypeScript#63566](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4772274987)

## Activity Summary

### [Issue microsoft/TypeScript#63560](https://github.com/microsoft/TypeScript/issues/63560) (Open, `Domain: Performance`, `Possible Improvement`)

**Quadratic duplicate declaration accumulation in intersection constructor properties can crash with RangeError**

*Quadratic accumulation of duplicate declarations in intersection constructor types causes RangeError crashes under diamond inheritance*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63560#issuecomment-4715669037) **MartinJohns** said "You should probably check if this still happens with tsgo."
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63560#issuecomment-4715904418) **canonic-epicure** said "That would be a huge context switch, staying with TS version for now."
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63560#issuecomment-4716141044) **MartinJohns** said "Kinda pointless then, since that version is not continued. 🤷‍♂️ "
 * [later](https://github.com/microsoft/TypeScript/issues/63560#issuecomment-4777370635) **canonic-epicure** said "I guess I can submit a reproduction-only issue to tsgo version, w/o a fix."

### [Issue microsoft/TypeScript#63566](https://github.com/microsoft/TypeScript/issues/63566) (Closed, `Working as Intended`)

**TypeScript doesn't consider contravariance in member functions even with strictFunctionTypes**

*TypeScript ignores contravariance in function-typed object members, allowing unsafe assignments even with strictFunctionTypes.*

 * created by **alecov**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4763077695) **guillaumebrunerie** explained that Example<T> is contravariant, that the suggested fix would make it covariant and thus incorrect, and that mutation of the argument causes the observed type inconsistency
 * [today](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4771157044) **alecov** acknowledged the contravariance point, explained using a dummy field to force invariance, demonstrated unsoundness due to mutation, and asked how to make Example<T> invariant
 * [today](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4772274987) **nmain** described a case of unsoundness on property writes when subtyping is involved and provided example code
 * **RyanCavanaugh** added label `Working as Intended`
 * [later](https://github.com/microsoft/TypeScript/issues/63566#issuecomment-4780976150) **RyanCavanaugh** explained that the problem was due to writes on properties rather than generic variance and pointed to issue #18770

### [PR microsoft/TypeScript#63571](https://github.com/microsoft/TypeScript/pull/63571) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump actions/checkout from 6\.0\.3 to 7\.0\.0 in the github\-actions group**

*Upgrade actions/checkout in the github-actions group from version 6.0.3 to 7.0.0*

 * **dependabot[bot]** added label `github_actions`
 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63573](https://github.com/microsoft/TypeScript/issues/63573) (Open, `Suggestion`, `Experience Enhancement`)

**Hover documentation for parameters documented with jsdoc renders improperly**

*VSCode hover feature misrenders JSDoc @param descriptions when using hyphens or wrapped lines.*

 * created by **SirzBenjie**

### [PR microsoft/TypeScript#63574](https://github.com/microsoft/TypeScript/pull/63574) (Open, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump js\-yaml from 4\.1\.1 to 4\.2\.0**

*Upgrade js-yaml to version 4.2.0 from 4.1.1 to incorporate safety documentation, new loader options, and bug fixes.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

