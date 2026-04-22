# Report for 2026-04-20 (Monday, April 20th, 2026)

5 different users commented on 20 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**, **Copilot**)

**Deprecate, remove support for \`baseUrl\`**

*TypeScript 6.0 will deprecate baseUrl support and require explicit prefixes in paths mappings.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4197912770) **SOMONSOUM** suggested removing the baseUrl setting and adding a paths configuration
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4205504780) **ArfanFahad** removed baseUrl and confirmed it worked after adding paths
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4220113144) **Jasper-Nelligan** reported that adding a catch-all paths entry caused VSCode to auto-suggest imports from node_modules and asked if anyone else was facing the issue
 * [later](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4288080930) **ruizmarc** confirmed experiencing the same issue where autoimports start with node_modules/ instead of the library name

### [PR microsoft/TypeScript#62646](https://github.com/microsoft/TypeScript/pull/62646) (Closed)

**Add iterator methods to DOMTokenList and improve code formatting**

*Adds entries, keys, and values iterator methods to DOMTokenList and improves code formatting across related interfaces.*

 * created by **atsushi196323**
 * [26 weeks ago](https://github.com/microsoft/TypeScript/pull/62646#issuecomment-3424407101) **jakebailey** said "This is not needed. These are already present in dom.generated.d.ts and so on."
 * (26 weeks ago) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/62646#issuecomment-4282661527) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405) (Closed, `Question`)

**VSCode's TypeScript Language Server Keeps Crashing on a Project**

*VSCode's TypeScript server repeatedly crashes with “TSServer exited. Code: 134” when opening a basic Vite React MUI project.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4261291709) **RyanCavanaugh** said "Yes, TypeScript provides language features in JavaScript projects"
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4271511013) **Takichih** said "Disabling Json auto imports worked for me too, thx @RyanCavanaugh "
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4272466307) **himhimlo** thanked RyanCavanaugh, confirmed both solutions worked, and stated that they had started using TypeScript 7
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4285354114) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63414](https://github.com/microsoft/TypeScript/pull/63414) (Closed, `For Uncommitted Bug`)

**Sort JSDoc parameter suggestions by argument position**

*Sort JSDoc @param completion suggestions by parameter position using unique index-based sortText instead of alphabetical order.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63414#issuecomment-4274030847) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63414#issuecomment-4274036241) **jakebailey** asked to disclaim what tool was used to send the PR
 * [today](https://github.com/microsoft/TypeScript/pull/63414#issuecomment-4282856152) **RyanCavanaugh** said "See #62963; this does not meet the 6.0 patch bar"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63416](https://github.com/microsoft/TypeScript/issues/63416) (Open, `Duplicate`)

**JSDoc parser treats \`@foo\` inside fenced code blocks as a tag, breaking hover previews**

*JSDoc parser does not respect fenced code blocks and incorrectly treats @tags inside them as JSDoc tags, breaking hover documentation previews.*

 * created by **BojanRatkovic**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63416#issuecomment-4276891516) **MartinJohns** said "Duplicate of #58992."
 * [today](https://github.com/microsoft/TypeScript/issues/63416#issuecomment-4282661729) **RyanCavanaugh** generated an automated analysis listing similar issues

### [Issue microsoft/TypeScript#63418](https://github.com/microsoft/TypeScript/issues/63418) (Closed, `Unactionable`)

**VS Code: support file jump for import paths with query params \(vanilla JS\)**

*Support file navigation in VS Code for vanilla JavaScript import paths that include query parameters to address browser caching*

 * created by **j787701730**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#63419](https://github.com/microsoft/TypeScript/issues/63419) (Open, `Won't Fix`)

**Transformer that updates an ambient property declaration is emitted as non\-ambient**

*TypeScript transformers updating ambient property declarations in TS 4.3 lose the ambient flag and emit the property.*

 * created by **JoostK**

### [Issue microsoft/TypeScript#63420](https://github.com/microsoft/TypeScript/issues/63420) (Open, `Bug`)

**union of pattern template literals intersected with optional brand mutually assignable to one with incompatible brand**

*TypeScript incorrectly allows mutual assignment between unions of template literal types intersected with incompatible optional brand properties.*

 * created by **jcalz**

