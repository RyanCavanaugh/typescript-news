# Report for 2026-06-25 (Thursday, June 25th, 2026)

8 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @WerdoxDev provided repro steps and logs in [microsoft/TypeScript-go#4392](https://github.com/microsoft/TypeScript-go/issues/4392#issuecomment-4810191860)

## Activity Summary

### [PR microsoft/TypeScript-go#4379](https://github.com/microsoft/TypeScript-go/pull/4379) (Open)

**Fix watch coalescing for FSEvents**

*Coalesce dense directory watch sets into recursive ancestor watches on FSEvents and Windows to reduce per-directory streams.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4792175080) **andrewbranch** said "In my experience, kqueue is untenable for the scale of watches we often try to register. I profiled it and it was all syscall time. Nothing to optimize."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4792182748) **andrewbranch** said "I guess, registering them in parallel would probably help, but I still don't think that's a good approach."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4792202888) **jakebailey** said "Ultimately, I guess my question is why Strada did not have major issues here, given it could only use kqueue as Node via libuv only did not do fsevents."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4804956291) **jakebailey** said "I think this PR is fine, but, I think #4447 is the wider fix; might be able to un-coalesce, even."

### [Issue microsoft/TypeScript-go#4392](https://github.com/microsoft/TypeScript-go/issues/4392) (Open, `Crash`, **DanielRosenwasser**, **andrewbranch**, **Copilot**)

**panic: cache entry not found \[recovered, repanicked\]**

*TypeScript server v7.0.0-dev panics with 'cache entry not found' while handling file open and config updates.*

 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * (yesterday) **RyanCavanaugh** set milestone to `TypeScript 7.0 Stable`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4392#issuecomment-4810191860) **WerdoxDev** confirmed the bug occurred when pressing ctrl+space for auto-complete in a monorepo and provided logs

### [PR microsoft/TypeScript-go#4431](https://github.com/microsoft/TypeScript-go/pull/4431) (Closed)

**API: add checker methods to get true and false types of a conditional type**

*Add API checker methods to fetch true and false branches of a conditional type.*

 * created by **piotrtomiak**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (later) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4437](https://github.com/microsoft/TypeScript-go/issues/4437) (Open)

**\`checkJs\` seems to default to true erroneously**

*tsgo implicitly enables checkJs by default, leading to erroneous JSDoc modifier errors in JavaScript files unless checkJs is explicitly disabled.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4794108129) **jakebailey** said "I think part of the confusion is that IIRC these are now early errors in the reparse process, at parse time, not even check errors. Perhaps they should move"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4794121041) **freshp86** asked why certain errors were suppressed when checkJs was false despite explicit configuration
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4796606071) **danyalahmed1995** noted that the errors occur during the JSDoc reparse process and asked whether validation should move or reparsed JSDoc modifiers should skip grammar diagnostics for JS/JSX
 * [today](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4804727384) **RyanCavanaugh** explained that checkJs has tristate behavior in TS 6 and illustrated it with an example showing different errors for false, unspecified, and true settings

### [Issue microsoft/TypeScript-go#4439](https://github.com/microsoft/TypeScript-go/issues/4439) (Open, `bug`, **andrewbranch**, **Copilot**)

**Feature Request: Permit backward\-compatible version checks at main export**

*Add a main package export for TypeScript 7 to enable backward-compatible version checks and avoid load errors.*

 * created by **kirkwaiblinger**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 Stable`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**

### [PR microsoft/TypeScript-go#4444](https://github.com/microsoft/TypeScript-go/pull/4444) (Open, **RyanCavanaugh**, **Copilot**)

**Handle recursive aliases in named tuple rest elements**

*Enable recursive type aliases in named tuple rest elements by extending alias resolution to ArrayType to avoid circularity errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4445](https://github.com/microsoft/TypeScript-go/pull/4445) (Closed, **andrewbranch**, **Copilot**)

**Add CJS "\." version stub entrypoint to @typescript/native\-preview**

*Add a CJS stub entrypoint as the dot export in @typescript/native-preview to expose ts.version and avoid module resolution errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4445#issuecomment-4803392648) **Copilot** removed the failing test due to the dev package.json lacking a real version number
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4446](https://github.com/microsoft/TypeScript-go/pull/4446) (Open)

**fix: Corsa differences in \`export=\` module augmentation**

*Corsa misreports TS4060 for types in namespaces exported via export= by not marking them visible during declaration emit.*

 * created by **pratheeknathani**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-4803987637) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-4803988303) **typescript-automation[bot]** announced performance test start with status and result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-4804157001) **typescript-automation[bot]** reported the requested performance run results for tsc comparing baseline and PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-4804369952) **pratheeknathani** pushed a commit removing a stale submoduleTriaged.txt entry to fix CI failures and verified tests locally

### [PR microsoft/TypeScript-go#4447](https://github.com/microsoft/TypeScript-go/pull/4447) (Open)

**Use shared FSEvents streams**

*Parcel’s watcher shares and chunks FSEvents streams to reduce stream count and prevent hitting OS limits.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4447#issuecomment-4804580045) **jakebailey** conducted testing and determined that chunking harmed performance while multiple streams remain necessary to avoid overflow, with setup time dominating

### [PR microsoft/TypeScript-go#4448](https://github.com/microsoft/TypeScript-go/pull/4448) (Open, **jakebailey**, **Copilot**)

**Fix spurious JSDoc modifier errors on object literal members**

*Skip reparsing JSDoc modifiers on object literal members to avoid spurious grammar errors*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4448#issuecomment-4804695916) **jakebailey** said "@copilot+claude-opus-4.8 Fix the PR description and title to now match the state of this change."

### [PR microsoft/TypeScript-go#4449](https://github.com/microsoft/TypeScript-go/pull/4449) (Open)

**restore JSDoc member name check for private identifier references**

*Restores the JSDoc member name validation for private identifiers in isValidReferencePosition by implementing the missing helper.*

 * created by **aamoghS**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4805882923) **jakebailey** said "This needs tests that show this does something; it might not due to reparsing"

### [PR microsoft/TypeScript-go#4450](https://github.com/microsoft/TypeScript-go/pull/4450) (Open)

**implement getContextNode for ForOf, ForIn, and Switch statements**

*Implement getContextNode support for ForOf, ForIn, and Switch statements to prevent nil returns that break cross-project find references and go-to-definition functionality*

 * created by **aamoghS**

### [Issue microsoft/TypeScript-go#4451](https://github.com/microsoft/TypeScript-go/issues/4451) (Open)

**Mapped type over any incorrectly rejects structural assignability**

*tsgo misinterprets Yup’s mapped Shape<any> type and wrongly rejects assigning ObjectSchema<MyValues> to AnyObjectSchema.*

 * created by **tmadeira**

