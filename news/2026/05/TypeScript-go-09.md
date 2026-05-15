# Report for 2026-05-09 (Saturday, May 9th, 2026)

5 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @rchl provided additional affected capabilities in [microsoft/TypeScript-go#3792](https://github.com/microsoft/TypeScript-go/issues/3792#issuecomment-4415413008)
    * @rchl suggested creating experimental properties and phasing out root ones in [microsoft/TypeScript-go#3792](https://github.com/microsoft/TypeScript-go/issues/3792#issuecomment-4415658755)

## Activity Summary

### [Issue microsoft/TypeScript-go#3788](https://github.com/microsoft/TypeScript-go/issues/3788) (Closed)

**Behavior difference: callback contextual typing — \`tsc@5\.9\.3\` passes, \`tsc@6\.0\.3\` / \`tsgo\` fail**

*TypeScript 6.0.3 and tsgo misinfer callback parameter types under pnpm enableGlobalVirtualStore symlinks, causing TS7031 errors that 5.9.3 did not produce.*

 * created by **dougludlow**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4412914876) **Andarist** said "It would be great if you could pull all of the relevant 3rd party types into a single file - a good repro usually can be created in a single import-less TS playground."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4412927439) **dougludlow** expressed uncertainty and specified that the import issue occurred only with pnpm’s enableGlobalVirtualStore, working in TypeScript v5.9.3 but failing in v6/v7
 * [today](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4413473493) **Andarist** said "Ah, I'm sorry! I've missed that this specifically requires enableGlobalVirtualStore"

### [Issue microsoft/TypeScript-go#3789](https://github.com/microsoft/TypeScript-go/issues/3789) (Closed, `Crash`, **ahejlsberg**)

**Panic in \`ast\.GetNextJSDocCommentLocation\`**

*ast.GetNextJSDocCommentLocation panics on shorthand property assignment nodes, causing tsgo compilation failures.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** added label `Crash`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3790](https://github.com/microsoft/TypeScript-go/pull/3790) (Closed)

**Align and simplify \`getFunctionLikeHost\` and \`GetNextJSDocCommentLocation\`**

*Align and simplify getFunctionLikeHost and GetNextJSDocCommentLocation for improved code consistency and maintainability.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3791](https://github.com/microsoft/TypeScript-go/issues/3791) (Closed, `Domain: Type Checking`, `Crash`, **ahejlsberg**)

**tsgo panics on a recursive\-mapped\-type \+ intersection \+ generic\-signature pattern**

*tsgo panics during type checking when combining recursive mapped types, intersections, and generic function signatures*

 * created by **shiweiwei97**
 * **shiweiwei97** added label `Crash`
 * (later) **ahejlsberg** added label `Domain: Type Checking`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3791#issuecomment-4415501540) **ahejlsberg** said "This assertion failure happens with both tsc and tsgo. A condition that shouldn't be false ends up being so due to an excessive stack depth which the logic doesn't account for."

### [Issue microsoft/TypeScript-go#3792](https://github.com/microsoft/TypeScript-go/issues/3792) (Open, `Needs Investigation`, **andrewbranch**)

**\[lsp\] Experimental server capabilities should be defined on "experimental" object**

*Align server capabilities with the LSP specification by defining experimental features under the "experimental" property*

 * created by **rchl**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3792#issuecomment-4415413008) **rchl** said "Same for capabilities like customMultiDocumentHighlightProvider and customSourceDefinitionProvider that I've just noticed."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3792#issuecomment-4415636188) **jakebailey** asked if not doing this was causing issues and stated that VS-related settings could not be changed
 * [later](https://github.com/microsoft/TypeScript-go/issues/3792#issuecomment-4415658755) **rchl** pointed out a spec violation and suggested moving the properties to an experimental object and phasing out the root ones
 * [later](https://github.com/microsoft/TypeScript-go/issues/3792#issuecomment-4415691581) **jakebailey** said "The VS ones are pretty locked in stone "

### [Issue microsoft/TypeScript-go#3793](https://github.com/microsoft/TypeScript-go/issues/3793) (Open, `possible improvement`)

**\[lsp\] make source action kinds more specific**

*Advertise more specific LSP code action kinds with .ts suffixes to enable TypeScript-specific on-save actions without affecting other servers.*

 * created by **rchl**

### [PR microsoft/TypeScript-go#3794](https://github.com/microsoft/TypeScript-go/pull/3794) (Closed)

**Remove assertion that doesn't hold after excessive stack depth overflow**

*Remove assertion that fails after excessive stack depth overflow causing spurious failures*

 * created by **ahejlsberg**

