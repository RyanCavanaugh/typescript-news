# Report for 2026-07-29 (Wednesday, July 29th, 2026)

11 different users commented on 13 different issues.

## Recommended Actions

 * Moderation
    * @nickshanks posted rude content in [microsoft/TypeScript#63683](https://github.com/microsoft/TypeScript/issues/63683#issuecomment-5128142005)
 * Response Recommended
    * @MulverineX pointed out that issue #44428 was closed despite not being fixed by TS 7.0 in [microsoft/TypeScript#41645](https://github.com/microsoft/TypeScript/issues/41645#issuecomment-5123864904)
    * @eeysudo provided a detailed terminal-only fix for TSServer hang issue in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-5121159127)
    * @nickshanks suggested updating the Issue text to mention Object.entries too in [microsoft/TypeScript#63683](https://github.com/microsoft/TypeScript/issues/63683#issuecomment-5128151844)

## Activity Summary

### [Issue microsoft/TypeScript#41645](https://github.com/microsoft/TypeScript/issues/41645) (Open, `Suggestion`, `Help Wanted`, `Effort: Moderate`, `Domain: LS: Completion Lists`, `Experience Enhancement`, `Experimentation Needed`)

**Incorrect inference/autocompletion on generic arrays, when values can be inferred from a defined object\.**

*TypeScript does not infer or suggest generic array values from keys defined in a related object property.*

 * [5.1 years ago](https://github.com/microsoft/TypeScript/issues/41645#issuecomment-857652928) **devanshj** offered two workarounds with TypeScript code examples
 * [5.1 years ago](https://github.com/microsoft/TypeScript/issues/41645#issuecomment-857683469) **TheMrZZ** described how the workaround reversed priority between objects and arrays for autocompletion, provided demonstration videos, and explained the expected behavior
 * [5.1 years ago](https://github.com/microsoft/TypeScript/issues/41645#issuecomment-857731950) **devanshj** provided a workaround link and noted missing autocomplete due to bug #44428
 * [today](https://github.com/microsoft/TypeScript/issues/41645#issuecomment-5123864904) **MulverineX** said "#44428 was closed despite not being fixed by TS 7.0"

### [Issue microsoft/TypeScript#45657](https://github.com/microsoft/TypeScript/issues/45657) (Closed, `Suggestion`, `In Discussion`)

**Deprecated property could be marked as strikethrough**

*Add strikethrough styling to deprecated TypeScript object properties to improve their visibility in code editors and the Playground*

 * **andrewbranch** added label `Suggestion`
 * [4.9 years ago](https://github.com/microsoft/TypeScript/issues/45657#issuecomment-909901832) **oldrich-s** traced the issue to this._languageService.getSuggestionDiagnostics only returning diagnostics for deprecated property access but not for property assignment
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/45657#issuecomment-2621120205) **BrainCrumbz** said "This seems definitely related to #39374 as well"
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#62636](https://github.com/microsoft/TypeScript/issues/62636) (Closed, `Needs More Info`)

**How can I force VSCode TypeScript auto\-imports to use \.ts extension instead of \.js?**

*VSCode TypeScript auto-imports inconsistently use .js and .ts extensions, prompting a request for a configuration or rule to enforce .ts.*

 * (40 weeks ago) **RyanCavanaugh** added label `VS Code Priority`, and removed label `VS Code Priority`
 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/62636#issuecomment-3430353542) **bwalendz** reported that manual typing included the extension but Copilot completion omitted it
 * [today](https://github.com/microsoft/TypeScript/issues/62636#issuecomment-5127637388) **RWB0104** mentioned encountering incorrect .js extension suggestions in a Turborepo monorepo setup and offered a ts-plugin-fix-import-suggestion package as a workaround
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`, `Domain: LS: TSServer`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4188436610) **AbhinavJD7** asked to be assigned to investigate the issue, described reproducing locally with large node_modules and tracing why the InferredProject graph update hangs
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4230165560) **Arlen22** reported that adding watchOptions to tsconfig.json and VSCode settings didn't fix the issue, and that enabling project diagnostics broke intellisense
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4230346939) **Arlen22** said "The experimental tsgo vscode plugin does not have any of these problems."
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-5121159127) **eeysudo** described a terminal-only TSServer hang fix for remote SSH/WSL2 with steps for WSL2 daemon reset, SSH verification, log capture, hang pattern identification, and kernel tweak

### [Issue microsoft/TypeScript#63672](https://github.com/microsoft/TypeScript/issues/63672) (Closed, `Working as Intended`)

**showConfig CLI option no longer shows all the compilation options**

*After updating to TypeScript 6.0.3, the CLI option --showConfig no longer displays default compiler options.*

 * created by **yohny**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63672#issuecomment-5094014249) **RyanCavanaugh** said "--showConfig intentionally doesn't show options which are not different from their defaults, and 6.0 changed the default values for the ones you see no longer listed."
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63672#issuecomment-5125329683) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63683](https://github.com/microsoft/TypeScript/issues/63683) (Closed, `Working as Intended`)

**Retain key type in \`Object\.entries\(\)\`**

*Enhance TypeScript’s lib.es2017 Object.entries definition to preserve specific object key types rather than generic strings.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63683#issuecomment-5096252862) **MartinJohns** said "Try searching for Object.keys in this repository. This has been rejected over and over again."
 * **RyanCavanaugh** added label `Working as Intended`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63683#issuecomment-5096497419) **RyanCavanaugh** said "entries is just keys + their values, so the same logic applies"
 * [today](https://github.com/microsoft/TypeScript/issues/63683#issuecomment-5125329550) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63683#issuecomment-5128142005) **nickshanks** challenged the suggestion and asked if the commenter had read their first line
 * [later](https://github.com/microsoft/TypeScript/issues/63683#issuecomment-5128151844) **nickshanks** suggested updating the issue text to mention Object.entries

### [PR microsoft/TypeScript#63689](https://github.com/microsoft/TypeScript/pull/63689) (Closed, `For Backlog Bug`)

**Gate ES2025 regex syntax \(duplicate named groups, pattern modifiers\) behind target**

*Gate duplicate named capturing groups and regex pattern modifiers behind the ES2025 target with corresponding errors and tests.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63689#issuecomment-5116430017) **sumukhl17-lgtm** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63689#issuecomment-5118257043) **MartinJohns** said "@sumukhl17-lgtm You implemented the change in the wrong repository. See https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md"
 * [today](https://github.com/microsoft/TypeScript/pull/63689#issuecomment-5120589284) **RyanCavanaugh** informed that the TypeScript repo was closed for development and directed the PR to the typescript-go repo referencing CONTRIBUTING.md and issue #62963
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63691](https://github.com/microsoft/TypeScript/issues/63691) (Open)

**JSDoc tag for getting around "Object literals are open\-ended"**

*Propose adding a JSDoc tag (e.g., @closed) to enforce exact object literal types in checked JavaScript files.*

 * created by **TheNamlessGuy**

### [Issue microsoft/TypeScript#63692](https://github.com/microsoft/TypeScript/issues/63692) (Closed)

**Putaek84/repository**

*Attachments Security_Modernization_Solution_Brief.pdf and gmail.com.txt failed to upload in the repository issue.*

 * created by **Putaek84**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63693](https://github.com/microsoft/TypeScript/issues/63693) (Open)

**Typescript 6\.0\.3升级到7\.0后报错**

*Upgrading TypeScript from 6.0.3 to 7.0 in VS2026 breaks compilation due to the removed 'target=ES5' option.*

 * created by **zlm166**

### [Issue microsoft/TypeScript#63694](https://github.com/microsoft/TypeScript/issues/63694) (Open)

**Assignability between distributive conditional types and their branch type is reversed in contravariant positions**

*TypeScript distributive conditional types incorrectly reverse assignability in contravariant positions.*

 * created by **ahmedajiz629**

### [Issue microsoft/TypeScript#63695](https://github.com/microsoft/TypeScript/issues/63695) (Open)

**Add support for \`@file\` jsdoc tag to describe a module**

*Support the JSDoc @file tag for module documentation in TypeScript and display descriptions in hover and autocomplete.*

 * created by **remcohaszing**

### [Issue microsoft/TypeScript#63696](https://github.com/microsoft/TypeScript/issues/63696) (Open)

**False positive on destructured \`require\` is \`verbatimModuleSyntax\` and \`module\` is \`preserve\`**

*TypeScript incorrectly rejects destructured CommonJS require calls when verbatimModuleSyntax is enabled and module is preserve.*

 * created by **remcohaszing**

