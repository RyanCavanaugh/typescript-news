# Report for 2026-01-05 (Monday, January 5th, 2026)

7 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @Netail reported that renaming directories caused alias and relative imports to break in [microsoft/TypeScript-go#1882](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3714016968)
    * @TFTomSun provided error logs and suggested a possible cause (Windows long path issue) in [microsoft/TypeScript-go#2441](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3711193517)

## Activity Summary

### [Issue microsoft/TypeScript-go#1882](https://github.com/microsoft/TypeScript-go/issues/1882) (Open, `Needs More Info`)

**Renaming/moving file breaks imports**

*Renaming a TypeScript file in tsgo leads to TS6307 errors due to missing project file listing, unlike TypeScript 5.8.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3633334604) **GitMurf** added a note to help others encountering the same issue
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3633341647) **jakebailey** suggested that file change/watch updates should suffice instead of didRenameFiles and requested LSP logs
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3633387689) **GitMurf** confirmed correct behavior in VSCode and Neovim and stated intent to update the earlier comment
 * [later](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3714016968) **Netail** described that renaming a directory or file in VSCode broke alias and relative imports while dependency imports still worked

### [Issue microsoft/TypeScript-go#2290](https://github.com/microsoft/TypeScript-go/issues/2290) (Closed, `Domain: JS`, `Crash`, **sandersn**)

**Crash for completions after JSDoc \`\*\` on line following string\-named property signature**

*TypeScript Go language server panics when requesting completions after a JSDoc asterisk following a string-named property signature.*

 * **DanielRosenwasser** added label `Domain: JS`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2290#issuecomment-3644048426) **DanielRosenwasser** suggested it was the same issue and provided a code snippet and stack trace showing a panic in textDocument/completion
 * **RyanCavanaugh** assigned to **sandersn**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2336](https://github.com/microsoft/TypeScript-go/issues/2336) (Open, `Crash`, **jakebailey**, **Copilot**)

**Crash for signature help in arrow function parameters**

*Signature help invoked on arrow function parameters crashes the TypeScript server without a stack trace*

 * (3 weeks ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3711830899) **gabritto** explained that printing the signature label for an anonymous function type generated an invalid UTF-8 name, causing JSON marshalling to fail and the server to stop

### [PR microsoft/TypeScript-go#2371](https://github.com/microsoft/TypeScript-go/pull/2371) (Closed)

**Fix getTokenAtPos in JSDoc trivia position**

*Modify getTokenAtPosition to track the next AST node and return nil for JSDoc trivia gap positions.*

 * created by **gabritto**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2371#issuecomment-3649659571) **ahejlsberg** said "@gabritto See my comment here."
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2435](https://github.com/microsoft/TypeScript-go/pull/2435) (Closed)

**Support identifier location in inlay hints**

*Update Corsa’s inlay hint implementation to record identifier symbol locations in a separate map and adjust tests avoiding URI conversions.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2441](https://github.com/microsoft/TypeScript-go/issues/2441) (Open)

**using tsgo fails with pnpx**

*Invoking tsgo via pnpx with @typescript/native-preview fails with a spawnSync ENOENT error because tsgo.exe cannot be found.*

 * created by **TFTomSun**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3711193517) **TFTomSun** suggested that a Windows long path issue caused the ENOENT spawnSync error due to a path exceeding 256 characters
 * [today](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3712210293) **DanielRosenwasser** said "So would this be a bug in pnpx?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3712297789) **JoostK** doubted that pnpx had a bug and explained that the tsgo JS wrapper spawned a native binary at a too-long path

### [Issue microsoft/TypeScript-go#2443](https://github.com/microsoft/TypeScript-go/issues/2443) (Open)

**\[Doc\]: paths map value points to removed baseUrl value**

*Inline documentation incorrectly references the removed baseUrl option for computing paths map values.*

 * created by **tanepiper**

### [Issue microsoft/TypeScript-go#2444](https://github.com/microsoft/TypeScript-go/issues/2444) (Open, `Domain: Editor`)

**Missing code actions \(\`editor\.codeActionsOnSave\`\) with \`typescript\.experimental\.useTsgo\` in VSCode**

*Enabling typescript.experimental.useTsgo in VSCode disables most code actions on save, preventing missing imports from being added automatically.*

 * created by **virtuallyunknown**
 * **virtuallyunknown** added label `Domain: Editor`

