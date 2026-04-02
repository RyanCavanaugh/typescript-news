# Report for 2025-12-29 (Monday, December 29th, 2025)

5 different users commented on 9 different issues.

## Recommended Actions

 * Moderation
    * @ItsHarper posted rude content in [microsoft/TypeScript-go#2414](https://github.com/microsoft/TypeScript-go/issues/2414#issuecomment-3699011420)
 * Response Recommended
    * @spanishpear asked if the test was configured correctly and provided profiling details in [microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3698941951)

## Activity Summary

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Open, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647062740) **jakebailey** said "Is this codebase public? That definitely sounds like the opposite of how it should behave."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647124648) **Knagis** suggested using an NDA path to share the private codebase and described its structure as React TSX files, Jest and Playwright specs, declaration-only emits, with few symlinks and path aliases
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3654358600) **Knagis** reported that running tsgo with specified flags resulted in a 30GB commit, hung, and could not be killed via task manager
 * [later](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3698941951) **spanishpear** reported high memory usage when typechecking a large project and its dependents, noted that tsc was faster, provided profiling details, and asked if the test was configured correctly

### [Issue microsoft/TypeScript-go#2414](https://github.com/microsoft/TypeScript-go/issues/2414) (Closed)

**there are like 30 tsgo lsp servers**

*Approximately 30 tsgo LSP server instances are running in a devcontainer, indicating a possible extension or VS Code bug.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2414#issuecomment-3677867868) **hg** explained that they were operating system threads in htop and instructed how to hide them by pressing capital H or display TGID in settings
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2414#issuecomment-3677940754) **jakebailey** said "Yeah, green in htop means threads; I personally disable showing userspace threads in htop."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2414#issuecomment-3678473411) **alita-moore** said "TIL, I think this issue can be closed then"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2414#issuecomment-3699011420) **ItsHarper** said "Why not close it yourself, instead of leaving clutter?"

### [Issue microsoft/TypeScript-go#2427](https://github.com/microsoft/TypeScript-go/issues/2427) (Open, `bug`)

**\`isolatedDeclarations\` is not yet implemented**

*tsgo does not implement the isolatedDeclarations compiler option, so it fails to report missing annotations unlike tsc 5.9.*

 * created by **so1ve**
 * **DanielRosenwasser** added label `bug`

### [Issue microsoft/TypeScript-go#2430](https://github.com/microsoft/TypeScript-go/issues/2430) (Open, `Domain: Editor`)

**C\# language server stopped working after switching to \.ts file with tsgo enabled**

*Enabling tsgo in a VS Code ASP.NET MVC project breaks C# language server’s go-to-definition and reference features.*

 * created by **bjoerni79**
 * **bjoerni79** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2430#issuecomment-3697359931) **DanielRosenwasser** said "Can you elaborate a bit more on what isn't working? Are you using this from a Razor template or something?"

### [PR microsoft/TypeScript-go#2432](https://github.com/microsoft/TypeScript-go/pull/2432) (Open)

**Include import specifiers as references in code lens**

*Import specifiers are now properly counted and deduplicated as code lens references, aligning behavior with TypeScript 6.0.*

 * created by **darwin808**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2432#issuecomment-3698447259) **darwin808** agreed with microsoft-github-policy-service

### [Issue microsoft/TypeScript-go#648](https://github.com/microsoft/TypeScript-go/issues/648) (Open, `Domain: API and Extensibility`)

**Support embedded JavaScript/TypeScript**

*Enable built-in handling of embedded JavaScript/TypeScript in languages such as MDX, Vue, Svelte, Astro, and Markdown in the Go rewrite.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3655258787) **remcohaszing** listed several downsides of forking, including the requirement to keep the fork up-to-date and the inability of extensions to interoperate
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3655671193) **auvred** illustrated feasibility with oxc-project/tsgolint and asked why extensions couldn’t interoperate
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3655911105) **jasonlyu123** suggested structuring the TypeScript rewrite to officially support custom file extensions and enhance LSP integration
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3699022588) **ItsHarper** asked why extensions couldn't interoperate and explained that compiler forks can’t interoperate without merging all changes
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3699085966) **auvred** suggested that a unified plugin architecture could allow language extensions to run in separate processes and be written in any language and noted that tsgo would be a nicer plugin host

