# Report for 2026-04-19 (Sunday, April 19th, 2026)

10 different users commented on 7 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4261231001) **andrewbranch** said "{firstname}.{lastname}@microsoft.com. Thanks!"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4262619314) **andrewbranch** said "@AndreiTS I think the issue in your video is #3423."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4267836701) **AndreiTS** confirmed that the issue matched #3423 and reported it was fixed in the new tsgo version with about 1.3 GiB RAM usage
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4276975338) **shinichy** described a proposed fix for getPackageRealpathFuncs to follow node_modules symlinks, provided a commit link and observed a reduced memory increase, and asked if the fix makes sense

### [Issue microsoft/TypeScript-go#3364](https://github.com/microsoft/TypeScript-go/issues/3364) (Open, **DanielRosenwasser**, **andrewbranch**, **mjbvz**, **Copilot**)

**No project found for untitled file**

*VS Code LSP reports a no project found for URI untitled:Untitled-1 error when opening an anonymous unsaved file*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3364#issuecomment-4216990910) **andrewbranch** suggested improving the error message and delaying file removal to handle diagnostic requests after closing an untitled file
 * (5 days ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3364#issuecomment-4276783406) **mjbvz** said "@andrewbranch You're using Dirk's LSP host, right? Or are you using the VS Code apis directly? "
 * [later](https://github.com/microsoft/TypeScript-go/issues/3364#issuecomment-4278651871) **DanielRosenwasser** stated that functionality should be handled by the language client and noted the project is on version 10.0.0-next.21, linking to the package.json

### [Issue microsoft/TypeScript-go#3441](https://github.com/microsoft/TypeScript-go/issues/3441) (Open, **jakebailey**, **Copilot**)

**Panic handling textDocument/semanticTokens/{full,range}: slice bounds out of range and token\-spans\-multiple\-lines**

*Semantic tokens full and range handlers panic due to slice bounds out-of-range errors and multi-line token spans.*

 * created by **liby**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3442](https://github.com/microsoft/TypeScript-go/pull/3442) (Open, **jakebailey**, **Copilot**)

**Fix utf8\.RuneLen bug in LineAndCharacterToPosition for invalid UTF\-8 sequences**

*Fixes utf8.RuneLen handling of invalid UTF-8 sequences in LineAndCharacterToPosition, adds position-mapping tests, and restores URI-filename conversion tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3442#issuecomment-4278352667) **jakebailey** said "This is certainly a bug, but I don't think it's the actual bug"

### [PR microsoft/TypeScript-go#3443](https://github.com/microsoft/TypeScript-go/pull/3443) (Open)

**Provide more accurate rename range in \`prepareRename\` LSP response**

*prepareRename returns ranges with leading trivia because it uses node.getStart instead of node.pos, causing mismatches with rename.*

 * created by **auvred**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3443#issuecomment-4281810956) **jakebailey** said "This seems fine but, no tests change?"

### [PR microsoft/TypeScript-go#3444](https://github.com/microsoft/TypeScript-go/pull/3444) (Open, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Bump actions/setup-node to v6.4.0 and update github/codeql-action in the root directory.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [PR microsoft/TypeScript-go#3445](https://github.com/microsoft/TypeScript-go/pull/3445) (Open)

**Improve recursion identity for direct type instantiations**

*Prevent false-positive generative recursion by excluding AST-resolved type references from using their symbol as recursion identity in isDeeplyNestedType.*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4282152133) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4282152795) **typescript-bot** reported build jobs starting and displayed their statuses

