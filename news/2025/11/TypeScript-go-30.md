# Report for 2025-11-30 (Sunday, November 30th, 2025)

3 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @eamodio provided the source of the issue and noted use of a TypeScript plugin in [microsoft/TypeScript-go#2154](https://github.com/microsoft/TypeScript-go/issues/2154#issuecomment-3592868843)

## Activity Summary

### [Issue microsoft/TypeScript-go#2152](https://github.com/microsoft/TypeScript-go/issues/2152) (Closed, `Domain: Editor`)

**Cannot find module when using paths**

*VS Code Insider with tsgo fails to resolve custom '@env/*' paths in the GitLens codebase, causing module not found errors.*

 * created by **eamodio**
 * **eamodio** added label `Domain: Editor`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2152#issuecomment-3568354264) **jakebailey** said "If you had been using paths and baseUrl, you may want to consider using the tool linked in https://github.com/microsoft/TypeScript/issues/62508#issuecomment-3348649259"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2152#issuecomment-3592866470) **eamodio** said "Thanks! Running that tool fixed it, not sure what was different than what I tried manually."
 * (today) **eamodio** closed the issue

### [Issue microsoft/TypeScript-go#2154](https://github.com/microsoft/TypeScript-go/issues/2154) (Closed, `Domain: Editor`)

**"Go to definition" is missing within html template strings \(lit\)**

*VS Code ctrl-click go to definition does not work for lit-html template string component tags when using tsgo*

 * created by **eamodio**
 * **eamodio** added label `Domain: Editor`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2154#issuecomment-3568356100) **jakebailey** said "Do you have a tsserver plugin enabled, or an extension that loaded one? Those will not work with tsgo."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2154#issuecomment-3592868843) **eamodio** said "Ah, yes this comes from https://marketplace.visualstudio.com/items?itemName=jackolope.lit-analyzer-plugin and it uses a typescript plugin."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2154#issuecomment-3593002146) **jakebailey** said "Yes, so this is expected. Existing plugins for tsserver won't work in the new codebase."

### [Issue microsoft/TypeScript-go#2169](https://github.com/microsoft/TypeScript-go/issues/2169) (Open, `Domain: Editor`)

**Support for \`workspace/diagnostic\` from LSP 3\.17**

*Implement LSP 3.17 workspace/diagnostics to provide reliable project-wide diagnostics without opening each file.*

 * created by **versecafe**

