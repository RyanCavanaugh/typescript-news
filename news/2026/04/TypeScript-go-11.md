# Report for 2026-04-11 (Saturday, April 11th, 2026)

4 different users commented on 6 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#3388](https://github.com/microsoft/TypeScript-go/pull/3388) (Closed)

**No reparsing of CommonJS constructs**

*Remove re-parsing of CommonJS constructs and instead handle module.exports and exports in the binder and checker, ignoring CJS in ES modules.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4229756532) **ahejlsberg** reported that they had to disable the formatting step locally in the AST generation scripts and showed logs of formatter failures
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4229759579) **ahejlsberg** said "@andrewbranch @jakebailey I'm not sure why hereby generate:ast fails for me locally. Could be a configuration issue, or could be that the script doesn't work properly on Windows. Ideas?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4229838104) **ahejlsberg** asked whether files were fully bound before computing build info and noted that CommonJSModuleIndicator assignment moved from parsing to binding
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4229925839) **jakebailey** assumed the race condition stemmed from affectsGlobalScope requiring binding information, suggested calling binder.BindSourceFile at the start of fileAffectsGlobalScope, and referenced Strada's use of getTypeChecker to ensure files are bound
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4229930867) **jakebailey** said "I cannot reproduce your ast generation issues on Windows, unfortunately..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4229943617) **ahejlsberg** asked why dprint couldn't find any files to format despite working from the CLI
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4229964129) **ahejlsberg** identified that the dprint issue occurred when the drive letter in the working directory was lower-case c: but succeeded when it was upper-case C:
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4230235843) **jakebailey** noted that PowerShell does not allow changing into a lowercase drive and asked if adding a directory change workaround at the top of Herebyfile.mjs would fix it
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4230326122) **ahejlsberg** confirmed that adding the code at the top of Herebyfile.mjs made it work

### [Issue microsoft/TypeScript-go#3389](https://github.com/microsoft/TypeScript-go/issues/3389) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**Factory statement and type declaration nodes do not emit export modifier**

*Factory-created type alias declarations and statements fail to include the export modifier when printed due to missing createNodeArray calls for modifiers.*

 * created by **virtulis**

### [PR microsoft/TypeScript-go#3390](https://github.com/microsoft/TypeScript-go/pull/3390) (Closed)

**Coerce factory modifiers argument to NodeArray**

*Automatically coerce the modifiers argument for factory functions into a NodeArray*

 * created by **virtulis**

### [PR microsoft/TypeScript-go#3391](https://github.com/microsoft/TypeScript-go/pull/3391) (Open)

**Fix inference from unions of arrays with different nesting depths**

*Add a matching pass to infer equally nested arrays first, correcting generic type inference for unions like T[] | T[][]*

 * created by **Yiin**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3391#issuecomment-4231802984) **Yiin** said "@microsoft-github-policy-service agree"

