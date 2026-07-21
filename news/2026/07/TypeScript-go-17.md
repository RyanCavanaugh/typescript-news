# Report for 2026-07-17 (Friday, July 17th, 2026)

6 different users commented on 25 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] reported a panic during hover request in [microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527132)
    * @typescript-automation[bot] reported a server connection error with repro steps in [microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527171)
    * @typescript-automation[bot] reported server connection closed prematurely error in [microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527206)
    * @typescript-automation[bot] reported server connection closed prematurely with repro steps provided in [microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527265)
    * @typescript-automation[bot] reported a server connection closed prematurely error and provided repro steps in [microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527319)
    * @typescript-automation[bot] reported a server connection closed prematurely: undefined in [microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527371)
    * @typescript-automation[bot] reported a server connection closed prematurely error in [microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527438)
    * @typescript-automation[bot] reported server connection closed prematurely for freeCodeCamp/freeCodeCamp in [microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527499)

## Activity Summary

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4991793665) **shining-mind** agreed and asked whether there were plans to create a dedicated feature request for CLI support for typechecking Vue, Svelte, and string template literals
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4994605079) **andrewbranch** said "https://github.com/microsoft/typescript/issues/45886 is basically that."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5004116575) **shining-mind** asked if the proposal should be moved to the typescript-go repo
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5005913332) **andrewbranch** said "No, development will move back to microsoft/TypeScript soon and typescript-go will be archived."

### [PR microsoft/TypeScript-go#3726](https://github.com/microsoft/TypeScript-go/pull/3726) (Open, **DanielRosenwasser**, **Copilot**)

**Preserve original stack traces in cross\-project panic handling**

*Wrap panics in PanicWithStack to capture and propagate original stack traces for cross-project panic handling.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4392475333) **Copilot** fixed NewPanicWithStack to strip recovery infrastructure frames from the captured stack to prevent duplication in telemetry output
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4652511528) **RyanCavanaugh** said "@copilot address the merge conflicts"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-5005763801) **RyanCavanaugh** said "Just doing some Copilot testing here, please ignore reviews"

### [Issue microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520) (Open, `Domain: Editor`)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*Enabling the TypeScript Native Preview extension in an empty folder without package.json causes a persistent memory leak until VS Code is closed.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4869357111) **KostyaTretyak** clarified that adding a default package.json with npm init -y prevented the memory leak and suggested a nearby service might be scanning git repositories
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4869534469) **KostyaTretyak** confirmed no memory leak when moving folder to a directory without other git repositories and suggested a service might misdetect neighboring repositories as part of the monorepo
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4952534039) **Skykill** reported that their three.js case reproduced with a minimal CLI setup, filed issue #4612 with repro steps and analysis, and suggested cross-linking due to a potential common underlying cause
 * **RyanCavanaugh** added to milestone `Need More Info`

### [Issue microsoft/TypeScript-go#4525](https://github.com/microsoft/TypeScript-go/issues/4525) (Open, `Needs Investigation`, **weswigham**)

**Follow\-up on issues/4254: \`typeof\` emit does not happen in \`export const { \.\.\. } = default\`**

*tsgo’s declaration emitter incorrectly inlines function signatures instead of using typeof when destructuring and exporting properties from a default export.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4528](https://github.com/microsoft/TypeScript-go/issues/4528) (Closed, `Domain: Type Checking`, `Type Ordering`)

**tsgo appears to loop until OOM on three/tsl Fn callback that TypeScript accepts**

*tsgo enters an infinite type-checking loop and exhausts memory when processing a three/tsl Fn callback that tsc accepts*

 * (2 weeks ago) **ahejlsberg** added labels `Domain: Type Checking`, `Type Ordering`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4528#issuecomment-4879046574) **ahejlsberg** suggested refactoring Node<TNodeType> into a NodeExtras mapping with specific extensions per type
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch's pipeline analyzing 300 popular TypeScript repositories detected 11 interesting changes and encountered errors, timeouts, and cloning failures.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803554) **typescript-automation[bot]** reported a panic during textDocument/rangeFormatting due to a debug failure
 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`

### [Issue microsoft/TypeScript-go#4560](https://github.com/microsoft/TypeScript-go/issues/4560) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Extension does not follow symlinks when resolving the tsdk path \(breaks pnpm virtual store\)**

*TypeScript native-preview extension ignores pnpm tsdk symlinks, fails to locate platform binary, and falls back to the bundled version.*

 * **ya-woodcutter** added label `Domain: Editor`
 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`

### [Issue microsoft/TypeScript-go#4571](https://github.com/microsoft/TypeScript-go/issues/4571) (Open, `Domain: Editor`, **RyanCavanaugh**, **Copilot**)

**Organize imports command doesn't respect tabSize/insertSpaces settings**

*Organize imports always uses a four-space indent for multiline named imports instead of honoring tabSize and insertSpaces settings*

 * created by **davidkarlsson**
 * **davidkarlsson** added label `Domain: Editor`
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4580](https://github.com/microsoft/TypeScript-go/issues/4580) (Closed, `Domain: Editor`)

**TS7 plugin is not working with Yarn 4 nodeLinker = pnp**

*TS7’s VSCode plugin and compiler fail to work with Yarn 4 PnP due to missing tsserver and inaccessible cached archives.*

 * created by **zuyetawarmatik**
 * **zuyetawarmatik** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Need More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4580#issuecomment-5007287838) **RyanCavanaugh** said ""uses Yarn 4" is not enough info to go on - we really need a concrete repro to investigate."

### [PR microsoft/TypeScript-go#4586](https://github.com/microsoft/TypeScript-go/pull/4586) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix TS2871 false positive for \`??\` operator in nullish coalescing check**

*Modify getSyntacticNullishnessSemantics to separate '??' and '??=' semantics from right controls and eliminate TS2871 false positives.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4586#issuecomment-4937552329) **RyanCavanaugh** said "This is a fix for https://github.com/microsoft/TypeScript/issues/63642"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4586#issuecomment-4937619051) **Copilot** replaced the test case with the minimal repro from the issue comment and updated baselines
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601) (Open, `bug`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*Server errors were reported on the main TypeScript branch during an Azure pipeline run analyzing 300 popular GitHub repositories.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940321025) **typescript-automation[bot]** reported a server connection closed prematurely error for strapi/strapi
 * (2 days ago) **RyanCavanaugh** added label `bug`, and assigned to **johnfav03**
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`

### [Issue microsoft/TypeScript-go#4616](https://github.com/microsoft/TypeScript-go/issues/4616) (Closed, `bug`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Behavior difference: declaration emit synthesizes extensionless \`import\(\)\` specifier under \`allowImportingTsExtensions\`, invalid in nodenext**

*Using allowImportingTsExtensions with module nodenext, tsgo's declaration emit drops file extensions, producing invalid import() specifiers.*

 * (2 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4657](https://github.com/microsoft/TypeScript-go/pull/4657) (Closed)

**Add even more bails on unchecked identifiers to markLinkedReferences**

*Continue adding bail checks for unchecked identifiers in markLinkedReferences to address remaining diffs*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4659](https://github.com/microsoft/TypeScript-go/pull/4659) (Closed)

**Move baselines mistakenly put into TS\-1 group without TS\-1 into accepted**

*Remove trio of diffs mistakenly assigned to the TS-1 group despite lacking TS-1 consistency diagnostics.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4662](https://github.com/microsoft/TypeScript-go/pull/4662) (Closed)

**Fix declaration emit synthesizing extensionless import\(\) specifier under allowImportingTsExtensions \+ nodenext**

*Declaration emit under allowImportingTsExtensions and nodenext stripped .js extensions from import() specifiers, causing TS2307 errors.*

 * created by **RyanCavanaugh**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4662#issuecomment-4997405723) **RyanCavanaugh** said "This is a redo of https://github.com/microsoft/typescript-go/pull/4649 but now GitHub API is down 🙁"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4666](https://github.com/microsoft/TypeScript-go/pull/4666) (Open, `Voight-Kampff Anomaly`)

**POC: ambient module declarations keyed on import attributes**

*Proof-of-concept for ambient module declarations keyed by import attributes to support text or bytes file imports in TypeScript's Go port.*

 * created by **bartlomieju**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4666#issuecomment-5004893772) **bartlomieju** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [PR microsoft/TypeScript-go#4667](https://github.com/microsoft/TypeScript-go/pull/4667) (Open, **RyanCavanaugh**, **Copilot**)

**Copilot test PR, do not merge**

*Change 'are subject' to 'is subject' for correct singular subject-verb agreement with 'any use'.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4667#issuecomment-5005824257) **sandersn** said "@copilot Make an additional correction"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4667#issuecomment-5005854778) **Copilot** fixed plural possessive in README.md trademarks section

### [PR microsoft/TypeScript-go#4668](https://github.com/microsoft/TypeScript-go/pull/4668) (Open, **RyanCavanaugh**, **Copilot**)

**Respect editor tab/space settings when parsing formatting prefs used by organize imports**

*Map editor tabSize and insertSpaces settings to formatting indentSize and convertTabsToSpaces so organizeImports honors editor indentation preferences.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch error-delta pipeline tested 300 repositories, analyzing 198, reporting 10 interesting changes, 188 unchanged, and various failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527132) **typescript-automation[bot]** reported a panic during hover request with debug failure and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527171) **typescript-automation[bot]** reported that the server connection closed prematurely with an undefined error for slopus/happy and provided error artifacts, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527206) **typescript-automation[bot]** reported a premature server connection closure error with repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527265) **typescript-automation[bot]** reported server connection closed prematurely for sequelize/sequelize and provided error details, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527319) **typescript-automation[bot]** reported a server connection closed prematurely error for AdGuardHome with logs and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527371) **typescript-automation[bot]** reported a premature server connection closure with undefined error for babel/babel and included logs, request history, and partial repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527438) **typescript-automation[bot]** reported that the server connection closed prematurely with undefined while processing nuxt/nuxt
 * [today](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527499) **typescript-automation[bot]** reported server connection closed prematurely error with affected repos, old server result, last requests, and repro steps

### [PR microsoft/TypeScript-go#4670](https://github.com/microsoft/TypeScript-go/pull/4670) (Open, `dependencies`, `javascript`)

**Bump adm\-zip from 0\.5\.17 to 0\.6\.0**

*Bump adm-zip from 0.5.17 to 0.6.0 to fix CVE-2026-39244, resolve bugs, add TypeScript types, and improve extraction behavior.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

