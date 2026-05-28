# Report for 2026-05-22 (Friday, May 22nd, 2026)

9 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @geekeren asked whether a beta version was available for validation in [microsoft/TypeScript-go#3264](https://github.com/microsoft/TypeScript-go/pull/3264#issuecomment-4523942459)

## Activity Summary

### [PR microsoft/TypeScript-go#3264](https://github.com/microsoft/TypeScript-go/pull/3264) (Open, **gabritto**)

**support quick info and go to definition on mapped keys**

*Add quick info and go-to-definition support for mapped type keys in TypeScript.*

 * created by **Zzzen**
 * (5 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3264#issuecomment-4523942459) **geekeren** said "do we have any beta version to validate?"

### [Issue microsoft/TypeScript-go#3405](https://github.com/microsoft/TypeScript-go/issues/3405) (Open, `Domain: Editor`, **ahejlsberg**)

**JSDoc disapprears after type calculation**

*Hovering over a parameter from an intersection type no longer shows its JSDoc comment after TS type calculation.*

 * (5 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **ahejlsberg** assigned to **ahejlsberg**, and unassigned **jakebailey**, **Copilot**

### [Issue microsoft/TypeScript-go#3950](https://github.com/microsoft/TypeScript-go/issues/3950) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Hovering on type \`const\` does not display the specific type**

*Hovering over an as const literal in VS Code with the tsgo extension fails to show the literal type 42.*

 * (4 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3951](https://github.com/microsoft/TypeScript-go/pull/3951) (Closed, **jakebailey**, **Copilot**)

**Fix hover on \`const\` in \`as const\` to display the specific type**

*Hovering on const in '42 as const' shows 'const = 42' instead of the generic 'type const'.*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4026](https://github.com/microsoft/TypeScript-go/pull/4026) (Open)

**Rebuilt CLI watcher around new \`fswatch\` package**

*CLI watch functionality was rebuilt using the fswatch package, cutting idle CPU usage from ~5% to under 1%.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4026#issuecomment-4521711233) **DanielRosenwasser** noted that the branch was based on the fswatch branch and that relevant changes start at commit 8230a72, then retracted the suggestion to use a stacked PR due to lacking access

### [PR microsoft/TypeScript-go#4028](https://github.com/microsoft/TypeScript-go/pull/4028) (Open)

**fix\(4019\): skip unloaded projects during file rename**

*Skip projects without loaded programs during file rename handling to prevent nil pointer panics*

 * created by **dcsid**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4028#issuecomment-4522106807) **dcsid** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4028#issuecomment-4523304765) **DanielRosenwasser** said "Are we going to miss rename locations in any unloaded programs? In other words, should we be loading the programs on the fly? If not, whose responsibility is it to do that?"

### [PR microsoft/TypeScript-go#4029](https://github.com/microsoft/TypeScript-go/pull/4029) (Open)

**Fix and simplify JSDoc handling for binding elements**

*Simplify and fix JSDoc quick info handling for destructured binding elements to prevent duplicate documentation and improve consistency.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#4030](https://github.com/microsoft/TypeScript-go/pull/4030) (Closed)

** Add classified text output for VS Find All References**

*Add classified text output for VS Find All References to restore syntax-highlighted definitions and prevent related crashes.*

 * created by **navya9singh**

### [PR microsoft/TypeScript-go#4031](https://github.com/microsoft/TypeScript-go/pull/4031) (Open)

**Possible tests for refcount cache issues**

*Develop test cases to identify and diagnose issues in the reference count cache.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4032](https://github.com/microsoft/TypeScript-go/pull/4032) (Open, `dependencies`, `javascript`)

**Bump uuid and @azure/msal\-node**

*Remove the unused uuid package and upgrade @azure/msal-node from v5.1.3 to v5.2.2*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

### [PR microsoft/TypeScript-go#4033](https://github.com/microsoft/TypeScript-go/pull/4033) (Open)

**Fix resolveNodeHandle to check not only child nodes but ancestor nodes**

*Enhance resolveNodeHandle to traverse ancestor nodes alongside children to correctly identify the actual AST node*

 * created by **jet2jet**

### [Issue microsoft/TypeScript-go#4034](https://github.com/microsoft/TypeScript-go/issues/4034) (Open, `Domain: Declaration Emit`, `possible improvement`, `Needs Investigation`, **weswigham**)

**Behavior difference: tsgo emits different output when keys from one object are referenced in another object**

*tsgo emits generic index signatures for computed property keys instead of preserving specific keys, causing noise in diffs compared to tsc*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#4035](https://github.com/microsoft/TypeScript-go/issues/4035) (Open, `Domain: Editor`, `Needs Investigation`, **gabritto**)

**VSCode bulk save \(Replace All / Save All across many \.ts files\) deadlocks the LSP server**

*Bulk replacing across many .ts files in VSCode deadlocks the TypeScript Native Preview LSP server, which doesn’t restart on reload.*

 * created by **AdrianBannister**
 * **AdrianBannister** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#4036](https://github.com/microsoft/TypeScript-go/pull/4036) (Open, `dependencies`, `javascript`)

**Bump qs from 6\.15\.1 to 6\.15\.2**

*Bump qs dependency to version 6.15.2 to include multiple stringify and parse fixes and updated tests.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

