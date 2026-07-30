# Report for 2026-07-26 (Sunday, July 26th, 2026)

8 different users commented on 22 different issues.

## Recommended Actions

 * Response Recommended
    * @jasonlyu123 asked whether the LSP-connected IPC API should use generated or source positions and if purely generated positions could be requested in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5086629187)

## Activity Summary

### [PR microsoft/TypeScript-go#4679](https://github.com/microsoft/TypeScript-go/pull/4679) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 4 updates**

*Upgrade actions/setup-node to v7.0.0 and bump CodeQL init, autobuild, and analyze actions in root directory.*

 * (6 days ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4679#issuecomment-5090263800) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (later) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Add support for external content mapper packages in TypeScript configuration to transform unsupported file types into valid TypeScript syntax.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5076803173) **andrewbranch** thanked the reviewer, explained that patch 0002 was incorrect, and illustrated the ambiguity in mapping end-of-span positions while suggesting left/right affinity context
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5076887616) **andrewbranch** provided an update before vacation and asked for feedback from implementers on the SpanMapPurpose classification
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5078512064) **mikearnaldi** explained that patch 0002 was incomplete, described mapping ambiguity at span boundaries requiring left/right affinity, and noted that his patch enabled completions at file end but might not be correct
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5086629187) **jasonlyu123** inquired whether the LSP-connected IPC API parameters should use generated or source positions and if purely generated positions could be requested

### [PR microsoft/TypeScript-go#4717](https://github.com/microsoft/TypeScript-go/pull/4717) (Closed)

**bundled/nativepath: survive kernel\-reported paths that the process cannot see \(PRoot link2symlink\)**

*tsgo crashes and fails module resolution inside PRoot's link2symlink environment due to inaccessible kernel-reported paths.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4717#issuecomment-5059907205) **jakebailey** questioned the explanation's clarity and asked why an issue wasn't filed first
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4717#issuecomment-5059950310) **dlecan** said "@microsoft-github-policy-service agree"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4717#issuecomment-5060234733) **dlecan** apologized for going straight to the PR, filed issue #4718 and rewrote the PR description; clarified the trust-but-verify approach using /proc/self/fd with a POSIX fallback and noted the bundled change mirrors a previous Windows fix; said they would address inline comments
 * [later](https://github.com/microsoft/TypeScript-go/pull/4717#issuecomment-5092037358) **dlecan** stated Android Termux/Proot was too niche, said they would close the PR, and directed support to issue #4715
 * (later) **dlecan** closed the issue

### [PR microsoft/TypeScript-go#4749](https://github.com/microsoft/TypeScript-go/pull/4749) (Open)

**Add \`Infer function return type\` refactoring code action**

*Implement initial 'Infer function return type' refactoring code action with fourslash testing infrastructure in typescript-go*

 * created by **xeho91**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4749#issuecomment-5084350033) **xeho91** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript-go#4751](https://github.com/microsoft/TypeScript-go/issues/4751) (Closed)

**\`package\.json\` points to the wrong repository**

*package.json's bugs.url and repository.url incorrectly point to the TypeScript repository rather than this project*

 * created by **abrahamguo**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4751#issuecomment-5085845909) **jakebailey** said "This repo is temporary and we are accepting issues in both. This repo will be archived in the near future."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4752](https://github.com/microsoft/TypeScript-go/issues/4752) (Open, `Crash`, **jakebailey**, **Copilot**)

**\`tsconfig\.json\`: \`{"" }\` causes a panic, and more TS errors than v6**

*An empty tsconfig.json literal {} crashes the compiler with a 'negative Repeat count' panic and produces more errors than TypeScript v6.*

 * created by **abrahamguo**
 * **abrahamguo** added label `Crash`
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4753](https://github.com/microsoft/TypeScript-go/issues/4753) (Closed, **jakebailey**, **Copilot**)

**Putting a compiler option at the top level instead of in \`compilerOptions\` no longer reports**

*Top-level compiler options in tsconfig.json no longer produce errors with tsgo, unlike TypeScript 6.0.*

 * created by **abrahamguo**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4754](https://github.com/microsoft/TypeScript-go/issues/4754) (Closed, **jakebailey**, **Copilot**)

**TS5092 no longer has a file/line/column**

*TS5092 error reported by tsgo lacks file, line, and column location information compared to TypeScript 6.0*

 * created by **abrahamguo**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4755](https://github.com/microsoft/TypeScript-go/issues/4755) (Closed, **jakebailey**, **Copilot**)

**TS no longer reports "Did you mean" for misspelled \`tsconfig\.json\` options**

*tsgo no longer suggests corrections for misspelled tsconfig compiler options like TypeScript 6.0 did*

 * created by **abrahamguo**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4756](https://github.com/microsoft/TypeScript-go/pull/4756) (Open, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 5 updates**

*Update GitHub Actions dependencies in root directory by upgrading actions/checkout to 7.0.1, actions/setup-node to 7.0.0, and CodeQL actions to 4.37.3.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript-go#4758](https://github.com/microsoft/TypeScript-go/issues/4758) (Closed)

**disableSourceOfProjectReferenceRedirect causes lodash per\-method submodule import to resolve to the wrong function**

*Enabling disableSourceOfProjectReferenceRedirect in a referenced TypeScript project causes lodash/get imports to resolve as lodash/set under tsgo.*

 * created by **valentinmelusson**

### [PR microsoft/TypeScript-go#4759](https://github.com/microsoft/TypeScript-go/pull/4759) (Closed, **jakebailey**, **Copilot**)

**Restore spelling suggestions for unknown tsconfig options**

*Reapply spelling suggestions for unknown tsconfig.json options by using the suggestion algorithm in JSON parsing and emitting TS5025.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4760](https://github.com/microsoft/TypeScript-go/pull/4760) (Closed, **jakebailey**, **Copilot**)

**Restore source location for TS5092**

*Associate TS5092 diagnostics with the root expression in tsconfig.json to restore file position and add test coverage for array-valued configs.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4761](https://github.com/microsoft/TypeScript-go/pull/4761) (Closed, **jakebailey**, **Copilot**)

**Report compiler options misplaced at the tsconfig root**

*Implement diagnostic TS6258 and nonzero exit status for misplaced tsconfig compiler options outside compilerOptions*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4762](https://github.com/microsoft/TypeScript-go/pull/4762) (Open, **jakebailey**, **Copilot**)

**Prevent panic and duplicate diagnostics for malformed tsconfig properties**

*Normalized recovered JSON node spans and suppressed redundant diagnostics to prevent panics and duplicate errors from malformed tsconfig properties.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

