# Report for 2025-12-14 (Sunday, December 14th, 2025)

22 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @Knagis reported that tsgo hung with large commit size and could not be terminated via task manager in [microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3654358600)
    * @longzheng provided repro steps as requested in [microsoft/TypeScript-go#1708](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3652337668)
    * @PaulRBerg reported that the issue still occurs in the latest version and forces him to restart the language server more than 10 times per day in [microsoft/TypeScript-go#2133](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3656242346)
    * @dalisoft provided a reproduction monorepo link in [microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3655512275)
    * @joaotavora reported that tsgo LSP doesn't support relatedDocumentSupport for diagnostics in [microsoft/TypeScript-go#2362](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3652274978)
    * @xxxxue confirmed that building from source fixed the bug in [microsoft/TypeScript-go#2375](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3653890130)
    * @jasonlyu123 suggested adding official support for custom file extensions and expanding LSP integration options in [microsoft/TypeScript-go#648](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3655911105)

## Activity Summary

### [PR microsoft/TypeScript-go#1556](https://github.com/microsoft/TypeScript-go/pull/1556) (Closed)

**fix: improve panic message for unspecified ScriptKind in \`Parser::initializeState\`**

*Enhance the panic message in Parser::initializeState to include the filename when ScriptKind is unknown for easier debugging*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1556#issuecomment-3175792209) **camc314** noted that many panics include extra debugging info, provided counts of total panics and formatted panics, and asked if telemetry could match only the first part of the panic string
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1556#issuecomment-3175851583) **jakebailey** pointed out that searching for just prints in panics isn't sufficient and mentioned that there is no current API, warning that usage comes without warranty and isn't optimized for external use
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/1556#issuecomment-3630516495) **jakebailey** said "Honestly, I think we can just take this; NewSourceFile already panics with a filename. I would just merge from main, however."
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Open, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647019868) **Knagis** reported performance metrics and observations for tsgo 7.0.0-dev.20251212.1 using different builder configurations
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647062740) **jakebailey** said "Is this codebase public? That definitely sounds like the opposite of how it should behave."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647124648) **Knagis** suggested using an NDA path to share the private codebase and described its structure as React TSX files, Jest and Playwright specs, declaration-only emits, with few symlinks and path aliases
 * [later](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3654358600) **Knagis** reported that running tsgo with specified flags resulted in a 30GB commit, hung, and could not be killed via task manager

### [Issue microsoft/TypeScript-go#1708](https://github.com/microsoft/TypeScript-go/issues/1708) (Open, `Domain: Editor`)

**tsgo preview: import suggestions are not aware of paths**

*tsgo preview in Zed lacks path-aware import suggestions provided by vtsls, making it unusable.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3390528659) **jakebailey** said "That is unrelated; please file a new issue with a repro."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3647571345) **marioparaschiv** said "What's the priority on user preferences for the LSP? "
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3647674267) **jakebailey** asked about the priority and requested repro steps if the issue persisted
 * [today](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3652337668) **longzheng** reproduced the issue after the latest changes in #1793 and extension version 0.20251214.1 and provided a reproduction project with relevant configuration

### [PR microsoft/TypeScript-go#1808](https://github.com/microsoft/TypeScript-go/pull/1808) (Closed)

**Add option for overriding \`GOMEMLIMIT\`**

*Provide a configuration option to override the GOMEMLIMIT environment variable.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/1808#issuecomment-3648125290) **jakebailey** expressed desire to merge the changes to enable testing and noted that a merge from main was required
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/1808#issuecomment-3648129981) **maschwenk** said "@jakebailey on it!"
 * (yesterday) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/1808#issuecomment-3656099158) **maschwenk** described testing that increasing the memory option increased usage and suggested moving the code into a server-side user preference

### [PR microsoft/TypeScript-go#1947](https://github.com/microsoft/TypeScript-go/pull/1947) (Open)

**fix: panic in \`regexp\.MustCompile\` when building wildcarddirectories with non ascii characters**

*Handle non-ASCII characters in wildcard directory patterns to prevent regexp.MustCompile panics.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3446588651) **camc314** clarified intent to revert the previous commit, explained the necessity of escaping for GetRegularExpressionForWildcard, and updated wildcarddirectories to use regexp2
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3446876374) **jakebailey** said "Why does Strada not need the escaping change, though?"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3630513577) **jakebailey** said "Honestly, this PR is probably fine. It would be good to make a test that would have crashed before. But, I would like to have this change upstreamed."
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3655915844) **camc314** explained that getWildcardDirectories produced invalid regex escapes from Windows file paths containing non-ASCII characters, causing a panic, and noted that percent-encoded paths avoid the issue

### [Issue microsoft/TypeScript-go#2133](https://github.com/microsoft/TypeScript-go/issues/2133) (Open, `Domain: Editor`)

**Renaming a file results in mis\-identifying the right sconfig file**

*Renaming a .spec.ts file in VSCode makes editor apply the base tsconfig instead of the local one, causing persistent errors.*

 * **lukpsaxo** added label `Domain: Editor`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3557108039) **lukpsaxo** shared relevant log snippet showing cache statistics and project configuration steps
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3557143441) **lukpsaxo** provided the same log after restarting tsgo
 * [later](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3656242346) **PaulRBerg** reported that the issue persisted in the latest version and forced frequent language server restarts

### [Issue microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189) (Open, `Domain: Editor`, **andrewbranch**)

**LSP doesn't offer auto\-importing packages**

*VS Code’s TypeScript LSP does not offer auto-import suggestions for installed packages like `typescript-result`, only built-in modules*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3623465376) **kieranm** said "We are seeing a bit of slowness with import suggestions right now too. We have a pnpm monorepo which is closed source but we can give access privately if volunteers are needed!"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3627394893) **andrewbranch** said "@kieranm that would be great! If you need an email for me, you can use my first name dot last name @microsoft.com."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3629567310) **rubnogueira** reproduced the issue in a monorepo with PNPM where imports were suggested on Ctrl + Space but not inserted until restarting the IDE
 * [later](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3655512275) **dalisoft** said "Same problem. You can check with this monorepo https://github.com/dalisoft/airlight"

### [PR microsoft/TypeScript-go#2343](https://github.com/microsoft/TypeScript-go/pull/2343) (Closed)

**\-\-experimentalDecorators and \-\-emitDecoratorMetadata**

*Implement decorator and metadata emit flags in TypeScript-Go, resolve sourcemap test mismatches, and review pending feature emits.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3645640415) **weswigham** clarified that the removal of !!! emitDecoratorMetadata had already occurred and was replaced by an error requiring emitDecoratorMetadata alongside experimentalDecorators
 * (2 days ago) **weswigham** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3647587892) **jycouet** said "Great news 🎉"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3654517076) **mlarabi** said "I am so happy to see this PR. I now know what to experiment this night. Thank you @weswigham and everyone involved for the work done."

### [Issue microsoft/TypeScript-go#2362](https://github.com/microsoft/TypeScript-go/issues/2362) (Open)

**LSP diagnostics not working in Emacs's eglot**

*tsgo LSP server fails to publish diagnostics to Emacs’s eglot unlike typescript-language-server, possibly due to client capabilities mismatch.*

 * created by **edkolev**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3647016225) **jakebailey** noted that only pull diagnostics are supported and asked whether eglot supports push diagnostics
 * [today](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3652274978) **joaotavora** reported that tsgo LSP implementation does not provide diagnostics for related documents via relatedDocumentSupport
 * [today](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3652555217) **jakebailey** compared the new language server’s diagnostic behavior to tsserver, noting it only showed diagnostics for opened files and referenced issue #2169 for unopened files
 * [later](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3654617423) **joaotavora** explained that he had two open documents and expected the language server to maintain a dependency graph for diagnostic pulls, criticized VSCode's approach as inefficient, and noted having long ago left JavaScript land

### [Issue microsoft/TypeScript-go#2366](https://github.com/microsoft/TypeScript-go/issues/2366) (Open)

**Diagnostics not shown in file peek views**

*Reference peek views in TypeScript no longer display diagnostics such as deprecation warnings across files.*

 * created by **mjbvz**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3648002251) **jakebailey** said "We don't control this; is VS Code / the LSP client not opening that file and asking for diagnostics?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3648014391) **mjbvz** said "Yes maybe an lsp issue? cc @dbaeumer "
 * [later](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3654930647) **dbaeumer** assumed the new TS extension used pull diagnostics, noted that VS Code did not represent peek view editors in the tab model, and asked if there was a way to detect peek editor tabs
 * [later](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3655002832) **jakebailey** stated that they currently exclusively used pull diagnostic as tsserver did before and suggested that the TS extension’s error requests may have already solved the issue

### [Issue microsoft/TypeScript-go#2375](https://github.com/microsoft/TypeScript-go/issues/2375) (Open, `Domain: Editor`)

**panic: bundled: failed to evaluate symlinks: The system cannot find the path specified\. \[recovered, repanicked\]**

*Setting typescript.experimental.useTsgo in VS Code on Windows causes a panic in the TypeScript-Go bundle due to failed symlink resolution.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3649778536) **jakebailey** said "Can you provide more info about your system? Are all of your files living within a symlink somehow?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3649823930) **fooooooooooooooo** reported the same error when evaluating symlinks on a scoop-installed VS Code data directory and included Go code and panic output
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3650321936) **xxxxue** described linking D:\UserDir\admin to C:\Users\admin via a directory symlink and noted that moving main.exe out of the symlinked directory allowed the code to run successfully
 * [today](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3651779644) **jakebailey** said "If you're able to build from source, can you try https://github.com/microsoft/typescript-go/pull/2381? Theoretically you could just swap the binary into where your extension lives."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2375#issuecomment-3653890130) **xxxxue** reported that they downloaded and compiled the source code and confirmed the bug was fixed and tsgo now worked

### [PR microsoft/TypeScript-go#2376](https://github.com/microsoft/TypeScript-go/pull/2376) (Closed)

**Fix \`isPropertyDeclaredInAncestorClass\` function**

*Revise the isPropertyDeclaredInAncestorClass function to accurately identify properties inherited from ancestor classes.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2376#issuecomment-3650972594) **camc314** said "nice, thank you 🙏 "
 * (today) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2376#issuecomment-3651573635) **ahejlsberg** said "@camc314 When you get a chance, can you verify that this has fixed the issue for you?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2376#issuecomment-3651626870) **camc314** said "Yep, this has fixed the panic, thank you!"

### [Issue microsoft/TypeScript-go#2380](https://github.com/microsoft/TypeScript-go/issues/2380) (Open)

**Explosion in emit time on VS Code**

*Removing the --noEmit flag in VS Code’s TypeScript compilation causes the emit phase to jump to 74 seconds.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2381](https://github.com/microsoft/TypeScript-go/pull/2381) (Open)

**Use Realpath instead of EvalSymlinks for exe dir**

*Switch from EvalSymlinks to Realpath for resolving the executable directory path.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2382](https://github.com/microsoft/TypeScript-go/issues/2382) (Open, `Domain: Editor`)

**\[bug\] JS/TS Format Selection can delete comments**

*Formatting a selected portion of a JavaScript or TypeScript block comment unexpectedly removes the comment.*

 * created by **RedCMD**
 * **RedCMD** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2383](https://github.com/microsoft/TypeScript-go/issues/2383) (Open, **andrewbranch**, **gabritto**)

**LSP: Path suggestion missing \(import/export\)**

*Path completion suggestions for import/export statements are missing in tsgo, unlike in TypeScript 5.9.*

 * created by **besserwisser**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3655514582) **dalisoft** said "Maybe related to https://github.com/microsoft/typescript-go/issues/2189"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3655614357) **besserwisser** thanked and stated uncertainty about whether auto import equates to file path completion in insert mode

### [Issue microsoft/TypeScript-go#2384](https://github.com/microsoft/TypeScript-go/issues/2384) (Open)

**slow Code Completion with use valibot schema define**

*TypeScript code completion becomes significantly slow when using Valibot to define large schemas.*

 * created by **wszgrcy**

### [PR microsoft/TypeScript-go#2385](https://github.com/microsoft/TypeScript-go/pull/2385) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 2 directories with 4 updates**

*Update GitHub Actions dependencies: bump codecov-action, upload-artifact, and codeql-action in the root and actions/cache in the setup-go directory.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript-go#2386](https://github.com/microsoft/TypeScript-go/issues/2386) (Open, `Domain: Editor`)

**TS2307 Delete a folder of \`\.ts\` files does not trigger \`ts\(2307\)\` error hint**

*VSCode does not display a ts(2307) missing module error when a referenced folder of .ts files is deleted*

 * created by **ColaFanta**
 * **ColaFanta** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#648](https://github.com/microsoft/TypeScript-go/issues/648) (Open, `Domain: API and Extensibility`)

**Support embedded JavaScript/TypeScript**

*Enable built-in handling of embedded JavaScript/TypeScript in languages such as MDX, Vue, Svelte, Astro, and Markdown in the Go rewrite.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3649420466) **NullVoxPopuli** warned against using regex and recommended a real parser, citing 40+ bugs from a previous regex-based parser and describing Ember's volar plugin approach
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3649443016) **silverwind** agreed that regex is too crude and suggested using a proper parser with an example of nested script tags
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3649445924) **segevfiner** explained that type checking Vue SFC requires handling template expressions and that vue-tsc uses a monkey patch in TypeScript due to tsc's lack of a plugin API
 * [today](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3651875416) **yacinehmito** presented a semi-working prototype of vue-tsc in tsgo and argued that forks would be inevitable until the TypeScript team clarified the extensibility story
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3655213044) **auvred** described building a working prototype of a Vue language server based on tsgo that supports diagnostics and hover in .vue files
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3655258787) **remcohaszing** listed several downsides of forking, including the requirement to keep the fork up-to-date and the inability of extensions to interoperate
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3655671193) **auvred** illustrated feasibility with oxc-project/tsgolint and asked why extensions couldn’t interoperate
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3655911105) **jasonlyu123** suggested structuring the TypeScript rewrite to officially support custom file extensions and enhance LSP integration

