# Report for 2026-05-26 (Tuesday, May 26th, 2026)

11 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @chriskrycho asked if the leading ${workspaceFolder}/ is required or if its omission is a bug in [microsoft/TypeScript-go#1946](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-4547381587)
    * @hkleungai asked to continue supporting expando types and work towards a fix in [microsoft/TypeScript-go#4045](https://github.com/microsoft/TypeScript-go/issues/4045#issuecomment-4553479379)

## Activity Summary

### [Issue microsoft/TypeScript-go#1946](https://github.com/microsoft/TypeScript-go/issues/1946) (Open, `Domain: Editor`, **mjbvz**)

**Support workspace specific typescript version**

*Allow the extension to use a workspace-specific TypeScript version rather than a global one.*

 * (8 weeks ago) **RyanCavanaugh** added label `Domain: Editor`, set milestone to `Possible Improvement`, and assigned to **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-4547381587) **chriskrycho** asked whether the leading ${workspaceFolder}/ prefix is required for typescript.native-preview.tsdk or if its omission is a bug

### [Issue microsoft/TypeScript-go#3320](https://github.com/microsoft/TypeScript-go/issues/3320) (Open, `Domain: Editor`, **iisaduan**)

**Missing \`removeUnused\` code fix/code action**

*The removeUnused code action and underlying unused identifier fixes are not implemented for VSCode’s TypeScript codeActionOnSave.*

 * **iisaduan** assigned to **iisaduan**
 * (6 weeks ago) **RyanCavanaugh** added label `Domain: Editor`, and set milestone to `Post-7.0`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3320#issuecomment-4554817607) **a-tarasyuk** asked whether implementing support for removeUnused/removeUnusedImports/unusedIdentifier was still considered useful

### [Issue microsoft/TypeScript-go#3661](https://github.com/microsoft/TypeScript-go/issues/3661) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo emits an "extra" TS7006 along with TS2769 at the same line in case of overload mismatch**

*tsgo redundantly emits both TS2769 and TS7006 errors for an overload mismatch call, unlike tsc.*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3661#issuecomment-4549508851) **weswigham** said "This, AFAIK, was an intentional strictness improvement to JS signature analysis - it's intentionally no longer lax on argument count in JS to match TS behavior."

### [Issue microsoft/TypeScript-go#3981](https://github.com/microsoft/TypeScript-go/issues/3981) (Closed, `bug`, `Domain: Editor`, **gabritto**)

**Excess path components suggested in completions**

*Import path completions for @typescript/native-preview/unstable repeatedly include existing segments, duplicating folder names and causing imports like unstable/unstable/ast.*

 * (1 week ago) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, and assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3983](https://github.com/microsoft/TypeScript-go/issues/3983) (Closed, `wontfix`)

**Declaration emit leaks namespace declarations for \`@internal\` functions with static property assignments**

*tsgo includes namespace declarations for internal functions with static property assignments in .d.ts files even when stripInternal is enabled*

 * created by **MgmClientGuy**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3983#issuecomment-4488712247) **danyalahmed1995** reproduced the stripInternal issue and observed that TS 6.0.3 omits the merged namespace while TS 7 native preview still emits it, indicating a declaration emit parity gap
 * **RyanCavanaugh** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3983#issuecomment-4549240811) **RyanCavanaugh** said "stripInternal is "use at your own risk""
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4010](https://github.com/microsoft/TypeScript-go/issues/4010) (Closed, `bug`, `Domain: Editor`, **gabritto**)

**\[lsp\] Hover verbosity fails after increasing verbosity**

*Toggling hover verbosity levels in LSP-tsgo for JobsStateToColor causes canIncreaseVerbosity to be omitted from server responses.*

 * (yesterday) **gabritto** added labels `bug`, `Domain: Editor`, and removed label `Needs Investigation`
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#4034](https://github.com/microsoft/TypeScript-go/issues/4034) (Open, `Domain: Declaration Emit`, `possible improvement`, `Needs Investigation`, **weswigham**)

**Behavior difference: tsgo emits different output when keys from one object are referenced in another object**

*tsgo emits generic index signatures for computed property keys instead of preserving specific keys, causing noise in diffs compared to tsc*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * (today) **weswigham** added labels `Domain: Declaration Emit`, `possible improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4034#issuecomment-4549484598) **weswigham** explained that the behavior was intentional for synthesized node types, acknowledged that more verbose output is preferable, and noted that the logic tracking original computed property names got lost in the port and needs reporting

### [Issue microsoft/TypeScript-go#4035](https://github.com/microsoft/TypeScript-go/issues/4035) (Open, `Domain: Editor`, `Needs Investigation`, **gabritto**)

**VSCode bulk save \(Replace All / Save All across many \.ts files\) deadlocks the LSP server**

*Bulk replacing across many .ts files in VSCode deadlocks the TypeScript Native Preview LSP server, which doesn’t restart on reload.*

 * created by **AdrianBannister**
 * **AdrianBannister** added label `Domain: Editor`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**

### [Issue microsoft/TypeScript-go#4037](https://github.com/microsoft/TypeScript-go/issues/4037) (Open, `bug`, **ahejlsberg**)

**TS2304 when a generic \(@template\) function JSDoc contains @overload**

*Generic functions documented with @template and @overload produce 'Cannot find name T' TS2304 errors in tsgo.*

 * (2 days ago) **ahejlsberg** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4546878117) **ahejlsberg** identified two issues with JSDoc @overload handling and offered to submit a PR fixing the first and documenting the second
 * [today](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4547708507) **antichris** lamented lack of arrow function overloading support, said they would have to rewrite their overloaded arrow functions as declarations, and thanked the maintainers
 * [today](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4549213250) **ahejlsberg** proposed a TypeScript overload translation from JSDoc overloads and said they would include it in their PR

### [Issue microsoft/TypeScript-go#4039](https://github.com/microsoft/TypeScript-go/issues/4039) (Open, `Domain: Declaration Emit`, `Domain: Comment Emit`)

**Behavior difference: Inline comment on arrow function parameters is emitted on tsc but not on tsgo**

*tsgo removes inline comments on arrow function parameters that tsc retains, resulting in lost parameter comments*

 * created by **hkleungai**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **weswigham** added labels `Domain: Declaration Emit`, `Domain: Comment Emit`

### [Issue microsoft/TypeScript-go#4040](https://github.com/microsoft/TypeScript-go/issues/4040) (Closed, `Working As Intended`)

**Behavior difference: Implicitly declared class member appear after constructor in tsc emit, but show up before constructor in tsgo**

*Implicitly declared class members appear before the constructor in tsgo output but after it in tsc output.*

 * created by **hkleungai**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4040#issuecomment-4527951322) **jakebailey** said "This is entirely benign and a side effect of https://github.com/microsoft/typescript-go/pull/3541 (see comments there)"
 * **weswigham** added label `Working As Intended`
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4041](https://github.com/microsoft/TypeScript-go/issues/4041) (Open, `Needs Investigation`, **andrewbranch**)

**Behavior difference: getTypeAtLocation returns method type for private method call**

*tsgo’s getTypeAtLocation incorrectly returns the private method’s function type instead of the call expression’s return type.*

 * created by **lucasavila00**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4042](https://github.com/microsoft/TypeScript-go/issues/4042) (Open)

**LSP custom/initializeAPISession never responds in stdio mode \(7\.0\.0\-dev\.20260518\.1 / 20260522\.1\)**

*Calling custom/initializeAPISession in tsgo’s stdio LSP mode hangs without JSON-RPC response or socket creation*

 * created by **re-thc**
 * (2 days ago) **re-thc** closed the issue
 * (2 days ago) **re-thc** reopened the issue
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4044](https://github.com/microsoft/TypeScript-go/issues/4044) (Closed, `Working As Intended`, **weswigham**)

**Behavior difference: tsc mark class method with \`override\` keyword according to jsdoc, but tsgo fails to do so\.**

*tsgo does not include the override keyword for class methods annotated with @override, unlike tsc.*

 * created by **hkleungai**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4044#issuecomment-4533873443) **a-tarasyuk** asked whether override should be stripped from declaration emit for JS files with @override jsdoc tags
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4044#issuecomment-4549427900) **weswigham** noted that Corsa aligns JS declarations with TS by eliding `override` from emitted declarations
 * (today) **weswigham** closed the issue
 * (today) **weswigham** added label `Working As Intended`, and removed label `Needs Investigation`

### [Issue microsoft/TypeScript-go#4045](https://github.com/microsoft/TypeScript-go/issues/4045) (Open, `bug`, `Domain: Declaration Emit`, `Domain: JS`, `Needs Investigation`)

**Behavior difference: Notable gap regarding expando declaration on a function between tsc & tsgo**

*tsgo aliases bound functions without namespaces compared to tsc, causing inconsistent type emissions for both PublicInternalBinding and PublicExportedBinding.*

 * created by **hkleungai**
 * (today) **weswigham** added labels `bug`, `Domain: Declaration Emit`, `Domain: JS`, and removed labels `bug`, `Domain: Declaration Emit`, `Domain: JS`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4045#issuecomment-4549409075) **weswigham** clarified that JS declaration emit in tsgo is syntactic, matching the input JS more closely, and noted that missing support for non-exported expando types may be a declaration emit bug
 * (today) **weswigham** added labels `bug`, `Domain: Declaration Emit`, `Domain: JS`, `Needs Investigation`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4045#issuecomment-4553479379) **hkleungai** expressed hope that tsgo continued to support expando types and requested a fix for Storybook CSF2 syntax

### [Issue microsoft/TypeScript-go#4046](https://github.com/microsoft/TypeScript-go/issues/4046) (Open, `Domain: Declaration Emit`)

**Behavior difference: Side\-effect imports of custom file extension are emitted by tsgo but not tsc**

*tsgo emits side-effect imports for custom file extensions in declaration files while tsc omits them.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Domain: Declaration Emit`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#4048](https://github.com/microsoft/TypeScript-go/issues/4048) (Closed, `possible improvement`)

**Behavior difference: Object key named \`new\` is double\-quoted in tsgo emit, but not in tsc emit**

*tsgo double-quotes object keys named new in emitted declaration files, unlike tsc which leaves them unquoted.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4049](https://github.com/microsoft/TypeScript-go/issues/4049) (Closed, `wontfix`)

**Cannot reference class type assigned to static member**

*In tsgo, importing a class type assigned to a static member fails because static properties aren’t recognized as exports.*

 * created by **avivkeller**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4049#issuecomment-4546522721) **DanielRosenwasser** explained that static members don’t function as type aliases in JSDoc and provided two example approaches using typedef or typeof/InstanceType to restore type meaning
 * [today](https://github.com/microsoft/TypeScript-go/issues/4049#issuecomment-4547333065) **DanielRosenwasser** said "I'll also add that in TypeScript 6.0, Other referred to the static side - basically typeof import('./dependency').Other, not the instance type (as I wrote above)."
 * **RyanCavanaugh** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4049#issuecomment-4549274448) **RyanCavanaugh** said "ref. https://github.com/microsoft/typescript-go/blob/main/CHANGES.md#values-are-no-longer-resolved-as-types-in-jsdoc-type-positions"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4049#issuecomment-4550002839) **avivkeller** said "Thank you! Sorry about opening a known wontfix!"
 * (today) **avivkeller** closed the issue

### [PR microsoft/TypeScript-go#4050](https://github.com/microsoft/TypeScript-go/pull/4050) (Closed)

**Don't use cached type node when expanding**

*Stop using cached type nodes when expanding and properly set verbosity on the reusable node builder*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4052](https://github.com/microsoft/TypeScript-go/pull/4052) (Closed, **weswigham**)

**fix\(4048\): fix declaration emit for new keyword used as property names**

*Corrects declaration file generation when 'new' is used as a property name.*

 * created by **a-tarasyuk**
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4053](https://github.com/microsoft/TypeScript-go/pull/4053) (Closed)

**Strip matching prefix in path mapping completions**

*Automatically strip matching prefixes from path mapping completions to ensure correct suggestions.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4054](https://github.com/microsoft/TypeScript-go/pull/4054) (Open)

**Fix configuration lookups and prefer saving as \`js/ts\`**

*Prefer js/ts.experimental.useTsgo over deprecated typescript settings, respect workspace specificity, migrate settings, and prevent server startup when disabled in development.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#4055](https://github.com/microsoft/TypeScript-go/issues/4055) (Open, `Needs Investigation`, **ahejlsberg**)

**Type recursion limit \(TS2589\) on recursive mapped types**

*The recursive mapped type Draft<T> triggers a TS2589 excessive recursion error when assigning a nested Conversation property due to exceeding TypeScript’s type instantiation depth*

 * created by **blickly**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4057](https://github.com/microsoft/TypeScript-go/issues/4057) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**New isolatedDeclarations error with generic \`this\` parameter inference**

*Using a generic this parameter in a method triggers a TS9008 isolatedDeclarations error under tsgo despite working in TypeScript 6.0.*

 * created by **blickly**
 * (today) **RyanCavanaugh** added labels `Needs Investigation`, `Domain: Declaration Emit`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**

### [PR microsoft/TypeScript-go#4058](https://github.com/microsoft/TypeScript-go/pull/4058) (Open)

**Reparse non\-identifier jsdoc names where possible, error otherwise**

*The parser now reparses non-identifier JSDoc names when possible and errors on unsupported nameless typedef patterns.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4549523307) **DanielRosenwasser** said "Can we give a more-specialized error message for reserved names?"

### [Issue microsoft/TypeScript-go#4059](https://github.com/microsoft/TypeScript-go/issues/4059) (Open)

**reference directive caused issue with ts\-check**

*Placing a triple-slash reference directive after a // @ts-check comment causes tsgo to bypass type-checking, effectively acting like ts-nocheck.*

 * created by **jasonlyu123**

