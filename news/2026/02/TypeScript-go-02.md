# Report for 2026-02-02 (Monday, February 2nd, 2026)

13 different users commented on 32 different issues.

## Recommended Actions

 * Response Recommended
    * @tomredman provided environment details and a stack trace in [microsoft/TypeScript-go#2648](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3840929021)
    * @tomredman provided a workaround and pointed out a duplicate issue in [microsoft/TypeScript-go#2648](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3841032189)
    * @ButbkaDrug provided reproduction steps and a workaround in [microsoft/TypeScript-go#2649](https://github.com/microsoft/TypeScript-go/issues/2649#issuecomment-3840802482)
    * @abrahamguo noted that a specific feature was missed after being introduced and ported in [microsoft/TypeScript-go#2652](https://github.com/microsoft/TypeScript-go/issues/2652#issuecomment-3841251001)

## Activity Summary

### [Issue microsoft/TypeScript-go#2503](https://github.com/microsoft/TypeScript-go/issues/2503) (Open, **gabritto**)

**Autocomplete and auto\-import is slower in JSX context**

*JSX tag autocomplete and auto-import in TypeScript monorepos remains slow (~1s vs ~100ms) due to expensive contextual type computation.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3751004372) **jansedlon** shared four videos demonstrating tsserver, native TS branch, and their fix performance, and asked how stable Typescript LSP performance should be
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3752145034) **gabritto** requested a repro project or CPU profile log to investigate JSX completions slowness
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3784284733) **jansedlon** said "Hey grabritto, sorry for the delay. I tried it today and for some reason it worked fine. When it happens again, i will take a cpu profile and send it to you"
 * **gabritto** assigned to **gabritto**

### [PR microsoft/TypeScript-go#2592](https://github.com/microsoft/TypeScript-go/pull/2592) (Closed)

**Support \`Object\.defineProperty\` in document symbols**

*Add support for Object.defineProperty in document symbols and refactor code to allow direct symbol name passing in special cases.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2609](https://github.com/microsoft/TypeScript-go/issues/2609) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Type instantiation is excessively deep and possibly infinite\.**

*tsgo throws a deep, possibly infinite type instantiation error for TanStack Form with zod that TypeScript 5.9 compiles without issue.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3819510125) **jakebailey** said "This is a pretty large repro; do you have something that doesn't pull in a the library?"
 * **jakebailey** assigned to **ahejlsberg**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3819956812) **TkDodo** removed zod and unnecessary type parameters to create a ~200-line reproduction, noted the TS2589 error still occurred in tsgo but not in tsc, and shared a TypeScript Playground link
 * [today](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3838297571) **ahejlsberg** identified the issue as a type ordering problem and observed that compiling with TS 6.0 in type ordering compatibility mode produced the same deep type instantiation error, concluding there was probably not much to be done
 * (today) **ahejlsberg** added labels `Type Ordering`, `Domain: Type Checking`

### [PR microsoft/TypeScript-go#2617](https://github.com/microsoft/TypeScript-go/pull/2617) (Closed)

**ExplainFiles to handle duplicated files **

*Enhance ExplainFiles to detect and properly handle duplicated files to avoid conflicts or redundancy.*

 * created by **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#2620](https://github.com/microsoft/TypeScript-go/pull/2620) (Open)

**Bring back async API, allow API connection to LSP process**

*Reintroduce a decoupled async JSON-RPC API client and server in the LSP to enable external extensions to query TypeScript state.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3836765880) **jakebailey** suggested using gensync for clever codegen to alleviate async function coloring annoyance in TypeScript client code

### [PR microsoft/TypeScript-go#2623](https://github.com/microsoft/TypeScript-go/pull/2623) (Open)

**Fix inlay hints panic: guard against stale line map in LineAndCharacterToPosition**

*Prevent inlay hint panics by guarding against stale line map offsets in LineAndCharacterToPosition*

 * created by **abelcha**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3827319301) **jakebailey** said "I don't think we should do this. If this happens, the caller is at fault and needs to be fixed. It can only be a symptom of a worse problem above."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3834947424) **abelcha** questioned whether recomputing line maps on every request was worth the performance hit and suggested using a guard instead
 * [today](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3837337190) **DanielRosenwasser** described two cases needing handling: '/resolve'-like requests with content length changes causing non-existent positions, and logic operating on nodes with source text from the wrong file; and noted the need to recalculate or dismiss outdated line maps
 * [today](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3837346475) **DanielRosenwasser** noted a potential issue with the snapshot implementation and explained that snapshots prevent data state inconsistencies

### [Issue microsoft/TypeScript-go#2631](https://github.com/microsoft/TypeScript-go/issues/2631) (Closed, **DanielRosenwasser**)

**Code lenses and inlay hints only respected from \`javascript\.\` settings since \`0\.20260127\.1\`**

*After v0.20260127.1, VS Code ignores TypeScript inlay hint and code lens settings unless defined under javascript.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2631#issuecomment-3833892969) **DanielRosenwasser** identified that trimming the file extension's leading dot caused ExtensionIsTs to fail and suggested adding a server test
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2632](https://github.com/microsoft/TypeScript-go/issues/2632) (Open)

**\`@param\` JSDoc requires parameter names, did not in 6\.0 and prior**

*Omitting parameter names in JSDoc @param tags prevents TypeScript from reporting argument type mismatches under noImplicitAny.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2632#issuecomment-3836132764) **a-tarasyuk** said "@DanielRosenwasser If I remember correctly, earlier versions also required a parameter name. Is this intentional, or is it a new feature to make it optional?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2632#issuecomment-3836891087) **DanielRosenwasser** said "I probably complained to @sandersn about it then and I'll complain about it in 7.0 too. 😄"

### [PR microsoft/TypeScript-go#2633](https://github.com/microsoft/TypeScript-go/pull/2633) (Closed)

**Leave extension as\-is for TS extension comparison\.**

*Preserve the original file extension during TypeScript extension comparisons and discuss server or VS Code extension tests.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2633#issuecomment-3836580852) **gabritto** observed that the fourslash client differed from vscode by passing preferences directly as a map and sending LSP messages without JSON marshalling, potentially affecting server tests
 * [today](https://github.com/microsoft/TypeScript-go/pull/2633#issuecomment-3837769802) **DanielRosenwasser** wrote a unit test for GetPreferences and offered to drop it if the configuration approach changes
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2635](https://github.com/microsoft/TypeScript-go/pull/2635) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 2 directories with 2 updates**

*Bump GitHub Actions dependencies by updating codeql-action to 4.32.0 and actions/cache in the setup-go directory.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2636](https://github.com/microsoft/TypeScript-go/issues/2636) (Open, **jakebailey**, **Copilot**)

**tsgo emits a \`require\` statement when a value is imported without the \`type\` keyword but only used in type\-level positions**

*tsgo incorrectly emits a require call for value imports used only in type positions, causing unwanted side effects at runtime.*

 * created by **psm14**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2638](https://github.com/microsoft/TypeScript-go/issues/2638) (Open)

**tsgo emits class field declarations for conditionally assigned fields that tsc doesn't**

*tsgo emits explicit class field declarations for optional or conditionally initialized properties that tsc omits, causing different runtime behavior.*

 * created by **psm14**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2638#issuecomment-3836274653) **jakebailey** said "Yes, this transform is not yet implemented"

### [PR microsoft/TypeScript-go#2639](https://github.com/microsoft/TypeScript-go/pull/2639) (Closed)

**Fix default configured project crash with \`disableReferecedProjectLoad\`**

*Finding a default configured project with disableReferencedProjectLoad crashes due to accessing unloaded referenced projects.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2640](https://github.com/microsoft/TypeScript-go/issues/2640) (Open)

**tsgo \-\-watch is lagging and sometimes not emitting at all**

*tsgo watch mode intermittently fails to emit updates promptly or at all when source files change*

 * created by **tharakadesilva**

### [PR microsoft/TypeScript-go#2641](https://github.com/microsoft/TypeScript-go/pull/2641) (Closed)

**Properly track first Quick Info declaration \+ fix issue in fourslash**

*Properly track initial Quick Info declarations and fix fourslash baseline verification in multi-file tests.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2641#issuecomment-3836694538) **jakebailey** said "You fixed four generated tests, so you should be able to do npm run updatefailing"
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2642](https://github.com/microsoft/TypeScript-go/pull/2642) (Closed)

**Update dependencies**

*Upgrade project dependencies including xxh3 v1.1.0 with ARM64 support, npm v11, and golangci-lint modernizers.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2643](https://github.com/microsoft/TypeScript-go/pull/2643) (Open)

**Misc customlint updates**

*Proposes several long-planned refactors and enhancements for the customlint tool*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2644](https://github.com/microsoft/TypeScript-go/pull/2644) (Closed)

**Major dep update, largely require node20**

*A significant dependency update was implemented, causing the project to predominantly require Node.js version 20.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2645](https://github.com/microsoft/TypeScript-go/pull/2645) (Closed)

**Add first\-class unused baseline tracking**

*Add unused baseline tracking to hereby test by incorporating TestMain to record baselines, flag unknown files, and emit .delete files.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [PR microsoft/TypeScript-go#2646](https://github.com/microsoft/TypeScript-go/pull/2646) (Closed, **jakebailey**, **Copilot**)

**Fix import elision with type\-only usage**

*Fix import elision logic in tsgo to prevent emitting require statements for imports used exclusively in type positions*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2647](https://github.com/microsoft/TypeScript-go/pull/2647) (Open)

**fix\(2632\): allow missing names in jsdoc param tags**

*Enable JSDoc @param tags to omit parameter names without causing errors*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#2648](https://github.com/microsoft/TypeScript-go/issues/2648) (Open, `Crash`)

**panic handling request textDocument/codeAction: textDocument/codeAction returned ErrNeedsAutoImports even after enabling auto imports**

*TypeScript LSP panics on codeAction requests returning ErrNeedsAutoImports despite auto imports being enabled*

 * created by **pattobrien**
 * **pattobrien** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3840929021) **tomredman** reported that the error persisted since version 0.20260129.1, provided environment details, and included a stack trace
 * [later](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3841032189) **tomredman** removed autoImport excludes to resolve the error and suggested the issue was a duplicate of microsoft/typescript-go#2598

### [Issue microsoft/TypeScript-go#2649](https://github.com/microsoft/TypeScript-go/issues/2649) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**LSP Panic: strings: negative Repeat count when formatting JSDoc within nested scope**

*The TypeScript LSP server panics with a negative repeat count error when formatting nested JSDoc comments.*

 * created by **ButbkaDrug**
 * **ButbkaDrug** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2649#issuecomment-3840618713) **DanielRosenwasser** said they couldn't reproduce the issue in Neovim and suggested guarding against negative tab size values
 * **DanielRosenwasser** added label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2649#issuecomment-3840802482) **ButbkaDrug** reported that tsgo consistently crashes when code starts on the first line, provided a code snippet and a workaround, and noted inconsistent trimming of first letters

### [Issue microsoft/TypeScript-go#2650](https://github.com/microsoft/TypeScript-go/issues/2650) (Open, `Crash`)

**Specifying declaration files in "moduleSuffixes" leads to panic**

*Including declaration files in moduleSuffixes triggers a panic in typescript-go’s checker during external module resolution.*

 * created by **voronin-ivan**
 * **voronin-ivan** added label `Crash`

### [Issue microsoft/TypeScript-go#2651](https://github.com/microsoft/TypeScript-go/issues/2651) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Different behaviour of \`editor\.action\.smartSelect\` vs built\-in TS**

*smartSelect.expand includes surrounding quotes when selecting bracketed strings with the TS native preview extension but not with the built-in TypeScript.*

 * created by **aantia**
 * **aantia** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2652](https://github.com/microsoft/TypeScript-go/issues/2652) (Closed, **jakebailey**, **Copilot**)

**\`resolveJsonModule\` is not defaulted to \`true\` when \`module\` is \`nodenext\`**

*When using module: nodenext, resolveJsonModule isn’t enabled by default, causing JSON imports to fail in tsgo.*

 * created by **abrahamguo**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2652#issuecomment-3841251001) **abrahamguo** said "This feature was introduced into TS in typescript#61805, and ported to tsgo in #1797, but it looks like this specific feature was missed."

### [Issue microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961) (Open, `bug`, `Domain: Emit`, `Domain: Type Checking`, **jakebailey**)

**tsgo fails to resolve namespace symbols in non\-extends contexts across files**

*tsgo fails to qualify namespace symbols A and Afunc outside extends contexts across files, causing incorrect JS and runtime errors.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3828459486) **magic-akari** thanked @dtscd for the patch, confirmed it worked for same-file scenarios, and asked whether cross-namespace value qualification should be supported, noting architectural consistency and ecosystem precedent
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3828685368) **dtscd** argued that removing cross-namespace resolution trivialized namespaces, highlighted ES modules' per-file scoping and minimal linking performance impact, and lamented added user complexity compared to Go
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3828862365) **dtscd** shared a proof-of-concept change adding outfile support with sourceMaps and a commit link, asserted it worked for their project and challenged the performance argument
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3837656679) **jakebailey** stated that they wouldn't change the behavior and asked for a PR to correct tsgo
 * **jakebailey** added label `bug`

