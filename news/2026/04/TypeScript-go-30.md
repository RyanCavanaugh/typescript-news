# Report for 2026-04-30 (Thursday, April 30th, 2026)

13 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @hkleungai suggested pushing subtle diff fixes to the Post 7.0 milestone in [microsoft/TypeScript-go#3665](https://github.com/microsoft/TypeScript-go/issues/3665#issuecomment-4355450508)
    * @hexsprite asked to confirm the intended compatibility contract and whether a default resolution change should be implemented in [microsoft/TypeScript-go#3674](https://github.com/microsoft/TypeScript-go/issues/3674#issuecomment-4356767783)

## Activity Summary

### [Issue microsoft/TypeScript-go#2186](https://github.com/microsoft/TypeScript-go/issues/2186) (Open, `bug`, **gabritto**)

**Broken assignability and quick info due to erroneously deferring keyof T since \#51621**

*Erroneously deferring keyof T since PR 51621 causes unsimplified quick info and invalid type assignments.*

 * (1 month ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, removed from milestone `TypeScript 7.0 RC`, and unassigned **gabritto**
 * **gabritto** assigned to **gabritto**

### [Issue microsoft/TypeScript-go#2683](https://github.com/microsoft/TypeScript-go/issues/2683) (Closed, `bug`, **gabritto**)

**TS2590: "Expression produces a union type that is too complex to represent" on generics types**

*A generic type union in the @regle monorepo triggers TS2590 errors due to overly complex inferred types in newer TypeScript versions*

 * (1 month ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-4354685818) **gabritto** said "@victorgarciaesgi do you still have the repro for this? I tried accessing https://github.com/victorgarciaesgi/regle/tree/FRONT/experimental/tsgo and I'm getting a file not found error."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-4354699795) **victorgarciaesgi** merged the changes into main, found workarounds, and fixed the problem through dichotomy
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3546](https://github.com/microsoft/TypeScript-go/issues/3546) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Declaration emit doesn't property handle CJS imports**

*tsgo’s declaration emitter for CommonJS modules omits necessary import statements, resulting in incorrect .d.ts output.*

 * (1 week ago) **ahejlsberg** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3546#issuecomment-4309229554) **weswigham** referenced PR #3541 as already fixing the issue
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3613](https://github.com/microsoft/TypeScript-go/issues/3613) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behaviour difference: merging \`interface\`s with identically named getter/setter pair and field**

*Merging interfaces with identical getter/setter and property definitions triggers duplicate identifier errors in tsgo but not in TypeScript 6.0.*

 * created by **mcpower**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3613#issuecomment-4340199480) **ahejlsberg** said "Strada doesn't really get this one right either. If you reverse the two interface declarations, Strada also errors. Corsa is at least consistent here in that it always errors."
 * (today) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3613#issuecomment-4354600393) **ahejlsberg** said "We want to permit accessor and property declarations with the same name as long as they occur in seperate type declarations. Neither Strada nor Corsa gets this right in all cases. I will put up a fix."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3614](https://github.com/microsoft/TypeScript-go/pull/3614) (Closed)

**fix\(3613\): allow prop–accessor merging in interfaces**

*Allow property accessor merging in interfaces to support combined getter and setter declarations.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3614#issuecomment-4354610464) **ahejlsberg** said "Unfortunately this isn't the right fix. Like Strada, it only gets it right in some cases."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3614#issuecomment-4354652897) **a-tarasyuk** said "@ahejlsberg, do you mean this change applies only to cases where the accessors are declared before the property signature?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3614#issuecomment-4354836750) **ahejlsberg** affirmed that the change applies only to cases where the accessors are declared before the property signature
 * (today) **a-tarasyuk** closed the issue

### [Issue microsoft/TypeScript-go#3635](https://github.com/microsoft/TypeScript-go/issues/3635) (Closed, `Crash`)

**When entering "\<" in it, it will panic**

*Typing '<' triggers a panic in the TypeScript language server’s signatureHelp handler due to a 'Not a subspan' assertion failure.*

 * created by **liy010**
 * **liy010** added label `Crash`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3636](https://github.com/microsoft/TypeScript-go/pull/3636) (Closed)

**Fix signature help crash in WIP JSX text on opening \`\<\`**

*Resolve a crash in TypeScript signature help triggered by typing an opening “<” in work-in-progress JSX text*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3636#issuecomment-4338030726) **andrewbranch** said "Is this fix a missing port from Strada? It's always helpful to know what the root cause is if Strada doesn't crash/error, because there could be more stuff that's wrong or missing deeper in the stack."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3636#issuecomment-4338285175) **DanielRosenwasser** suggested that Strada discarded the << token in createChildren/addSyntheticNodes because its end exceeded the containing node's end position
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3636#issuecomment-4339385269) **Andarist** recalled that the children syntax list was reparsed on demand in Strada, agreed that the `textPos <= end` check prevented the issue, reconsidered a similar bounds check, and confirmed that Strada missed the first token in node.getChildren() due to that check
 * [today](https://github.com/microsoft/TypeScript-go/pull/3636#issuecomment-4354599699) **DanielRosenwasser** said "Thanks!"
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3665](https://github.com/microsoft/TypeScript-go/issues/3665) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: jsdoc typing on child class member overrides parent class's type in tsgo but not in tsc**

*tsgo incorrectly reports an error when a child class’s JSDoc-typed state property overrides its parent class’s type, while tsc accepts it.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3665#issuecomment-4354512469) **Andarist** described that the error matched the old TypeScript compiler behavior and noted that an implicitly inferred derived class type shouldn’t override an explicitly typed base property
 * [today](https://github.com/microsoft/TypeScript-go/issues/3665#issuecomment-4355450508) **hkleungai** argued that even though TS7 is a native port on TS6, subtle type-checking discrepancies were worth fixing and suggested scheduling fixes for the Post 7.0 milestone

### [Issue microsoft/TypeScript-go#3667](https://github.com/microsoft/TypeScript-go/issues/3667) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Assigning array to uninitialized class members yields different error on tsc & tsgo**

*Assigning arrays to uninitialized class members in JavaScript triggers different implicit any and type inference errors in tsc vs tsgo.*

 * created by **hkleungai**
 * (later) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3667#issuecomment-4359947311) **ahejlsberg** noted that Strada handled self-referential this.xxx assignments and suggested porting that code while ignoring such assignments instead of typing them as any

### [Issue microsoft/TypeScript-go#3668](https://github.com/microsoft/TypeScript-go/issues/3668) (Open, `Domain: Editor`, **johnfav03**)

**Enable/Disable Native Preview commands don't work when user & workspace settings are both configured**

*Disabling native preview with conflicting user and workspace js/ts.experimental.useTsgo settings ignores workspace override, causing duplicate results and no enable command.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3669](https://github.com/microsoft/TypeScript-go/pull/3669) (Closed)

**Add TS\_GO\_DEBUG\_STACK\_LIMIT to Copilot workflow**

*Add TS_GO_DEBUG_STACK_LIMIT to the Copilot workflow to allow all tests to pass and limit recursion.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3670](https://github.com/microsoft/TypeScript-go/pull/3670) (Open)

**Watcher build mode efficiency updates**

*Refactors tsc --build --watch to use a shared FileWatcher and trackingVFS structure, reducing code duplication and redundant dependency scanning.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#3671](https://github.com/microsoft/TypeScript-go/pull/3671) (Closed)

**Fix JSDoc \`@extends\` mismatch diagnostics for property access bases**

*Corrects JSDoc @extends mismatch diagnostics for cases where the base type is a property access expression.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3672](https://github.com/microsoft/TypeScript-go/pull/3672) (Closed)

**Fix checks for disallowed property/accessor duplicate declarations**

*Prevent duplicate property declarations and combined accessor–property definitions within the same type declaration.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3672#issuecomment-4356092604) **jakebailey** said "Probably the new diffs can be marked as accepted, since they are intentional?"
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3673](https://github.com/microsoft/TypeScript-go/pull/3673) (Open, **RyanCavanaugh**, **Copilot**)

**Bound \`createAnonymousTypeNodeEx\` reuse for recursive instantiation expression types**

*Wrap tryReuseExistingNonParameterTypeNode in createAnonymousTypeNodeEx with a visitedTypes guard to avoid infinite recursion on recursive instantiation expression types*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3674](https://github.com/microsoft/TypeScript-go/issues/3674) (Closed)

**TS2305 on named import from ambient \`declare module\` that uses \`export \* from\`**

*tsgo fails to re-export named symbols from an ambient module using export * from, causing TS2305 errors absent in tsc.*

 * created by **jordanbbaker**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3674#issuecomment-4356767783) **hexsprite** reproduced the issue locally, identified bundler default resolution as the cause of star-export failure, and outlined a plan to add a regression test, confirm compatibility semantics, patch default resolution, avoid special-case workarounds, and run tests
 * [today](https://github.com/microsoft/TypeScript-go/issues/3674#issuecomment-4356774930) **jakebailey** said "You need to be testing with TS 6.0, not 5.9; we are not aiming for compat with 5.9 or anything deprecated in 6.0."
 * (today) **jordanbbaker** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3674#issuecomment-4356788308) **hexsprite** said "@jakebailey thanks for the response, yes I just realized that as well!"

