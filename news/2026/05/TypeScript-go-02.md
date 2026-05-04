# Report for 2026-05-02 (Saturday, May 2nd, 2026)

7 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @birkskyum provided repro steps as requested in [microsoft/TypeScript-go#3688](https://github.com/microsoft/TypeScript-go/issues/3688#issuecomment-4366254698)
    * @Jelcoo provided TS server settings screenshot in [microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4365884783)
    * @Jelcoo provided additional context on the issue’s occurrence in [microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4365889287)

## Activity Summary

### [PR microsoft/TypeScript-go#3684](https://github.com/microsoft/TypeScript-go/pull/3684) (Closed)

**ls/semantictokens: skip multi\-line tokens instead of panicking**

*Skip multi-line LSP semantic tokens in the language server to avoid panics.*

 * created by **SAY-5**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3684#issuecomment-4363050752) **jakebailey** critiqued the proposed fix for masking the root cause and requested adding a reproducing test after #3483
 * [today](https://github.com/microsoft/TypeScript-go/pull/3684#issuecomment-4364438002) **SAY-5** closed the issue per @jakebailey's read and agreed to defer a proper parser fix
 * (today) **SAY-5** closed the issue

### [Issue microsoft/TypeScript-go#3687](https://github.com/microsoft/TypeScript-go/issues/3687) (Open)

**No compiled packages for netbsd**

*No compiled @typescript/native-preview package is available for NetBSD x64, causing an error.*

 * created by **mudcovered**

### [Issue microsoft/TypeScript-go#3688](https://github.com/microsoft/TypeScript-go/issues/3688) (Open)

**Behavior difference: const T extends string = string binds to default instead of inferring never**

*tsgo's native preview defaults generic T to string instead of inferring never, causing via's conditional type to error.*

 * created by **birkskyum**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3688#issuecomment-4365074002) **jakebailey** said "Have you tested with --stableTypeOrdering in 6.0?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3688#issuecomment-4366254698) **birkskyum** tested various compiler commands including tsc and tsgo with and without stableTypeOrdering and found the type-check divergence persisted

### [Issue microsoft/TypeScript-go#3689](https://github.com/microsoft/TypeScript-go/issues/3689) (Open)

**project reference resolution fails when workspace is opened through a symlinked root path**

*tsgo fails to resolve project references and reports TS2307 errors when the workspace root is opened via a symlink*

 * created by **Zzzen**

### [PR microsoft/TypeScript-go#3690](https://github.com/microsoft/TypeScript-go/pull/3690) (Open)

**fix: handle symlink workspace roots in project reference redirects**

*Improve project reference redirects to correctly handle symlinked workspace roots.*

 * created by **Zzzen**

### [Issue microsoft/TypeScript-go#3691](https://github.com/microsoft/TypeScript-go/issues/3691) (Open, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Assigning \`Object\.values\(obj\)\` to \`obj\[field\]\` gives error on tsgo but not on tsc**

*Assigning Object.values(obj) to a property triggers a self-referential initialization type error in tsgo but not in tsc*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692) (Open)

**Excessive CPU usage**

*WebStorm’s ts-go server often consumes 80-100% CPU when adding new imports in a monorepo frontend until restarted.*

 * created by **Jelcoo**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4365884783) **Jelcoo** shared WebStorm TypeScript server settings screenshot
 * [later](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4365889287) **Jelcoo** said "While writing this issue I was working on https://github.com/calagopus/panel/commit/2db0200f2c03ab2174db6f012363fe0a49a7c967, but it has been happening with all sorts of other changes."

### [Issue microsoft/TypeScript-go#3693](https://github.com/microsoft/TypeScript-go/issues/3693) (Open)

**Behavior difference: Exporting object literal from js file emits object literal type in tsgo, as opposed to \`namespace\` in tsc\.**

*tsgo exports JavaScript object literals as literal types instead of namespaces like tsc, and this behavior difference (along with optional omission of @satisfies JSDoc comments) should be documented in CHANGES.md.*

 * created by **hkleungai**

