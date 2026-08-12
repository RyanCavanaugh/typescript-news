# Report for 2026-08-09 (Sunday, August 9th, 2026)

6 different users commented on 10 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#61577](https://github.com/microsoft/TypeScript/issues/61577) (Closed, `Not a Defect`)

**Confusing error message when there is an accidental circular reference in monorepo**

*TypeScript’s uninformative overwrite error hides accidental circular project references in monorepos, complicating debugging.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/61577#issuecomment-5219811100) **RyanCavanaugh** said "I can understand how that might be confusing, because the situation itself is confusing, but the error message really does describe reality"
 * (2 days ago) **RyanCavanaugh** added label `Not a Defect`, and removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/61577#issuecomment-5234964976) **typescript-automation[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#63680](https://github.com/microsoft/TypeScript/pull/63680) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 8 updates**

*Update eight GitHub Actions in the repository root, upgrading checkout, setup-node, cache, CodeQL, and Scorecard actions to their latest releases.*

 * (2 weeks ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63680#issuecomment-5234802035) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63733](https://github.com/microsoft/TypeScript/issues/63733) (Open, `Not a Defect`)

**\[REGRESSION 6\.0\.2\-\>7\.0\.2\] Type \`T\<A\>\` not assignable to \`T\<A\|B\>\`**

*ChartDataset<'scatter'> is no longer assignable to ChartDataset<keyof ChartTypeRegistry> due to a TypeScript 7.0.2 regression.*

 * created by **denis-migdal**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63733#issuecomment-5221000005) **MartinJohns** stated that the same error occurred in TS 6.0 with stable types ordering and pointed out that their types used UnionToIntersection, which the TypeScript team declared unsupported
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63733#issuecomment-5224681687) **denis-migdal** thanked maintainers and asked if there was a way to avoid `UnionToIntersection`
 * **RyanCavanaugh** added label `Not a Defect`

### [PR microsoft/TypeScript#63736](https://github.com/microsoft/TypeScript/pull/63736) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 9 updates**

*Nine GitHub Actions dependencies in the root directory were updated to newer versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63737](https://github.com/microsoft/TypeScript/issues/63737) (Open, `Not a Defect`)

**Superclass type argument inferred as unknown when it's only used as a method parameter type constraint**

*TypeScript infers unknown when extracting a superclass’s generic type used only in a method parameter constraint instead of the expected type.*

 * created by **aweebit**

### [PR microsoft/TypeScript#63738](https://github.com/microsoft/TypeScript/pull/63738) (Open, `For Uncommitted Bug`)

**lib: document remaining ProxyHandler trap parameters**

*Document missing ProxyHandler trap parameters and rename setPrototypeOf’s v parameter to newPrototype to align JSDoc with code*

 * created by **yogesh968**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63738#issuecomment-5237173780) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63738#issuecomment-5237173801) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#63739](https://github.com/microsoft/TypeScript/pull/63739) (Open, `For Uncommitted Bug`)

**lib: fix Atomics\.waitAsync timeout parameter description**

*Fix Atomics.waitAsync JSDoc to correctly document the timeout parameter and its default behavior.*

 * created by **yogesh968**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63739#issuecomment-5237175018) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#63740](https://github.com/microsoft/TypeScript/pull/63740) (Open, `For Uncommitted Bug`)

**lib: fix two Reflect JSDoc defects**

*Two JSDoc defects in lib.es2015.reflect.d.ts include missing documentation for Reflect.set's value parameter and incorrect parameter names in Reflect.setPrototypeOf's description.*

 * created by **yogesh968**
 * [later](https://github.com/microsoft/TypeScript/pull/63740#issuecomment-5237175533) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63740#issuecomment-5237175538) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63741](https://github.com/microsoft/TypeScript/pull/63741) (Open, `For Uncommitted Bug`)

**lib: fix JSDoc @param tags that document nothing**

*Align JSDoc @param tags with actual parameter names in RegExp[Symbol.matchAll] and WScript.CreateObject and fill missing descriptions.*

 * created by **yogesh968**
 * [later](https://github.com/microsoft/TypeScript/pull/63741#issuecomment-5237175941) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63741#issuecomment-5237175975) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63741#issuecomment-5237177917) **microsoft-github-policy-service[bot]** prompted the contributor to agree to the CLA by replying with the appropriate command

### [Issue microsoft/TypeScript#63742](https://github.com/microsoft/TypeScript/issues/63742) (Open)

**Rest\-parameter mapped\-type wrapping breaks tuple\-literal inference once real\-world complexity is added**

*The use of a rest-parameter mapped type to inject ThisType in jml’s signature prevents tuple literal inference in complex scenarios.*

 * created by **brettz9**

