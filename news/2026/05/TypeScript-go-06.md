# Report for 2026-05-06 (Wednesday, May 6th, 2026)

14 different users commented on 49 different issues.

## Recommended Actions

 * Response Recommended
    * @kwonoj asked if there are diagnostic logs they could collect in [microsoft/TypeScript-go#3612](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4392365318)
    * @Netail provided reproduction steps and video in [microsoft/TypeScript-go#3638](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4392650518)
    * @kbrooks asked for a review when someone has bandwidth in [microsoft/TypeScript-go#3664](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4393623807)
    * @adavila0703 was asked to agree to the Contributor License Agreement in [microsoft/TypeScript-go#3728](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-4390943530)

## Activity Summary

### [Issue microsoft/TypeScript-go#3480](https://github.com/microsoft/TypeScript-go/issues/3480) (Closed, `Needs Investigation`, **weswigham**)

**Missing error about jsx\-runtime package**

*Error messages for missing jsx-runtime package are not reported in legacy module detection tests for react-jsx and react-jsxdev*

 * created by **RyanCavanaugh**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3480#issuecomment-4291050128) **jakebailey** said "This comes down to us not detecting that this is a module due to other changes, which then changes how JSX behaves, IIRC"
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3481](https://github.com/microsoft/TypeScript-go/issues/3481) (Open, `help wanted`)

**Corsa differences in \`export=\` module augmentation**

*Corsa changes how export= module augmentation works, causing differences in exported name visibility.*

 * created by **RyanCavanaugh**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4291838613) **ahejlsberg** said "The issue in augmentExportEquals2.errors.txt.diff is actually that the test is broken. There are two // @filename: file3.ts in a row, which we apparently no longer handle."
 * (today) **RyanCavanaugh** added label `help wanted`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#3484](https://github.com/microsoft/TypeScript-go/issues/3484) (Closed, `bug`, **iisaduan**)

**Static property conflicts with built\-in Function properties \(TS2699\) no longer reported when useDefineForClassFields is false**

*TypeScript does not report TS2699 errors for static class properties conflicting with built-in Function properties when useDefineForClassFields is false.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3489](https://github.com/microsoft/TypeScript-go/issues/3489) (Open, `bug`, **iisaduan**)

**Lowercase\<"İ"\>\` differs between tsgo and tsc \(Go strings\.ToLower vs JS String\.prototype\.toLowerCase\)**

*tsgo’s Lowercase intrinsic uses Go’s strings.ToLower rather than ECMAScript’s full Unicode case mapping, causing mismatched lowercase results for characters like 'İ'*

 * created by **tomquist**
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3492](https://github.com/microsoft/TypeScript-go/issues/3492) (Closed, `Type Ordering`)

**tsgo rejects unknown JSX props that appear before a \`{\.\.\.spread}\` and are accepted by tsc 6\.0**

*tsgo incorrectly flags unknown JSX props before a spread operator as errors while TypeScript 6.0 accepts them*

 * created by **tomquist**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3492#issuecomment-4298335966) **jakebailey** explained that the code errored previously, noted a non-ideal fix for preserving spread ordering, and suggested avoiding the error by casting the object
 * **RyanCavanaugh** added label `Type Ordering`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3492#issuecomment-4390392921) **RyanCavanaugh** explained that error span shifts are allowable due to determinism changes between versions
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3504](https://github.com/microsoft/TypeScript-go/issues/3504) (Closed, `Crash`, **weswigham**, **Copilot**)

**Crash in declaration emit for JavaScript Test262 reserved\-words**

*Emitting declaration files panics with a nil pointer dereference when processing JavaScript Test262 reserved-word expando assignments.*

 * created by **turadg**
 * **turadg** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3504#issuecomment-4390505722) **RyanCavanaugh** provided a minimal repro including code and tsconfig configuration
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, assigned to **weswigham**, **Copilot**, **RyanCavanaugh**, and unassigned **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3508](https://github.com/microsoft/TypeScript-go/issues/3508) (Open, `Needs Investigation`, **gabritto**)

**Corsa no longer emits the TS\-1 internal diagnostic about pre\-emit/post\-emit diagnostic count mismatches**

*Corsa no longer emits TS-1 diagnostics for mismatched pre-emit and post-emit diagnostic counts in certain test files.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**

### [Issue microsoft/TypeScript-go#3511](https://github.com/microsoft/TypeScript-go/issues/3511) (Open, `Needs Investigation`, **weswigham**)

**Unicode escapes in identifier names now displayed as literal characters**

*Identifier names containing Unicode escape sequences are now shown as their literal characters in conformance test outputs.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3514](https://github.com/microsoft/TypeScript-go/issues/3514) (Closed, `wontfix`)

**Illegally constructing a private/protected constructor from outside the class does not resolve to \`any\` for non\-generic classes**

*tsgo preserves types for non-generic classes with private constructors but still resolves generic classes to any, unlike TypeScript 6.0.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3514#issuecomment-4300077335) **Andarist** noted that baseline diffs already show this and suggested treating the change as intentional
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3514#issuecomment-4300374534) **Bertie690** noted that the inconsistency was likely accidental as `GenericA` remained typed as `any` and observed that error-suppression tools undermined the rule against making assumptions about code with errors
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3514#issuecomment-4305880059) **RyanCavanaugh** explained that both outcomes are defensible and no invariant exists for types from errorful expressions
 * **RyanCavanaugh** added label `wontfix`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3548](https://github.com/microsoft/TypeScript-go/issues/3548) (Closed, `bug`, **weswigham**)

**Baselines: Decorator metadata reflects stable union type ordering**

*Reflect.getMetadata design:type for T|null unions now reports the non-null type instead of Object due to updated decorator metadata ordering.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3557](https://github.com/microsoft/TypeScript-go/issues/3557) (Closed, `Domain: Parser`, `Needs Investigation`, **sandersn**, **Copilot**)

**Baselines: @satisfies tag handling changes: functions become const declarations**

*Functions annotated with @satisfies now become declare const arrow functions with changed parameter types and added @param/@satisfies annotations*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Parser`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **sandersn**

### [Issue microsoft/TypeScript-go#3562](https://github.com/microsoft/TypeScript-go/issues/3562) (Closed, `Domain: Type Checking`, `Needs Investigation`, **sandersn**, **jakebailey**, **Copilot**)

**Baselines: JSDoc module namepath module:A emits as unresolved module instead of any**

*JSDoc module namepath syntax (module:A) now emits an unresolved module rather than any, producing type errors.*

 * created by **RyanCavanaugh**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3562#issuecomment-4315989334) **ahejlsberg** said "Seems like we should more gracefully handle JSDoc namepaths (even if we don't support them)."
 * **ahejlsberg** added label `Domain: Type Checking`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **sandersn**

### [Issue microsoft/TypeScript-go#3563](https://github.com/microsoft/TypeScript-go/issues/3563) (Open, **ahejlsberg**)

**Baselines: definiteAssignment shorthand in object literal loses optional modifier**

*Optional method properties in object literal shorthand lose their optional modifier when emitted with definite assignment assertions.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** assigned to **ahejlsberg**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3563#issuecomment-4393068890) **ahejlsberg** asked whether to handle '?' modifiers on object literal properties and noted uncertainty about declaration emit behavior

### [Issue microsoft/TypeScript-go#3564](https://github.com/microsoft/TypeScript-go/issues/3564) (Open, `Domain: Type Checking`, `Needs Investigation`, **ahejlsberg**)

**Baselines: Generic function parameter inference change**

*Baseline tests updated to reflect generic function parameter inference changing x3’s type from any[] to any[][].*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Type Checking`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#3573](https://github.com/microsoft/TypeScript-go/pull/3573) (Closed)

**Optimize type variable scope map cloning with CoW**

*Reintroduce copy-on-write for type variable scope maps to cut 720k allocations in the test suite.*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3573#issuecomment-4383719204) **jakebailey** said "Not a bad idea to formalize this, I'll give it a go"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3575](https://github.com/microsoft/TypeScript-go/pull/3575) (Closed)

**Avoid over\-expanding recursive constraints in \`getBaseSignature\`**

*Prevent excessive expansion of recursive type constraints in the getBaseSignature function.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3575#issuecomment-4392766649) **ahejlsberg** said "Looks like we need conformance/genericFunctionParameters.js.diff removed from submoduleTriaged.txt."

### [Issue microsoft/TypeScript-go#3585](https://github.com/microsoft/TypeScript-go/issues/3585) (Closed, `wontfix`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Remove extraneous \`declare\` in \.d\.ts output to better match strada**

*Remove extraneous declare modifiers from .d.ts output for both TypeScript and JavaScript*

 * created by **RyanCavanaugh**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3585#issuecomment-4320288542) **Andarist** noted that a change around ensureModifiers/maskModifierFlags wouldn't quite eliminate all diverging declare modifiers and linked a comparison
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3596](https://github.com/microsoft/TypeScript-go/issues/3596) (Closed, `Needs Investigation`, **andrewbranch**, **Copilot**)

**TS2883 regression in \-\-build with project references on inferred export from referenced package**

*tsgo --build now fails with TS2883 on inferred exports referencing types from a project-referenced package in a pnpm monorepo*

 * created by **kbrooks**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**

### [Issue microsoft/TypeScript-go#3611](https://github.com/microsoft/TypeScript-go/issues/3611) (Open, `bug`, **jakebailey**, **johnfav03**)

**Elevated CPU usage in \`\-\-watch\` mode when idle \(compared to tsc\)**

*tsgo --watch mode consistently consumes 5-10% CPU while idle, whereas tsc --watch mode remains at 0%.*

 * created by **alexswan93**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3611#issuecomment-4339900462) **DanielRosenwasser** described that the current strategy was naive polling at a fixed frequency and mentioned that @jakebailey was implementing perf infrastructure in the typescript-go repo
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, assigned to **andrewbranch**, **jakebailey**, **johnfav03**, and unassigned **andrewbranch**

### [Issue microsoft/TypeScript-go#3612](https://github.com/microsoft/TypeScript-go/issues/3612) (Open, `Needs More Info`)

**Intermittent tsgo build failures with incorrect inferences**

*tsgo intermittently misinfers arktype-inferred referenced types as empty objects, causing build failures in incremental builds*

 * created by **kwonoj**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4330636333) **jakebailey** suggested trying --checkers 1, --singleThreaded, and disabling incremental mode, and asked if the code is public or could be shared under NDA
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4330791306) **kwonoj** suggested trying --checkers 1 or --singleThreaded, noted one fixed the issue but forgot which, said the code is private and asked if they'd sign an NDA
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4391736486) **RyanCavanaugh** said "We're definitely going to need a repro of some sort."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4391958805) **RyanCavanaugh** reported being unable to reproduce the intermittent build failure after extensive testing across multiple reproduction strategies
 * [today](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4392365318) **kwonoj** acknowledged difficulty diagnosing without a repro and asked if there were diagnostic logs to collect
 * [today](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4392876439) **RyanCavanaugh** suggested setting a coding agent to produce a minimal shareable version and linked a relevant TypeScript Maintainer Skills resource
 * [today](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4392883922) **kwonoj** said "Build time is somewhat larger, but I can spin a remote box to keep spinning. Thanks for the suggestion, will give it a go and come back later."

### [Issue microsoft/TypeScript-go#3615](https://github.com/microsoft/TypeScript-go/issues/3615) (Closed, **andrewbranch**, **Copilot**)

**Server stops responding after \`Running scheduled diagnostics refresh\`**

*The TypeScript language server hangs after running scheduled diagnostics refresh in large monorepos with many open editors and file system event bursts.*

 * (1 week ago) **andrewbranch** assigned to **Copilot**, **andrewbranch**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3628](https://github.com/microsoft/TypeScript-go/pull/3628) (Closed, **andrewbranch**, **Copilot**)

**Fix server hang after "Running scheduled diagnostics refresh"**

*Convert scheduled diagnostics refresh to non-blocking and introduce per-request timeouts, watcher deduplication, and registry encapsulation to prevent server deadlocks.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4383400405) **Copilot** described moving deduplication into WatchedFiles and updating Watchers() to deduplicate via slices.Compact and removing updateWatch logic
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4383467093) **andrewbranch** said "@copilot move mutex locking into watchRegistry methods."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4383561544) **Copilot** moved mutex locking into watchRegistry methods and removed external lock calls from session.go
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3638](https://github.com/microsoft/TypeScript-go/issues/3638) (Closed, `Domain: Editor`, `Needs Investigation`, **gabritto**)

**Cannot find name html element\.**

*Closing div tags in .tsx files intermittently trigger “Cannot find name 'div'” errors in VS Code’s TypeScript language server until it’s restarted.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4335853459) **jakebailey** said "We would really need a repro, or at least some logs"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4335893311) **Netail** explained that the issue occurred randomly across multiple TSX files and offered to provide logs
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4351168228) **Netail** attached log file and described that the error occurred spontaneously on a large TSX file after idling
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4391323874) **RyanCavanaugh** said "Log does indeed show something weird happen, but it's super hard to guess what's going on. Log + repo might be enough to reconstruct what's happening."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4391619315) **Netail** noted logs show weird behavior but reproduction was unclear, speculated an LSP re-indexing issue related to pnpm, and said they would try more things
 * [today](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4392256211) **Netail** said "Okay, was able to reproduce it in https://github.com/Netail/repro-typescript-go-unknown-html-element. In the page.tsx (ts6 + tsgo vscode extension) Now I have to figure out the repro steps"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4392650518) **Netail** provided reproduction steps and a video demonstrating the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4392820370) **RyanCavanaugh** said "Confirmed locally, investigating. Great repro, thanks!"
 * (today) **RyanCavanaugh** added label `Needs Investigation`, removed label `Needs More Info`, set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4392958734) **Netail** thanked Ryan and wished him luck
 * [today](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4393922780) **RyanCavanaugh** added a fourslash regression test verifying hover then diagnostics on a JSX intrinsic element
 * (today) **RyanCavanaugh** assigned to **gabritto**, and unassigned **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4394496405) **jakebailey** said "I suspect #3435 would fix this by way of not sharing checkers."

### [Issue microsoft/TypeScript-go#3659](https://github.com/microsoft/TypeScript-go/issues/3659) (Open, `bug`)

**Behavior difference: JSDoc comments are stripped for mapped types**

*Mapped types in TypeScript 7 beta strip JSDoc comments from original properties, unlike TypeScript 6.0.3.*

 * created by **andrewzolotukhin**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3659#issuecomment-4346021402) **Withered-Flower-0422** said "Maybe related to #3405 ?"
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`

### [PR microsoft/TypeScript-go#3664](https://github.com/microsoft/TypeScript-go/pull/3664) (Closed)

**Align dependency symlink handling with TS6 for module specifiers**

*Align tsgo’s dependency symlink cache with TypeScript 6 by using normal module resolution to respect paths mappings in declaration emits.*

 * created by **kbrooks**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4347464727) **kbrooks** agreed with the policy service and indicated affiliation with Snap Inc.
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4347528448) **kbrooks** agreed to policy request and specified company as Snap Inc.
 * [today](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4393623807) **kbrooks** asked for someone to review when they had bandwidth

### [Issue microsoft/TypeScript-go#3666](https://github.com/microsoft/TypeScript-go/issues/3666) (Closed, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo does not \(fully\) respect jsdoc \`@extend\` clause**

*tsgo fails to report mismatched JSDoc @extends errors for JS classes, unlike tsc which correctly flags them.*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3671](https://github.com/microsoft/TypeScript-go/pull/3671) (Closed)

**Fix JSDoc \`@extends\` mismatch diagnostics for property access bases**

*Corrects JSDoc @extends mismatch diagnostics for cases where the base type is a property access expression.*

 * created by **Andarist**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3687](https://github.com/microsoft/TypeScript-go/issues/3687) (Open, `possible improvement`)

**No compiled packages for netbsd**

*No compiled @typescript/native-preview package is available for NetBSD x64, causing an error.*

 * created by **mudcovered**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3687#issuecomment-4375095282) **jakebailey** explained that builds currently match VS Code and that supporting additional platforms will be considered but nightly builds for all platforms are unlikely at this time
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#3689](https://github.com/microsoft/TypeScript-go/issues/3689) (Open, `Needs Investigation`, **andrewbranch**)

**project reference resolution fails when workspace is opened through a symlinked root path**

*tsgo fails to resolve project references and reports TS2307 errors when the workspace root is opened via a symlink*

 * created by **Zzzen**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692) (Open, `Needs More Info`)

**Excessive CPU usage**

*WebStorm’s ts-go server often consumes 80-100% CPU when adding new imports in a monorepo frontend until restarted.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4374556539) **jakebailey** said "I have no idea how WebStorm works, but in VS Code, we have a command that can take a profile and you could upload that."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4374635334) **andrewbranch** explained that briefly spiking to 80–100% CPU usage when adding imports was not unusual, and that only sustained high usage would be abnormal
 * [today](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4385893760) **Jelcoo** mentioned that the issue did not occur in VS Code, asked how to manually capture a profile, and noted that CPU spikes halted autocomplete
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4391545891) **RyanCavanaugh** said "We need some clue as to what WebStorm is doing differently - sending different requests, etc?"

### [Issue microsoft/TypeScript-go#3694](https://github.com/microsoft/TypeScript-go/issues/3694) (Closed, `wontfix`, **DanielRosenwasser**, **iisaduan**, **Copilot**)

**Behavior difference: jsdoc \`@param\` referencing object attribute value throws TS2749 in tsc but throws TS2503 in tsgo**

*When using jsdoc @param to reference an object property, tsgo throws TS2503 instead of TS2749 like tsc*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3694#issuecomment-4391127074) **ahejlsberg** acknowledged the namespace error was not better than the typeof error in JSDoc @param context and explained that Corsa lacked the complex lookup logic for JS files in Strada, noting the Corsa error resembled a TypeScript error when using map.foo as a type
 * (today) **ahejlsberg** added label `wontfix`, removed label `Needs Investigation`, and removed from milestone `TypeScript 7.0 RC`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3719](https://github.com/microsoft/TypeScript-go/issues/3719) (Open, `bug`, **iisaduan**)

**Support localized user\-facing strings in VS Code extension**

*Add localization support by moving user-facing strings into package.nls.json and using vscode-l10n tools.*

 * created by **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3719#issuecomment-4383830006) **jakebailey** said "You mean for extension strings, right?"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3721](https://github.com/microsoft/TypeScript-go/issues/3721) (Closed, `wontfix`)

**tsgo drops re\-exported names when declare module combines export = X with a type\-only export**

*tsgo incorrectly omits re-exported members when an export = X module augmentation includes a type-only export.*

 * created by **vasilev-alex**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3721#issuecomment-4389411834) **ahejlsberg** explained that removing skipLibCheck reveals errors due to mixing export = with regular exports and suggested properly augmenting the module by making the declaration file a module with export {} and a declare module 'react'
 * **RyanCavanaugh** added label `wontfix`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3723](https://github.com/microsoft/TypeScript-go/pull/3723) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix nil pointer in transformExpandoAssignment for element access expressions**

*Replace left.Name().Text() with the computed property variable to prevent nil pointer panics on JS expando element access assignments.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3724](https://github.com/microsoft/TypeScript-go/issues/3724) (Open, `wontfix`, **ahejlsberg**)

**Behavior difference: tsgo fails to typecheck self\-referential identity in a classic linked list**

*tsgo reports an implicit any error for a self-referential node property in a JavaScript linked list that TypeScript 6 accepts.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3724#issuecomment-4392273353) **ahejlsberg** explained that self-referential assignments widen the inferred type to any and suggested adding a type annotation
 * (today) **ahejlsberg** added label `wontfix`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3724#issuecomment-4394184138) **hkleungai** described how adding a callback-based update method allowed tsgo to infer types correctly and contrasted this behavior with a similar issue regarding self-references in the same scope
 * [today](https://github.com/microsoft/TypeScript-go/issues/3724#issuecomment-4394209685) **hkleungai** mentioned that while type annotations are necessary, they’d prefer to rely on tsgo’s type inference to minimize annotations

### [Issue microsoft/TypeScript-go#3725](https://github.com/microsoft/TypeScript-go/issues/3725) (Open, `possible improvement`, **DanielRosenwasser**, **Copilot**)

**Preserve more context in cross\-project stack traces**

*Cross-project error handling in codelens resolution discards original stack trace details, obscuring the underlying failure cause.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#3726](https://github.com/microsoft/TypeScript-go/pull/3726) (Open, **DanielRosenwasser**, **Copilot**)

**Preserve original stack traces in cross\-project panic handling**

*Add a PanicWithStack wrapper to record and rethrow the original panic stack trace in cross-project worker recovery.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4391760347) **DanielRosenwasser** outlined steps to intentionally trigger a new panic, report the resulting stack trace in telemetry, and add a test for the stack sanitizer
 * [today](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4391869776) **Copilot** demonstrated telemetry stack trace before and after the fix, preserved original crash site, and added a baseline test
 * [today](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4392374682) **DanielRosenwasser** asked whether duplicate parts of the stack trace could be omitted
 * [today](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4392475333) **Copilot** fixed NewPanicWithStack to strip recovery infrastructure frames from the captured stack to prevent duplication in telemetry output

### [Issue microsoft/TypeScript-go#3727](https://github.com/microsoft/TypeScript-go/issues/3727) (Open, `Domain: Editor`, `possible improvement`)

**Unify tsdk between built\-in and native preview extensions**

*Share the built-in tsdk setting with the native preview and choose the TypeScript server based on useTsGo and tsdk directory.*

 * created by **DanielRosenwasser**
 * (today) **RyanCavanaugh** added labels `possible improvement`, `Domain: Editor`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#3728](https://github.com/microsoft/TypeScript-go/pull/3728) (Open)

**Fix keyof deferred for non\-generic substitution types \(\#2186\)**

*Resolve keyof immediately for non-generic substitution types, fixing indexed access assignability and unsimplified quick info.*

 * created by **adavila0703**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-4390943530) **adavila0703** quoted the Contributor License Agreement and instructions for agreeing

### [PR microsoft/TypeScript-go#3729](https://github.com/microsoft/TypeScript-go/pull/3729) (Open, **RyanCavanaugh**, **Copilot**)

**Remove extraneous \`declare\` in \.d\.ts output to better match strada**

*Strip redundant ambient declare modifiers from all .d.ts outputs to align with strada behavior.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3730](https://github.com/microsoft/TypeScript-go/pull/3730) (Closed, **andrewbranch**, **Copilot**)

**Fix TS2883 regression in \-\-build with project references on inferred export from non\-index file**

*Add fallback module specifier generation in --build to prevent TS2883 errors for inferred types from non-index files in project references*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#3731](https://github.com/microsoft/TypeScript-go/pull/3731) (Closed)

**Handle config file diagnostics updates via file watching**

*Enable file-watching for tsconfig.json to update diagnostics for both open and closed projects, ignoring configs outside the workspace or in node_modules.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#3732](https://github.com/microsoft/TypeScript-go/pull/3732) (Closed)

**fix\(3560\): fix nested export variable transformation in if/labeled statements**

*Correct nested export variable transformation in if and labeled statements.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#3733](https://github.com/microsoft/TypeScript-go/issues/3733) (Open, `Domain: Editor`, `Needs More Info`)

**No autocomplete for local symbols and some global types when creating a new file**

*VS Code fails to autocomplete or auto-import local symbols and ESNext types like Temporal in new TypeScript files until restart.*

 * created by **jansedlon**
 * **jansedlon** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#3734](https://github.com/microsoft/TypeScript-go/issues/3734) (Closed, `Crash`, `Needs More Info`)

**Entering "ai\.messages\.find\(m =\> m\.\)" will cause the language server to crash\.**

*Typing ai.messages.find(m => m.) triggers an internal token-end mismatch panic that crashes the language server*

 * created by **ShenHongFei**
 * **ShenHongFei** added label `Crash`
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3735](https://github.com/microsoft/TypeScript-go/issues/3735) (Closed)

**Behavior difference: tsgo fails to emit error on class field's unmatched params between jsdoc & js code**

*tsgo reports unmatched JSDoc '@param' errors for methods but not for class field arrow functions, unlike TypeScript.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3735#issuecomment-4398617779) **a-tarasyuk** said "@hkleungai could you add simplified repro? Thanks "
 * [later](https://github.com/microsoft/TypeScript-go/issues/3735#issuecomment-4398629943) **hkleungai** said "Sorry just notice that. "
 * [later](https://github.com/microsoft/TypeScript-go/issues/3735#issuecomment-4398645120) **a-tarasyuk** said "Thanks, I’ll check the issue "

### [PR microsoft/TypeScript-go#3736](https://github.com/microsoft/TypeScript-go/pull/3736) (Closed, **jakebailey**, **Copilot**)

**Investigate format crash during auto\-import completion resolve**

*Resolving auto-import completions crashes the Go language server due to assertion failures from mutated node positions during formatting*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

