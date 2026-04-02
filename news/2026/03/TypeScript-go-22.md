# Report for 2026-03-22 (Sunday, March 22nd, 2026)

7 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @ejekanshjain provided reproduction steps with code examples in [microsoft/TypeScript-go#3146](https://github.com/microsoft/TypeScript-go/issues/3146#issuecomment-4108755647)
    * @yzhe554 reported that the issue doesn't exist in TS 6.0.1-rc with strict:true in [microsoft/TypeScript-go#3198](https://github.com/microsoft/TypeScript-go/issues/3198#issuecomment-4107063277)

## Activity Summary

### [Issue microsoft/TypeScript-go#3146](https://github.com/microsoft/TypeScript-go/issues/3146) (Closed, `bug`, `Domain: Emit`, **jakebailey**, **Copilot**)

**experimentalDecorators renames enum accesses with same name as class**

*experimentalDecorators causes enum member accesses sharing a class name to be incorrectly renamed in emitted code*

 * (4 days ago) **jakebailey** added label `Domain: Emit`, and assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3146#issuecomment-4108755647) **ejekanshjain** demonstrated that with typeorm decorators and tsgo ^7.0.0-dev.20260312.1+, the emitted js code used ItemType.Product_1 instead of ItemType.Product and provided code examples

### [Issue microsoft/TypeScript-go#3192](https://github.com/microsoft/TypeScript-go/issues/3192) (Closed, **weswigham**, **jakebailey**, **Copilot**)

**0320 vs 0321**

*The workglow build fails when using tsgo 7.0.0-dev.20260321.1 but succeeds with the previous day's 20260320.1 version.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4106400401) **Andarist** said "Correct behavior related to https://github.com/microsoft/TypeScript/pull/55229 + https://github.com/microsoft/TypeScript/pull/55522"
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4106574091) **jakebailey** asked which behavior was correct regarding the referenced issues
 * [today](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4106654378) **Andarist** confirmed the issue was real and referenced Anders’ PR and a follow-up test-only PR

### [Issue microsoft/TypeScript-go#3198](https://github.com/microsoft/TypeScript-go/issues/3198) (Closed)

**ts 2322**

*Mocking window.open to return null triggers a 'null not assignable to ArrayBuffer' error in TypeScript 5.9.3 but not in tsgo.*

 * created by **yzhe554**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3198#issuecomment-4106310819) **jakebailey** requested testing with v6.0 instead of 5.9 and asked if strictNullChecks was enabled
 * [today](https://github.com/microsoft/TypeScript-go/issues/3198#issuecomment-4107063277) **yzhe554** said "@jakebailey we have strict: true. The issue doesn't exist in ts 6.0.1-rc."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3198#issuecomment-4111641317) **RyanCavanaugh** said "Please post a complete repro in a new issue."
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3200](https://github.com/microsoft/TypeScript-go/issues/3200) (Closed, `Type Ordering`)

**Complex deeply nested types compile differently**

*Complex deeply nested TypeScript types compile correctly with tsc@6.0 but error under tsgo due to constraint mismatches.*

 * created by **ekwoka**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3200#issuecomment-4110001792) **jakebailey** suggested passing --stableTypeOrdering in TypeScript 6.0
 * [later](https://github.com/microsoft/TypeScript-go/issues/3200#issuecomment-4110035663) **ekwoka** observed that TypeScript 6.0 and tsgo both failed while the latest TSC succeeded, noted that TSC computed the correct type despite the error claiming 'unknown', and highlighted the curious behavioral difference

### [PR microsoft/TypeScript-go#3201](https://github.com/microsoft/TypeScript-go/pull/3201) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 2 directories with 3 updates**

*Update three GitHub Actions dependencies across the root and setup-go directories, bumping codecov-action to v5.5.3, github/codeql-action, and actions/cache.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

