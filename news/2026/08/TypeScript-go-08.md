# Report for 2026-08-08 (Saturday, August 8th, 2026)

5 different users commented on 10 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#4611](https://github.com/microsoft/TypeScript-go/pull/4611) (Closed)

**Add devcontainer feature lockfile**

*Pin devcontainer feature versions and digests by adding a .devcontainer/devcontainer-lock.json for dprint-asdf, github-cli, and node.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-4951931688) **MasterTLF** said "fix without second review and approval"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5028999862) **MasterTLF** said "is this resolved"
 * (2 weeks ago) **MasterTLF** closed the issue
 * (today) **MasterTLF** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5227724864) **MasterTLF** said "wait for required approvals from githubcopilot and then fix resolve merge comitt deploy"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5227783445) **MasterTLF** added a devcontainer feature lockfile to pin feature versions and digests, formatted the JSON per repo conventions, and confirmed PR feedback was addressed and tooling checks passed
 * [today](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5227789531) **MasterTLF** added a devcontainer feature lockfile to pin feature versions and digests, formatted the JSON per repo conventions, and confirmed PR feedback was addressed and tooling checks passed
 * [today](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5227806043) **MasterTLF** said "unblock merge, fix, merge new, commit, deploy"

### [PR microsoft/TypeScript-go#4749](https://github.com/microsoft/TypeScript-go/pull/4749) (Closed)

**Add \`Infer function return type\` refactoring code action**

*Implement initial 'Infer function return type' refactoring code action with fourslash testing infrastructure in typescript-go*

 * created by **xeho91**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4749#issuecomment-5084350033) **xeho91** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4749#issuecomment-5230503374) **xeho91** said "Superseded by work done in https://github.com/microsoft/typescript-go/pull/4855"
 * (later) **xeho91** closed the issue

### [PR microsoft/TypeScript-go#4853](https://github.com/microsoft/TypeScript-go/pull/4853) (Closed)

**Fix merge queue permissions**

*Add pull-requests: write permission to the GitHub Actions workflow to fix merge queue enqueue errors.*

 * created by **MasterTLF**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4853#issuecomment-5228383848) **jakebailey** said "Not sure why you need this but we definitely do not"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4854](https://github.com/microsoft/TypeScript-go/issues/4854) (Closed, `enhancement`, **jakebailey**)

**macOS: allow DYLD\_INSERT\_LIBRARIES in tsgo**

*Add Hardened Runtime entitlements to tsgo’s macOS builds to allow DYLD_INSERT_LIBRARIES for dyld interposition tools.*

 * created by **wan9chi**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4854#issuecomment-5230324746) **jakebailey** stated they were limited in options and offered to check with the signing team, noted it seemed strange to un-harden the binary and cursed to rely on track file reads

### [PR microsoft/TypeScript-go#4855](https://github.com/microsoft/TypeScript-go/pull/4855) (Open)

**Add LSP refactoring capabilities framework**

*Add a base LSP refactoring framework with provider registration, action filtering, disablement support, testing helpers, and position mapping.*

 * created by **xeho91**

### [PR microsoft/TypeScript-go#4856](https://github.com/microsoft/TypeScript-go/pull/4856) (Closed)

**\[Experiment\] parallel type checking with weighted file batches**

*Parallel weighted-batch type checking achieves up to 11% faster checks, 9% faster wall times, and 11% less memory usage.*

 * created by **a-tarasyuk**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4856#issuecomment-5232172870) **jakebailey** said "Is this the same as #4313?"
 * (later) **a-tarasyuk** closed the issue
 * (later) **a-tarasyuk** reopened the issue
 * (later) **a-tarasyuk** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/4856#issuecomment-5232282883) **jakebailey** noted that the memory improvement was better than his PR for vscode and suggested that adjustments for other benchmarks might have impacted the results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4856#issuecomment-5232336778) **a-tarasyuk** acknowledged not seeing the PR, noted its differences in weight estimation and partitioning, and closed their own PR since work was underway

