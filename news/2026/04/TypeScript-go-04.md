# Report for 2026-04-04 (Saturday, April 4th, 2026)

6 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @zaverden provided issue #3342 for missing files field after testing dev version in [microsoft/TypeScript-go#3324](https://github.com/microsoft/TypeScript-go/issues/3324#issuecomment-4188207882)

## Activity Summary

### [PR microsoft/TypeScript-go#3314](https://github.com/microsoft/TypeScript-go/pull/3314) (Closed)

**Fix declaration emit alias reuse for inferred exports**

*Align serializeTypeName’s resolveEntityName call with upstream to preserve imported type aliases in declaration emit and update baselines accordingly.*

 * created by **thromel**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3314#issuecomment-4184928308) **jakebailey** said "Not sure if you have properly cloned the submodule or not, as you are missing other baseline updates that should have happened."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3314#issuecomment-4186676928) **thromel** initialized the TypeScript submodule, ran npm ci, accepted the missing baseline updates, and confirmed that the full test suite now passes
 * [today](https://github.com/microsoft/TypeScript-go/pull/3314#issuecomment-4187330427) **thromel** explained that CI was blocked on the ‘test (race mode)’ job due to lack of assigned runner and asked someone with permissions to rerun or inspect the runner pool
 * [today](https://github.com/microsoft/TypeScript-go/pull/3314#issuecomment-4187396711) **jakebailey** said "It's a known problem and will unblock itself eventually (otherwise I'll figure it out next week)"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3324](https://github.com/microsoft/TypeScript-go/issues/3324) (Closed, `bug`, **jakebailey**, **RyanCavanaugh**, **Copilot**)

**Different \`\-\-showConfig\` output**

*tsgo's --showConfig output differs from tsc by omitting file listings, using numeric enum values, and absolute paths.*

 * (2 days ago) **RyanCavanaugh** added label `bug`, and assigned to **RyanCavanaugh**
 * (2 days ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3324#issuecomment-4188207882) **zaverden** thanked RyanCavanaugh, reported that the files field issue persisted in the tested dev version, and created issue #3342

### [Issue microsoft/TypeScript-go#3341](https://github.com/microsoft/TypeScript-go/issues/3341) (Open)

**Suggested autocompletions are not accepted by the compiler**

*TypeScript’s autocomplete for the attributes option erroneously suggests "age" despite it being excluded by forbiddenAttributes.*

 * created by **limwa**

### [Issue microsoft/TypeScript-go#3342](https://github.com/microsoft/TypeScript-go/issues/3342) (Open, **jakebailey**, **Copilot**)

**\`\-\-showConfig\` does not include \`files\` field**

*tsgo’s --showConfig command fails to include the resolved files list in its output, unlike tsc’s --showConfig.*

 * created by **zaverden**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3342#issuecomment-4188373927) **jakebailey** said "Funnily, the original code was not written with the intent that this work, but behaved this way due to a bug!"

### [PR microsoft/TypeScript-go#3343](https://github.com/microsoft/TypeScript-go/pull/3343) (Open, **jakebailey**, **Copilot**)

**Fix \`\-\-showConfig\` to include \`files\` field**

*Fix tsgo --showConfig to include resolved files by removing incorrect glob filtering and directly listing all file paths*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3345](https://github.com/microsoft/TypeScript-go/pull/3345) (Open)

**Reparse CJS export assignments only when not shadowed by locals**

*Parser now tracks local module and exports shadowing to prevent misparsing CommonJS export assignments.*

 * created by **ahejlsberg**

