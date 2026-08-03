# Report for 2026-08-02 (Sunday, August 2nd, 2026)

3 different users commented on 4 different issues.

## Recommended Actions

 * Response Recommended
    * @Abhirup0 offered to work on the issue in [microsoft/TypeScript#28396](https://github.com/microsoft/TypeScript/issues/28396#issuecomment-5166762655)
    * @snarbles2 asked whether it validated constraints to `Show` based on the original types and then performed substitution based on narrower constituents in [microsoft/TypeScript#63708](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5166870235)

## Activity Summary

### [Issue microsoft/TypeScript#28396](https://github.com/microsoft/TypeScript/issues/28396) (Open, `Bug`, `Domain: Parser`)

**parameter property's modifier may not be followed by newline**

*TypeScript incorrectly treats a parameter property modifier followed by a newline as separate parameters, producing a syntax error.*

 * (7.4 years ago) **RyanCavanaugh** added label `Domain: Parser`, set milestone to `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * [later](https://github.com/microsoft/TypeScript/issues/28396#issuecomment-5166762655) **Abhirup0** said "Hey i would like to work on this!"

### [PR microsoft/TypeScript#63680](https://github.com/microsoft/TypeScript/pull/63680) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 8 updates**

*Update eight GitHub Actions in the repository root, upgrading checkout, setup-node, cache, CodeQL, and Scorecard actions to their latest releases.*

 * (1 week ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63708](https://github.com/microsoft/TypeScript/issues/63708) (Open)

**It is possible to violate generic constraints when distributing union types**

*Distributive union types in TypeScript can bypass generic constraints, allowing invalid B extends A combinations without error.*

 * created by **aweebit**
 * [later](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5166145811) **snarbles2** questioned where distribution occurred and argued that the constraint was not violated due to Show's distribution, suggesting TypeScript's behavior might coincidentally produce the correct result
 * [later](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5166761425) **jcalz** demonstrated a potential unsoundness in TypeScript's type constraint evaluation with an example and playground link
 * [later](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5166870235) **snarbles2** asked whether it validated `Show` constraints based on the original types for `A` and `B` and then performed substitution based on the distributed constituents

### [PR microsoft/TypeScript#63713](https://github.com/microsoft/TypeScript/pull/63713) (Open, `For Backlog Bug`)

**Fix parameter property modifier followed by newline \(fixes \#28396\)**

*Allow line breaks between constructor parameter property modifiers and names by enabling permitLineBreak in parsing, fixing misinterpretation errors.*

 * created by **Abhirup0**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63713#issuecomment-5168441321) **Abhirup0** agreed to the Contributor License Agreement using the microsoft-github-policy-service

