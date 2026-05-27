# Report for 2026-05-24 (Sunday, May 24th, 2026)

4 different users commented on 8 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#4037](https://github.com/microsoft/TypeScript-go/issues/4037) (Open, `bug`, **ahejlsberg**)

**TS2304 when a generic \(@template\) function JSDoc contains @overload**

*Generic functions documented with @template and @overload produce 'Cannot find name T' TS2304 errors in tsgo.*

 * created by **antichris**
 * (today) **ahejlsberg** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4038](https://github.com/microsoft/TypeScript-go/issues/4038) (Open, `bug`, **ahejlsberg**)

**TS2315 when using \`@template\` more than once in a file**

*tsgo misreports TS2315 'export=' is not generic when a file contains more than one JSDoc @template declaration.*

 * created by **avivkeller**
 * (today) **ahejlsberg** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4038#issuecomment-4529508062) **ahejlsberg** explained that resolveEntityName only invoked resolveAlias once and promised a PR to add multiple invocations for CommonJS modules with exported type declarations

### [Issue microsoft/TypeScript-go#4042](https://github.com/microsoft/TypeScript-go/issues/4042) (Open)

**LSP custom/initializeAPISession never responds in stdio mode \(7\.0\.0\-dev\.20260518\.1 / 20260522\.1\)**

*Calling custom/initializeAPISession in tsgo’s stdio LSP mode hangs without JSON-RPC response or socket creation*

 * created by **re-thc**
 * (today) **re-thc** closed the issue
 * (today) **re-thc** reopened the issue

### [PR microsoft/TypeScript-go#4043](https://github.com/microsoft/TypeScript-go/pull/4043) (Open)

**Resolve aliases in \`resolveEntityName\` until we find the given meaning**

*Allow resolveEntityName to follow alias chains until the desired symbol meaning is found*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#4044](https://github.com/microsoft/TypeScript-go/issues/4044) (Closed, `Working As Intended`, **weswigham**)

**Behavior difference: tsc mark class method with \`override\` keyword according to jsdoc, but tsgo fails to do so\.**

*tsgo does not include the override keyword for class methods annotated with @override, unlike tsc.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4044#issuecomment-4533873443) **a-tarasyuk** asked whether override should be stripped from declaration emit for JS files with @override jsdoc tags

### [Issue microsoft/TypeScript-go#4045](https://github.com/microsoft/TypeScript-go/issues/4045) (Open, `bug`, `Domain: Declaration Emit`, `Domain: JS`, `Needs Investigation`)

**Behavior difference: Notable gap regarding expando declaration on a function between tsc & tsgo**

*tsgo aliases bound functions without namespaces compared to tsc, causing inconsistent type emissions for both PublicInternalBinding and PublicExportedBinding.*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#4046](https://github.com/microsoft/TypeScript-go/issues/4046) (Open, `Domain: Declaration Emit`)

**Behavior difference: Side\-effect imports of custom file extension are emitted by tsgo but not tsc**

*tsgo emits side-effect imports for custom file extensions in declaration files while tsc omits them.*

 * created by **hkleungai**

