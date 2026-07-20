# Report for 2026-07-19 (Sunday, July 19th, 2026)

7 different users commented on 8 different issues.

## Recommended Actions

 * Moderation
    * @nofaceprotocol5-prog posted unrelated content in [microsoft/TypeScript#63662](https://github.com/microsoft/TypeScript/pull/63662#issuecomment-5020161307)
 * Response Recommended
    * @LangLangBart provided CPU profiling results to illustrate the performance issue in [microsoft/TypeScript#63653](https://github.com/microsoft/TypeScript/issues/63653#issuecomment-5016906450)

## Activity Summary

### [Issue microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508) (Open, `Discussion`)

**6\.0 Migration Guide**

*Placeholder issue for drafting and publishing the migration guide for version 6.0.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871404071) **ljharb** asked what the difference between bundler and node10 was and why node10 support was removed, noting that people supporting old nodes would lose type support
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871588327) **andrewbranch** explained the distinctions between node10, bundler, and node16 module resolution algorithms and justified dropping node10 from TypeScript’s maintained algorithms
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871607338) **ljharb** argued that in latest node all code was CJS or ESM because they're indistinguishable; noted that testing multiple TypeScript versions was prohibitively hard due to TS 6 incompatibility; decided to use bundler; mentioned that resolve@next already models all node resolution permutations and has near-zero maintenance cost
 * [later](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-5023031732) **xr0master** advised updating code instead of requesting libraries to support Node 10

### [PR microsoft/TypeScript#63589](https://github.com/microsoft/TypeScript/pull/63589) (Closed, `For Uncommitted Bug`)

**lib: add Math\.sumPrecise type definition \(ES2025\)**

*Add Math.sumPrecise type declarations to the TypeScript esnext.math library for upcoming ES2026 support.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63589#issuecomment-4809926294) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63589#issuecomment-4809926301) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63589#issuecomment-4826321995) **MartinJohns** said "Duplicate of #63429."
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63590](https://github.com/microsoft/TypeScript/pull/63590) (Closed, `For Uncommitted Bug`)

**lib: add Math\.sumPrecise type definition \(ES2025\)**

*Add TypeScript definitions for the new ES2026 Math.sumPrecise method in the esnext.math library.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63590#issuecomment-4809947237) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63590#issuecomment-4809947257) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63590#issuecomment-4826322993) **MartinJohns** said "Duplicate of #63429."
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63615](https://github.com/microsoft/TypeScript/pull/63615) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 5 updates**

*Updates actions/cache from 5.0.5 to 6.1.0 and all CodeQL GitHub Action steps from 4.36.2 to 4.36.3 in the root directory.*

 * (2 weeks ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63615#issuecomment-5017965194) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63653](https://github.com/microsoft/TypeScript/issues/63653) (Open, `Needs Investigation`, **ahejlsberg**)

**Template literal union type\-checking is exponentially slower when type is explicitly annotated vs inferred**

*TypeScript’s type-checker experiences exponential slowdown when checking large template literal union types on explicitly annotated variables compared to inferred ones.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63653#issuecomment-4997425821) **RyanCavanaugh** said "This might not be a bug; // repro-inferred.ts really does have to do less work than // repro.ts - the latter has to do an assignability check, the former does not."
 * [today](https://github.com/microsoft/TypeScript/issues/63653#issuecomment-5016906450) **LangLangBart** profiled CPU usage of tsc6 for repro.ts and repro-inferred.ts and identified hotspots confirming exponential behavior

### [PR microsoft/TypeScript#63660](https://github.com/microsoft/TypeScript/pull/63660) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 6 updates**

*Dependabot updates six GitHub Actions dependencies in one directory to their latest versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63661](https://github.com/microsoft/TypeScript/issues/63661) (Open, `Bug`)

**\`as\`/\`satisfies\` between exponentiation operators cannot be safely erased**

*Removing 'as' or 'satisfies' assertions between exponentiation operators in TypeScript changes operator grouping without errors.*

 * created by **magic-akari**
 * (later) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63662](https://github.com/microsoft/TypeScript/pull/63662) (Closed, `For Uncommitted Bug`)

**Add OpenAI workflow for Deno linting and automation**

*Add GitHub Actions workflow to install Deno and perform continuous linting and testing.*

 * created by **nofaceprotocol5-prog**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63662#issuecomment-5020148863) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63662#issuecomment-5020148864) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63662#issuecomment-5020161307) **nofaceprotocol5-prog** provided an unclear, unrelated update about autonomous 24/7 updates and fixes
 * [later](https://github.com/microsoft/TypeScript/pull/63662#issuecomment-5023803977) **RyanCavanaugh** said "We are not accepting unsolicited PRs for new github workflows."
 * (later) **RyanCavanaugh** closed the issue

