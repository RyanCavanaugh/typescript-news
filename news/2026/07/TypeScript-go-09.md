# Report for 2026-07-09 (Wednesday, July 8th, 2026)

21 different users commented on 26 different issues.

## Recommended Actions

 * Response Recommended
    * @parched provided repro steps and code in [microsoft/TypeScript-go#1057](https://github.com/microsoft/TypeScript-go/issues/1057#issuecomment-4919142288)
    * @GGomez99 provided instructions for how to build and run the PR in a yarn project in [microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4926997057)
    * @HolgerJeromin requested an updated NuGet package with TypeScript 7.0.2 and reported a build configuration bug in [microsoft/TypeScript-go#2310](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4923231836)
    * @dummdidumm asked whether content mappers can be asynchronous and influence LSP functionality such as diagnostics and rename behavior in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4924997952)
    * @remcohaszing provided detailed discussion and suggestions regarding diagnostics, config, and editor integration in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4925537831)
    * @AndrewMax asked for assistance after the workaround did not work in [microsoft/TypeScript-go#4567](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4926594165)
    * @AndrewMax asked for advice on resolving the Yarn-related issue in [microsoft/TypeScript-go#4567](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4927038067)

## Activity Summary

### [Issue microsoft/TypeScript-go#1057](https://github.com/microsoft/TypeScript-go/issues/1057) (Open, `Domain: Type Checking`, `Type Ordering`)

**Inconsistency involving discriminated union and flatMap**

*flatMap callback returning either InputOp[] or remove-only arrays causes a TypeScript discriminated union inference error*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1057#issuecomment-4218073370) **RyanCavanaugh** said "The linked PR didn't correctly implement the proposal"
 * (12 weeks ago) **RyanCavanaugh** unassigned **ahejlsberg**, **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1057#issuecomment-4919142288) **parched** provided a minimal repro showing TS2322 error under TS 7.0.2 when using flatMap with a union array after upgrading from TS 6 and noted it was fixed by adding a type annotation

### [Issue microsoft/TypeScript-go#1493](https://github.com/microsoft/TypeScript-go/issues/1493) (Open, `Domain: CLI`, **jakebailey**, **Copilot**)

**Exit code for type error is incorrect starting from \`7\.0\.0\-dev\.20250724\.1\`**

*tsgo in @typescript/native-preview@7.0.0-dev.20250724.1 returns exit code 1 for type errors instead of the expected code 2.*

 * (2 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`
 * (today) **jakebailey** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 Stable`

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open, `No linked issue`)

**Add Yarn PnP support**

*Add native Yarn Plug'n'Play support to TypeScript Go with VFS integration and manifest handling following PnP specification.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4707217638) **GGomez99** provided the full link to the linked issue and asked if it should be linked differently
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4709751672) **SerenModz21** suggested adding "Closes #460" to the PR description to properly link the issue and provided a documentation link
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4905614254) **proyectoramirez** said "What is a good way to try this PR in a yarn project?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4926997057) **GGomez99** suggested cloning the repository and following the How to build and run section of the contributing doc

### [Issue microsoft/TypeScript-go#2310](https://github.com/microsoft/TypeScript-go/issues/2310) (Open, `possible improvement`, **joj**)

**TypeScript for \.Net Projects**

*Custom MSBuild targets file and instructions to compile TypeScript 7 in .NET projects with tsgo until official support arrives.*

 * (14 weeks ago) **RyanCavanaugh** added label `possible improvement`, set milestone to `Possible Improvement`, and assigned to **joj**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4923231836) **HolgerJeromin** reported that the Microsoft.TypeScript.MSBuild 7.0.0-beta NuGet package worked but had a buggy TypeScript build configuration (missing module and target settings in TypeScriptProjectProperties.xaml), showed comparison images, and requested an updated package with TypeScript 7.0.2
 * [later](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4927037353) **joj** asked for more information about the setup and a build binlog, and explained the upcoming NuGet update and deprecated options

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4769881765) **shining-mind** explained that the HTML tag `my-card` resolves to the MyCard class with a typed `title` property and that binding validation requires TypeScript
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4769904119) **jakebailey** said "That isn't what I meant; if we have an API that can be accessed out-of-proc, you can ask for the type in opened files without being "inside" the process. Perhaps we are agreeing?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4769927814) **shining-mind** clarified that with an out-of-process API one could request types of opened files and expressed a desire to type-check HTML in tagged template literals with CLI support
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4919145963) **andrewbranch** organized the issue into two separate discussions and clarified what’s already shipping in the unstable API preview
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4924997952) **dummdidumm** asked whether content mappers can be asynchronous and influence LSP features such as diagnostics and rename functionality, or if a separate Svelte LSP is needed to intercept and modify requests
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4925537831) **remcohaszing** addressed unanswered questions about diagnostics mapping, transformer config reliance, TS emit scenarios, and editor integration, and proposed reading the bugs field from package.json and constraining commands to node_modules packages

### [Issue microsoft/TypeScript-go#4392](https://github.com/microsoft/TypeScript-go/issues/4392) (Open, `Crash`, **andrewbranch**)

**panic: cache entry not found \[recovered, repanicked\]**

*TypeScript server v7.0.0-dev panics with 'cache entry not found' while handling file open and config updates.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4392#issuecomment-4811067445) **RyanCavanaugh** said "@WerdoxDev thanks, confirmed this locally - the repro is contingent on opening mediasoup.ts + oxfmt.config.ts (I suspect any file from the repo root would do)"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4392#issuecomment-4811285902) **RyanCavanaugh** said "Foolishly I didn't save my entire log when I reprod it, and now I can't repro it again. @WerdoxDev can you share a full log file by chance?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4392#issuecomment-4811355785) **WerdoxDev** attached the complete crash log from today's usage
 * (today) **jakebailey** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 Stable`

### [PR microsoft/TypeScript-go#4416](https://github.com/microsoft/TypeScript-go/pull/4416) (Closed, `Voight-Kampff Anomaly`)

**Fix panic in checker\.GetTypeArguments for non\-reference types \(\#4338\)**

*Guard exported Checker.GetTypeArguments to return an empty slice for non-reference types instead of panicking.*

 * created by **UditDewan**
 * (2 weeks ago) **RyanCavanaugh** added label `Voight-Kampff Anomaly`, and set milestone to `Post-7.0`
 * (today) **UditDewan** closed the issue

### [PR microsoft/TypeScript-go#4449](https://github.com/microsoft/TypeScript-go/pull/4449) (Open)

**restore JSDoc member name check for private identifier references**

*Restores the JSDoc member name validation for private identifiers in isValidReferencePosition by implementing the missing helper.*

 * created by **aamoghS**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4805882923) **jakebailey** said "This needs tests that show this does something; it might not due to reparsing"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4906335658) **jakebailey** said "What is this for? You're making the baselines worse?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4917489457) **aamoghS** fixed the parser to retain private identifier nodes in JSDoc @see tags, tightened up isJSDocMemberName to avoid normal this.#x matches, updated the checker to resolve private identifiers, and refreshed the baselines

### [Issue microsoft/TypeScript-go#4461](https://github.com/microsoft/TypeScript-go/issues/4461) (Closed, `Needs Investigation`, **weswigham**)

**Behavior difference: Inconsistency when supplying \(internal\) expando function to another generic function call for exports**

*tsgo inconsistently omits .propTypes for memoized function components in .js and .tsx files compared to tsc*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch's pipeline analyzing 300 popular TypeScript repositories detected 11 interesting changes and encountered errors, timeouts, and cloning failures.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803487) **typescript-automation[bot]** reported that the server connection closed prematurely with undefined error and provided affected repo, logs, and repro steps
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803515) **typescript-automation[bot]** reported server connection closed prematurely with undefined error for mermaid-js/mermaid and provided log and replay command details
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803554) **typescript-automation[bot]** reported a panic during textDocument/rangeFormatting due to a debug failure
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [PR microsoft/TypeScript-go#4535](https://github.com/microsoft/TypeScript-go/pull/4535) (Closed, `Voight-Kampff Anomaly`)

**Emit expando properties for functions that only become visible late in declaration emit**

*Defer expando property assignment processing so properties on functions only marked visible late are correctly emitted.*

 * created by **UditDewan**
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4535#issuecomment-4918820170) **jakebailey** said "Will this need a backport, or is it fine to sit in 7.1?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4535#issuecomment-4918888371) **UditDewan** suggested considering a backport for a silent declaration emit regression in non-exported React components and offered to prepare a backport PR
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4562](https://github.com/microsoft/TypeScript-go/pull/4562) (Closed)

**Fix concurrent extractionCache read/write**

*Unprotected reads of the shared extractionCache during @types fallback conflict with concurrent worker writes in registryBuilder.updateIndexes, causing data races.*

 * created by **johnfav03**

### [Issue microsoft/TypeScript-go#4563](https://github.com/microsoft/TypeScript-go/issues/4563) (Closed)

**\`typescript@next\` dist\-tag points to 6\.0\.0\-dev, not a TS7 nightly, contradicting the TS7 announcement**

*The typescript@next dist-tag points to a 6.0.0-dev build instead of the expected TypeScript 7 nightly, contradicting the announced instructions.*

 * created by **alexander-vershinin**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4563#issuecomment-4917032812) **jakebailey** said "Yes, this is just one pipeline run away; I wanted to make sure the stable version was out before the next bit 😄 "
 * [today](https://github.com/microsoft/TypeScript-go/issues/4563#issuecomment-4917178651) **jakebailey** reported that the issue was resolved and showed npm info output for typescript@next
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4563#issuecomment-4917212472) **alexander-vershinin** said "@jakebailey sorry about that :), I couldn't wait to try it"

### [PR microsoft/TypeScript-go#4564](https://github.com/microsoft/TypeScript-go/pull/4564) (Open)

**Add native\-preview API: getSourceFiles, TypeParameter getters, StructuredType, TupleTypeReference, inferredProjectName**

*Add Program.getSourceFiles, TypeParameter.getConstraint/getDefault, StructuredType, TupleTypeReference, and inferredProjectName to the native-preview API.*

 * created by **aamoghS**

### [PR microsoft/TypeScript-go#4565](https://github.com/microsoft/TypeScript-go/pull/4565) (Open)

**Fix stack overflow in \`checkTypeExpandability\(\)\`**

*checkTypeExpandability fails to track reference type arguments, causing infinite recursion and stack overflow*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#4566](https://github.com/microsoft/TypeScript-go/pull/4566) (Open)

**Use published packages for stable releases**

*Pull prebuilt npm packages in the release branch instead of rebuilding them to work around npm's platform limitations.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#4567](https://github.com/microsoft/TypeScript-go/issues/4567) (Closed)

**\`tsc\` incorrectly points to v6 rather than v7**

*The npm alias setup for TypeScript 6 and 7 side-by-side assigns the tsc binary to version 6 instead of 7.*

 * created by **abrahamguo**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4919083741) **RyanCavanaugh** explained that npm picks bin winners based on lexical sort, provided a working alias configuration, and noted that the blog would be fixed
 * [later](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4926594165) **AndrewMax** reported that the suggested config still didn't work and asked @RyanCavanaugh for help
 * [later](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4926910710) **RyanCavanaugh** said "@AndrewMax which package manager, and which version, are you running?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4927038067) **AndrewMax** specified package manager as Yarn Berry 4.17.1 and asked for advice on resolving the Yarn-related issue

### [PR microsoft/TypeScript-go#4568](https://github.com/microsoft/TypeScript-go/pull/4568) (Closed)

**Native Yarn Plug'n'Play module resolution**

*Enable TypeScript to natively resolve modules via Yarn Plug’n’Play manifests and zip archives.*

 * created by **ejc3**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4568#issuecomment-4919533417) **jakebailey** noted that PR #1966 already existed and questioned the need for a second PR without specific improvements or group effort
 * [today](https://github.com/microsoft/TypeScript-go/pull/4568#issuecomment-4919564445) **ejc3** acknowledged not reviewing existing pull requests and said they would check for missing edge cases
 * [today](https://github.com/microsoft/TypeScript-go/pull/4568#issuecomment-4919683876) **ejc3** acknowledged the duplicate, closed the PR, and extracted the useful part into a small PR against #1966's branch, enabling additional test cases and fixing two bugs
 * (today) **ejc3** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4568#issuecomment-4919694750) **ejc3** described the test-coverage and fixes PR against #1966's branch, mentioning removal of the limiting conditional in TestResolveUnqualified and fixes for fallback-pool aliases and ignorePatternData importer behavior
 * [today](https://github.com/microsoft/TypeScript-go/pull/4568#issuecomment-4919700017) **ejc3** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#4569](https://github.com/microsoft/TypeScript-go/pull/4569) (Closed)

**Fix more return types that can’t actually be undefined**

*Remove undefined from client-defined return types of several methods that cannot actually be undefined.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4570](https://github.com/microsoft/TypeScript-go/pull/4570) (Closed, **andrewbranch**, **Copilot**)

**Resolving unchecked assertion in parseProjectReference**

*Replace unchecked assertion in parseProjectReference with explicit validation to prevent runtime errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [Issue microsoft/TypeScript-go#4571](https://github.com/microsoft/TypeScript-go/issues/4571) (Open, `Domain: Editor`)

**Organize imports command doesn't respect tabSize/insertSpaces settings**

*Organize imports always uses a four-space indent for multiline named imports instead of honoring tabSize and insertSpaces settings*

 * created by **davidkarlsson**
 * **davidkarlsson** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#4572](https://github.com/microsoft/TypeScript-go/issues/4572) (Open)

**Overloaded assertion in inferred\-return function expression loses destructured discriminant narrowing**

*An overloaded assert in an arrow function without a return type annotation prevents TypeScript from narrowing a destructured discriminant property.*

 * created by **adri1wald**

### [Issue microsoft/TypeScript-go#4573](https://github.com/microsoft/TypeScript-go/issues/4573) (Open)

**Add ability to get emit output from the API**

*Enable TypeScript API's program.emit to return JS, declaration, and source map outputs for multiple files in one call.*

 * created by **dragomirtitian**

### [PR microsoft/TypeScript-go#4574](https://github.com/microsoft/TypeScript-go/pull/4574) (Open)

**Add ability to get emit output from the API**

*Add an API feature that allows users to programmatically retrieve emitted output.*

 * created by **dragomirtitian**

### [PR microsoft/TypeScript-go#4575](https://github.com/microsoft/TypeScript-go/pull/4575) (Open)

**Create Workspace**

*Request to create a new workspace named Abmc.*

 * created by **leonelmateopucperez05-sudo**

