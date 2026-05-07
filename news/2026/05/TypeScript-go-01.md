# Report for 2026-05-01 (Friday, May 1st, 2026)

12 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @purelualight requested a review from @gabritto in [microsoft/TypeScript-go#3528](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4360385161)
    * @Raynos reported that the same issue occurred in cursor in [microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4361443953)
    * @Withered-Flower-0422 reported that the emitted .d.ts files differ between TypeScript 6.0 and tsgo and provided examples in [microsoft/TypeScript-go#3686](https://github.com/microsoft/TypeScript-go/issues/3686#issuecomment-4363259768)

## Activity Summary

### [Issue microsoft/TypeScript-go#3318](https://github.com/microsoft/TypeScript-go/issues/3318) (Open, `Domain: Editor`, **iisaduan**)

**Missing \`addMissingImports\` code action/code fix**

*VSCode’s editor.codeActionOnSave lacks implementation of TypeScript’s addMissingImports code action and code fix.*

 * **iisaduan** assigned to **iisaduan**
 * (2 weeks ago) **RyanCavanaugh** added label `Domain: Editor`, and set milestone to `Post-7.0`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4364081565) **dhoulb** said "Have become so reliant on this it might force me back to the non-experimental extension for now."

### [PR microsoft/TypeScript-go#3528](https://github.com/microsoft/TypeScript-go/pull/3528) (Open)

**chore: fix some minor issues in comments**

*Fix minor typos and inconsistencies in code comments.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4306110575) **purelualight** said "@microsoft-github-policy-service agree"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4306115325) **purelualight** quoted the Contributor License Agreement and provided instructions on how to agree with it
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4306116514) **purelualight** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4360385161) **purelualight** said "@gabritto Hi, Could you please review this PR at your convenience? Thank you very much."

### [Issue microsoft/TypeScript-go#3552](https://github.com/microsoft/TypeScript-go/issues/3552) (Open, `Domain: Declaration Emit`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Baselines: export = a reordered; ESM side\-effect import replaces export {}**

*Baseline diffs indicate that CommonJS export assignments are reordered after declarations and empty ES exports are replaced by side-effect imports.*

 * (4 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4361735218) **andrewbranch** acknowledged that JS elision behavior was unique to the Strada JS declaration emitter and suggested standardizing on the TS emitter, possibly marking the issue as wontfix

### [Issue microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621) (Open, `Crash`, `Needs More Info`)

**Panic Alert Notification when Cursor edits some file and opening that file causes panic\.**

*Opening or editing a file causes a panic in the semanticTokens request because a token improperly spans multiple lines.*

 * created by **RealHaris**
 * **RealHaris** added label `Crash`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4342371254) **Swiftwork** said "Observing same issue for the last 1-2 weeks"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4361443953) **Raynos** said "Observing same issue in cursor too."

### [Issue microsoft/TypeScript-go#3645](https://github.com/microsoft/TypeScript-go/issues/3645) (Open, `Domain: Editor`, `Crash`, **andrewbranch**, **Copilot**)

**Auto\-imports for JSX tag trigger assertion violation when React is type\-imported\.**

*Automatic JSX tag imports crash with an assertion violation when React is imported only as a type*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3645#issuecomment-4339305888) **DanielRosenwasser** suggested applying the promotion from type-only to regular import for returned names and falling back to usual auto-import logic when that fails
 * (3 days ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **andrewbranch**, and unassigned **DanielRosenwasser**
 * (today) **andrewbranch** added labels `Domain: Editor`, `Crash`, and set milestone to `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3650](https://github.com/microsoft/TypeScript-go/pull/3650) (Open, **DanielRosenwasser**, **Copilot**)

**Fix assertion violation in auto\-imports for JSX tag when React is type\-imported**

*Refactor symbol import logic to handle type-only React imports and prevent JSX auto-import assertion failures.*

 * (3 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4339635488) **DanielRosenwasser** asked if each fix was discrete and could be combined and noted that `isJsxNamespaceFix` was never set
 * [today](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4360709862) **andrewbranch** said "@copilot ^"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4360778682) **Copilot** explained why multiple symbol names appeared from getSymbolNamesToImport, described the simplification in revision 8134793 to return only a single promotion fix, and confirmed that isJsxNamespaceFix remained unset
 * [today](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4361646191) **andrewbranch** said "@copilot ^"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4361828952) **andrewbranch** suggested modifying getSymbolNamesToImport to return richer info and described handling of type-only imports to avoid duplicates or improve correlation
 * [today](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4361891178) **Copilot** refactored getSymbolNamesToImport to return symbolNameInfo with name and isTypeOnly fields, adjusted type-only and auto-import filters, reverted needsJsxNamespaceFix, and included component name when type-only

### [Issue microsoft/TypeScript-go#3667](https://github.com/microsoft/TypeScript-go/issues/3667) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Assigning array to uninitialized class members yields different error on tsc & tsgo**

*Assigning arrays to uninitialized class members in JavaScript triggers different implicit any and type inference errors in tsc vs tsgo.*

 * (today) **ahejlsberg** added labels `bug`, `Domain: Type Checking`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3667#issuecomment-4359947311) **ahejlsberg** noted that Strada handled self-referential this.xxx assignments and suggested porting that code while ignoring such assignments instead of typing them as any
 * [today](https://github.com/microsoft/TypeScript-go/issues/3667#issuecomment-4360528679) **ahejlsberg** described that the differing type for `this.bar` was due to a JavaScript-specific rule about empty array literals being typed as `any[]`
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3668](https://github.com/microsoft/TypeScript-go/issues/3668) (Open, `Domain: Editor`, **johnfav03**)

**Enable/Disable Native Preview commands don't work when user & workspace settings are both configured**

*Disabling native preview with conflicting user and workspace js/ts.experimental.useTsgo settings ignores workspace override, causing duplicate results and no enable command.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Domain: Editor`, set milestone to `TypeScript 7.0 RC`, and assigned to **johnfav03**

### [PR microsoft/TypeScript-go#3675](https://github.com/microsoft/TypeScript-go/pull/3675) (Closed)

**Port experimentation service and reporting to extension**

*Port the experimentation service and integrate its reporting capabilities into the extension.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3676](https://github.com/microsoft/TypeScript-go/issues/3676) (Open, **gabritto**)

**tsconfig diagnostics not refreshed if no TS/JS files are open**

*Diagnostic errors for a removed 'baseUrl' option in tsconfig.json fail to clear when no TS or JS files are open.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3676#issuecomment-4360644660) **DanielRosenwasser** said "I'm not sure if there really is a great fix here given how pull diagnostics works, but I think it's worth investigating here."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3676#issuecomment-4360656283) **DanielRosenwasser** said "Maybe we can do something custom with our extension's client when a config file changes?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3676#issuecomment-4360821353) **jakebailey** recommended pushing an empty diagnostic set when a project became unreferenced after all files were closed

### [PR microsoft/TypeScript-go#3677](https://github.com/microsoft/TypeScript-go/pull/3677) (Closed)

**Remove redundant work from polling watcher**

*Reduce tsgo --watch CPU usage by eliminating redundant directory hashing and state iteration and doubling the polling interval.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3679](https://github.com/microsoft/TypeScript-go/issues/3679) (Closed)

**\[ServerErrors\]\[JavaScript\] main vs **

*The main pipeline analyzed JavaScript errors across 300 TypeScript repositories, successfully processing 255 and reporting 7 changes, timeouts, and failures.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3679#issuecomment-4361805001) **typescript-bot** reported that the server connection closed prematurely and provided error details, last requests, and repro steps for BoostIO/BoostNote-Legacy

### [PR microsoft/TypeScript-go#3680](https://github.com/microsoft/TypeScript-go/pull/3680) (Closed)

**Port JS specific code for \`this\.xxx\` assignment declaration typing**

*Port JavaScript-specific code to provide proper typing support for this.xxx assignment declarations.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3681](https://github.com/microsoft/TypeScript-go/issues/3681) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main TypeScript branch’s Azure pipeline run on 300 popular GitHub repositories encountered server errors, clone failures, and timeouts.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138714) **typescript-bot** reported a panic due to a debug assertion failure in textDocument/formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138743) **typescript-bot** reported a panic in textDocument/formatting due to a failed debug assertion
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138762) **typescript-bot** reported a panic handling request textDocument/formatting due to a debug failure 'False expression: Token end is child end' and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138790) **typescript-bot** reported debug failure on textDocument/rangeFormatting due to false expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138819) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138850) **typescript-bot** reported a server connection closed prematurely error for elastic/kibana and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138875) **typescript-bot** reported that the server connection closed prematurely with undefined
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138906) **typescript-bot** reported that the server connection closed prematurely with an undefined error and provided affected repo details, request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138944) **typescript-bot** described a premature server connection closure error for the payloadcms/payload repo, listed related requests and provided reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138979) **typescript-bot** reported server connection closed prematurely error for cypress-io/cypress and shared logs, request details, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362139013) **typescript-bot** reported server connection closed prematurely error and provided logs and repro steps for n8n-io/n8n

### [Issue microsoft/TypeScript-go#3682](https://github.com/microsoft/TypeScript-go/issues/3682) (Closed, `wontfix`)

**Behavior difference: Assigning static field outside class definition gives TS7005 in tsc but gives TS7008 in tsgo**

*Assigning a static field outside a class triggers TS7005 in tsc but TS7008 in tsgo.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3682#issuecomment-4364020807) **ahejlsberg** stated that Strada incorrectly tagged expando properties as variables and that the Corsa terminology was more correct, so no fix was needed
 * **ahejlsberg** added label `wontfix`

### [Issue microsoft/TypeScript-go#3683](https://github.com/microsoft/TypeScript-go/issues/3683) (Closed, `wontfix`)

**Behavior difference: jsdoc \`@readonly\` placed on class getter gives error on tsgo but not in tsc**

*Applying jsdoc @readonly to a class getter produces no error with tsc but triggers a TS1024 error in tsgo.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3683#issuecomment-4364015917) **ahejlsberg** said "This definitely seems like a reasonable diagnostic. I don't think we want to change anything here."
 * **ahejlsberg** added label `wontfix`

### [PR microsoft/TypeScript-go#3684](https://github.com/microsoft/TypeScript-go/pull/3684) (Closed)

**ls/semantictokens: skip multi\-line tokens instead of panicking**

*Skip multi-line LSP semantic tokens in the language server to avoid panics.*

 * created by **SAY-5**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3684#issuecomment-4363050752) **jakebailey** critiqued the proposed fix for masking the root cause and requested adding a reproducing test after #3483

### [PR microsoft/TypeScript-go#3685](https://github.com/microsoft/TypeScript-go/pull/3685) (Closed)

**Fix flake in TestRegistryLifecycle pnpm\-style symlink test**

*Intermittent failure of TestRegistryLifecycle’s pnpm-style symlinks test due to bucket not marked dirty after package change*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3686](https://github.com/microsoft/TypeScript-go/issues/3686) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Unnecessary declaration in \.d\.ts**

*tsgo emits declarations for a non-exported function and its namespace in the .d.ts file that should be omitted.*

 * created by **Withered-Flower-0422**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3686#issuecomment-4363259768) **Withered-Flower-0422** demonstrated that the emitted .d.ts files differed between TypeScript 6.0 and tsgo for an exported function with a property

