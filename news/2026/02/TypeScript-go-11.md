# Report for 2026-02-11 (Wednesday, February 11th, 2026)

12 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @davidjbng asked if the change is expected while upgrading to tsgo or will be fixed in TypeScript 7 in [microsoft/TypeScript-go#2698](https://github.com/microsoft/TypeScript-go/issues/2698#issuecomment-3886882717)

## Activity Summary

### [Issue microsoft/TypeScript-go#2253](https://github.com/microsoft/TypeScript-go/issues/2253) (Closed, `Domain: JS`, `Crash`, **Copilot**)

**Crash completing beginning of property name when preceded by JSDoc**

*Completion requests at the start of a JSDoc-preceded property name cause a nil pointer dereference crash in the TypeScript service.*

 * (9 weeks ago) **DanielRosenwasser** added labels `Crash`, `Domain: JS`, and assigned to **Copilot**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2340](https://github.com/microsoft/TypeScript-go/issues/2340) (Closed)

**In mono repo, tsgo not picking types from custom packages**

*Tsgo in a monorepo setup fails to resolve and compile types from custom packages.*

 * created by **Hemantvetal**
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2340#issuecomment-3640601629) **jakebailey** said "This isn't enough information; do you have a repo you can share?"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2340#issuecomment-3640634938) **Hemantvetal** provided minimal reproduction steps for a pnpm-based monorepo TypeScript import error
 * (later) **Hemantvetal** closed the issue

### [Issue microsoft/TypeScript-go#2661](https://github.com/microsoft/TypeScript-go/issues/2661) (Open, `Domain: Editor`, **andrewbranch**)

**auto\-import adds inline type modifier to existing import type statement**

*Auto-import incorrectly adds inline type modifiers to named imports in an import type statement, causing a TS2206 error.*

 * created by **mrvissercb**
 * **mrvissercb** added label `Domain: Editor`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2661#issuecomment-3843462895) **mrvissercb** said "Originally reported here: https://github.com/microsoft/vscode/issues/292038"
 * **andrewbranch** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690) (Closed, `Crash`, **andrewbranch**)

**Panic \- inlayHint \- bad line number \- from autofix/auto\-formatting setup**

*The language server panics during inlayHint requests because an autofix formatting change produces an out-of-range line number.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3860791698) **lukpsaxo** described making a standalone repo and that the error occurred only once under rapid edits, linking the repo and noting larger repos fail more often
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3863002996) **andrewbranch** said "@lukpsaxo that's a 404 for me. Is it a private repo?"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3863780432) **lukpsaxo** said "Sorry, made it public now."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3887686460) **andrewbranch** said "Amazing—I can repro. Thank you!"

### [Issue microsoft/TypeScript-go#2697](https://github.com/microsoft/TypeScript-go/issues/2697) (Closed, `Crash`, `Needs More Info`, **ahejlsberg**)

**Crash compiling TypeScript tests**

*Typescript-Go checker panics with index out-of-range error in TupleNormalizer.normalize during TypeScript test compilation*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2697#issuecomment-3861208874) **ahejlsberg** observed that the repro steps produced a TS18003 error indicating no inputs were found in tsconfig.all.json
 * **ahejlsberg** added label `Needs More Info`
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2697#issuecomment-3861613785) **andrewbranch** said "@ahejlsberg sorry, I meant do that in the microsoft/TypeScript repo 😄 "
 * [today](https://github.com/microsoft/TypeScript-go/issues/2697#issuecomment-3886934556) **ahejlsberg** said "Fixed by #2755."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2698](https://github.com/microsoft/TypeScript-go/issues/2698) (Open, `Type Ordering`)

**Behavior Difference: Error TS2456: Type alias circularly references itself**

*tsgo incorrectly reports circular type alias errors for StaticParamList that compile without errors in TypeScript 6.0*

 * created by **davidjbng**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2698#issuecomment-3886882717) **davidjbng** provided a diff that resolved the error and asked if this change is expected during upgrade to tsgo or will be fixed in TypeScript 7
 * **ahejlsberg** added label `Type Ordering`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2698#issuecomment-3887449579) **ahejlsberg** stated that the error was due to type ordering and would not be changed

### [PR microsoft/TypeScript-go#2723](https://github.com/microsoft/TypeScript-go/pull/2723) (Closed)

**Fix race on snapshot in DidOpenFile**

*The DidOpenFile method lacks snapshotUpdateMu locking during UpdateSnapshot, leading to race conditions and intermittent segmentation faults in tests*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2739](https://github.com/microsoft/TypeScript-go/pull/2739) (Closed)

**Fix recursion proceeding to JSDoc node even if outside of range**

*Prevent recursion from traversing into JSDoc nodes that fall outside the specified range.*

 * created by **apendua**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2739#issuecomment-3887541831) **apendua** thanked the reviewer and updated the list of crashing tests as suggested
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2753](https://github.com/microsoft/TypeScript-go/pull/2753) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript\#63070: Be more lenient about iteration when lib=es5 / noLib**

*Allow for..of iteration under es5/noLib when no global Iterable exists by falling back to array and string iteration.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2753#issuecomment-3886448191) **DanielRosenwasser** said "https://github.com/microsoft/typescript/pull/63070"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2754](https://github.com/microsoft/TypeScript-go/pull/2754) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript \#63026: Fix crash from circularly\-reentrant getEffectsSignature**

*Add flow containers and this-keyword propagation for function-like types in Go binder to prevent infinite getEffectsSignature recursion.*

 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2754#issuecomment-3881579132) **jakebailey** said "Nothing seems to change, confusingly"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2754#issuecomment-3885580443) **jakebailey** said "I think this needs #2748 to make sense, or rather, this may be a noop after."

### [PR microsoft/TypeScript-go#2755](https://github.com/microsoft/TypeScript-go/pull/2755) (Closed)

**Fix multiple issues related to extreme symbol merging**

*Merging thousands of test scripts into one program causes nonsensical symbol overload consolidation, assertion panics, and out-of-bounds errors.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2755#issuecomment-3885713555) **ahejlsberg** said "Copilot likes clamping. 😄 "
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2758](https://github.com/microsoft/TypeScript-go/pull/2758) (Closed, **jakebailey**, **Copilot**)

**Port \#62311: Fix parenthesizer rules for binary expressions mixing ?? with \|\|/&&**

*Port PR #62311 to ensure binary expressions mixing ?? with ||/&& are parenthesized by adding helper and updating emit logic.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2758#issuecomment-3885551073) **jakebailey** said "http://github.com/microsoft/TypeScript/pull/62311"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2760](https://github.com/microsoft/TypeScript-go/pull/2760) (Open, **jakebailey**, **Copilot**)

**Error on modules\-as\-namespaces**

*Emit parse errors for 'module' namespace declarations, remove obsolete utilities and tests, and update baselines to match TypeScript.*

 * **Copilot** assigned to **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3882779331) **jakebailey** said "@copilot the intent is that module is illegal and produces a parse error"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3882864264) **Copilot** updated the parser to emit TS1540 parse errors on each identifier for illegal module namespace declarations and aligned baselines by deleting diff files
 * [today](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3885570532) **jakebailey** said "I guess this is fine, though I think I was hoping to hard remove it and not even have this diagnostic, as though module foo { were entirely illegal."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3885934528) **DanielRosenwasser** recommended gracefully parsing and issuing a parse error

### [PR microsoft/TypeScript-go#2761](https://github.com/microsoft/TypeScript-go/pull/2761) (Closed)

**Bump to Go 1\.26**

*Upgrading to Go 1.26 reduces tsgo compilation time by 30% and removes ptrTo in favor of new.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2761#issuecomment-3885917316) **jakebailey** said "This came out quite literally yesterday; I'm not sure when the right time to do this is given it's not in the Arch Linux repos, longsleep PPA, homebrew."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2761#issuecomment-3885952235) **gabritto** asked what consequences delaying the update might have and suggested waiting a bit though preferring faster builds
 * [today](https://github.com/microsoft/TypeScript-go/pull/2761#issuecomment-3885961232) **jakebailey** clarified that with GOTOOLCHAIN newer Go releases auto-download, the Microsoft Go build works, and noted that delve may not support Go 1.26 though he uses a gotip-built version
 * [today](https://github.com/microsoft/TypeScript-go/pull/2761#issuecomment-3886114250) **jakebailey** said "Also, on my laptop, go clean -cache -testcache; hereby test takes 4m20s, but on this branch, it only takes 2m6s."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2761#issuecomment-3886301588) **jakebailey** attached a screenshot of their desktop
 * [today](https://github.com/microsoft/TypeScript-go/pull/2761#issuecomment-3886473563) **jakebailey** said "A downside is that tinygo doesn't have Go 1.26 yet, and I like to test things with it, but it's also broken for other reasons anyway. So probably not a blocker."

### [Issue microsoft/TypeScript-go#2762](https://github.com/microsoft/TypeScript-go/issues/2762) (Open)

**Reconsider tsconfig membership lookups for \`\.d\.ts\` files**

*Due to rootDir changes, TypeScript 6.0/7.0 fail to include .d.ts files specified in tsconfig’s files, include, or types*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2763](https://github.com/microsoft/TypeScript-go/pull/2763) (Closed)

**Add check for \`nil\` symbol in \`getJSDocOrTag\`**

*Add a nil symbol check in getJSDocOrTag to avoid null errors in JSDoc retrieval.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2763#issuecomment-3886914886) **ahejlsberg** said "Don't think we need a test here, it was just a missing nil check that wasn't ported from the corresponding Strada code."

### [PR microsoft/TypeScript-go#2764](https://github.com/microsoft/TypeScript-go/pull/2764) (Closed)

**Fix invalid params error handling**

*Fix unmarshal failures by sending correctly identified invalid params errors rather than generic invalid request codes.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#2765](https://github.com/microsoft/TypeScript-go/pull/2765) (Closed)

**Acquire snapshots synchronously while blocking other requests/notifications**

*Modify the server dispatch loop to synchronously acquire document snapshots before executing request handlers, preventing concurrent change notifications from causing inconsistencies.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#2766](https://github.com/microsoft/TypeScript-go/pull/2766) (Closed)

**Resolve/merge configuration on the client**

*Add LSP client middleware to merge VS Code js/ts, TypeScript, and JavaScript settings into a single resolved configuration object.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2767](https://github.com/microsoft/TypeScript-go/issues/2767) (Open, **jakebailey**, **Copilot**)

**Spreading variable of \`RegExpIndicesArray\` type will cause error**

*Spreading a RegExpIndicesArray in tsgo triggers a spurious iterator error that does not occur in TypeScript 6.0.*

 * created by **hkleungai**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2768](https://github.com/microsoft/TypeScript-go/pull/2768) (Open, **jakebailey**, **Copilot**)

**Fix union type error reporting in getIterationTypesOfIterable**

*Modify getIterationTypesOfIterable to fail entire non-iterable union types instead of reporting errors on individual constituents.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2769](https://github.com/microsoft/TypeScript-go/issues/2769) (Open)

**reference path 不能跳转**

*Ctrl-click navigation on reference paths in .d.ts files fails to jump to the referenced file.*

 * created by **myNinety**

### [Issue microsoft/TypeScript-go#2770](https://github.com/microsoft/TypeScript-go/issues/2770) (Closed, `Crash`)

**Unable to run win32\-arm64 releases \(not a valid Win32 application\)**

*The ARM64 Windows build of the ts-go-fork server in PhpStorm fails to start with CreateProcess error 193 invalid Win32 application.*

 * created by **tobias-barth**
 * **tobias-barth** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2770#issuecomment-3891470913) **tobias-barth** said "Whoops, posted to wrong repo. My bad!"
 * (later) **tobias-barth** closed the issue

### [Issue microsoft/TypeScript-go#2771](https://github.com/microsoft/TypeScript-go/issues/2771) (Closed, **jakebailey**, **Copilot**)

**VSCode: code folding ranges**

*The TypeScript Native Preview extension in VSCode provides worse code folding ranges than the stable TypeScript@6.0 release.*

 * created by **lukeed**

