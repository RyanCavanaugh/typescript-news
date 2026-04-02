# Report for 2026-02-05 (Thursday, February 5th, 2026)

11 different users commented on 18 different issues.

## Recommended Actions

 * Response Recommended
    * @TkDodo asked if there was anything we can improve in the TanStack form typings in [microsoft/TypeScript-go#2609](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3855592321)
    * @lukeapage offered to create a dedicated repository in [microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3855215392)
    * @lukeapage reported noticing repeated writes over two weeks that might be due to specific setup and multiple ESLint rules in [microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3855231208)
    * @lukeapage reported that they will reproduce the issue using a file with many imports and noted it could be Windows-specific in [microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3855276597)
    * @gggdomi provided logs and environment details in [microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3859284870)
    * @lukpsaxo provided reproduction details and offered to create a standalone repro in [microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3860622182)
    * @lukpsaxo provided a standalone repository for reproducing the issue in [microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3860791698)

## Activity Summary

### [Issue microsoft/TypeScript-go#1531](https://github.com/microsoft/TypeScript-go/issues/1531) (Closed, `Crash`, `Domain: Program`, **sheetalkamat**, **gabritto**)

**tsgo panics with invalid UTF\-8 when marshalling build info**

*tsgo panics during build info marshalling because it encounters invalid UTF-8 in diagnostic messages.*

 * **RyanCavanaugh** assigned to **sheetalkamat**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1531#issuecomment-3746812464) **gabritto** said "Related: #2336"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1531#issuecomment-3815132905) **scarf005** asked what to do to fix a panic error in tsgo typecheck and reported that removing .tsbuildinfo did not help
 * **gabritto** assigned to **gabritto**

### [Issue microsoft/TypeScript-go#2208](https://github.com/microsoft/TypeScript-go/issues/2208) (Closed, `Crash`, **sheetalkamat**)

**crash on initial load of a large react\-native/expo project**

*The tsgo language server panics with a nil pointer dereference on initial load of a large React Native/Expo project.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2208#issuecomment-3609801339) **jakebailey** provided a better-formatted panic stack trace
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2208#issuecomment-3609805062) **jakebailey** noted that in the provided code snippet p.typingsWatch must be nil
 * **RyanCavanaugh** assigned to **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2208#issuecomment-3857049385) **sheetalkamat** said "Fixed by https://github.com/microsoft/typescript-go/pull/2252"
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2336](https://github.com/microsoft/TypeScript-go/issues/2336) (Closed, `Crash`, **jakebailey**, **gabritto**, **Copilot**)

**Crash for signature help in arrow function parameters**

*Signature help invoked on arrow function parameters crashes the TypeScript server without a stack trace*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3720201285) **jakebailey** said "We should probably make it so that the node builder detects internal types and auto-escapes them like the old compiler?"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3720210437) **gabritto** asked where the old compiler escaped internal types and noted that Strada returned "__type(...)" as label
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3720242722) **jakebailey** clarified that symbol names with __ prefixes sometimes leaked, which was unacceptable in Go code due to the UTF-8 trick, and that they had not found a better alternative
 * **gabritto** assigned to **gabritto**

### [PR microsoft/TypeScript-go#2577](https://github.com/microsoft/TypeScript-go/pull/2577) (Open)

**Add \-\-release flag to emulate real released binaries, rename build tag to noassert, test release in CI**

*Add a --release flag to produce stripped binaries, rename the build tag to ‘noassert’, and test release builds in CI.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3793259156) **rubiesonthesky** said "nodebug seems logical flag, but without context, it’s easy to read it as “node bug” 🐛 probably no harm, just funny coincidence. "
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3793261911) **jakebailey** said they thought the name was funny, couldn't think of a better name, suggested leaving it as release and questioned flipping code in release mode
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3800621851) **jakebailey** said "Thinking more, we should have a --nodebug like --noembed, except that aliases another flag too. So, it's probably a bad build tag name and release was fine. Maybe..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3855769882) **jakebailey** said "Also TODO, going to add a task which actually exercises the release procedure, for CI testing."

### [Issue microsoft/TypeScript-go#2609](https://github.com/microsoft/TypeScript-go/issues/2609) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Type instantiation is excessively deep and possibly infinite\.**

*tsgo throws a deep, possibly infinite type instantiation error for TanStack Form with zod that TypeScript 5.9 compiles without issue.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3838297571) **ahejlsberg** identified the issue as a type ordering problem and observed that compiling with TS 6.0 in type ordering compatibility mode produced the same deep type instantiation error, concluding there was probably not much to be done
 * (3 days ago) **ahejlsberg** added labels `Type Ordering`, `Domain: Type Checking`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3855592321) **TkDodo** inquired if anything could be improved in the TanStack form typings

### [Issue microsoft/TypeScript-go#2681](https://github.com/microsoft/TypeScript-go/issues/2681) (Closed, `help wanted`, `Crash`)

**textDocument/completion: runtime error: invalid memory address or nil pointer dereference**

*The TypeScript Go LSP server panics with a nil pointer dereference during textDocument/completion requests.*

 * (yesterday) **DanielRosenwasser** added label `help wanted`, and unassigned **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2681#issuecomment-3849539979) **DanielRosenwasser** provided minimal repros and explained that reserved keywords disrupt parsing, causing a stray colon token, and noted the code change to direct Parent.Parent access
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2687](https://github.com/microsoft/TypeScript-go/pull/2687) (Closed)

**fix\(2681\): prevent nil parent context in import\-attributes**

*Add validation to import-attributes to prevent a nil parent context from causing errors.*

 * created by **a-tarasyuk**
 * (today) **DanielRosenwasser** closed the issue
 * (today) **DanielRosenwasser** reopened the issue
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2689](https://github.com/microsoft/TypeScript-go/pull/2689) (Closed)

**Start targeting TS 6\.0 behavior**

*Bump TypeScript submodule to main, port key compiler settings, and adjust or skip tests for TypeScript 6.0 compliance.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690) (Open, `Crash`, **andrewbranch**)

**Panic \- inlayHint \- bad line number \- from autofix/auto\-formatting setup**

*The language server panics during inlayHint requests because an autofix formatting change produces an out-of-range line number.*

 * created by **lukpsaxo**
 * **lukpsaxo** added label `Crash`
 * **DanielRosenwasser** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3854837016) **andrewbranch** asked what they were doing wrong with their VSCode and ESLint configuration
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3855215392) **lukeapage** said "I’m not sure -  I can only guess timing issues. I can have a go at making a dedicated repo."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3855231208) **lukeapage** reported noticing repeated writes over the last two weeks possibly due to specific setup and many ESLint rules
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3855276597) **lukeapage** mentioned they would reproduce the issue using the prefer-export-from rule on a file with over 10 imports and noted it might be Windows-specific
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3855360352) **andrewbranch** noted that watch events were ignored for open files, offered to test the rule on Windows, and asked to be informed if a repro was achieved
 * [later](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3859284870) **gggdomi** concurred that they started seeing the same error today on macOS while using eslint and prettier
 * [later](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3860622182) **lukpsaxo** reproduced the issue consistently on longer files but not on smaller ones and said they would create a standalone repro
 * [later](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3860791698) **lukpsaxo** described making a standalone repo and that the error occurred only once under rapid edits, linking the repo and noting larger repos fail more often

### [PR microsoft/TypeScript-go#2694](https://github.com/microsoft/TypeScript-go/pull/2694) (Open, **jakebailey**, **Copilot**)

**Fix panic when moduleSuffixes resolves to declaration files**

*Fix panic by extracting file extensions from the original candidate path when moduleSuffixes includes declaration file suffixes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2694#issuecomment-3854845143) **jakebailey** said "@copilot You didn't make a test and show that it failed. This may well be the right change, but without a test we can't verify the solution."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2694#issuecomment-3854907655) **Copilot** added a failing test case in commit 88ad6db5 reproducing the panic and explained the corresponding fix in commit 5c685c94

### [PR microsoft/TypeScript-go#2695](https://github.com/microsoft/TypeScript-go/pull/2695) (Closed)

**Fix missing typedarrays lib**

*Port the missing typedarrays library definitions to restore ESNext support.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2696](https://github.com/microsoft/TypeScript-go/issues/2696) (Open, `Crash`)

**Crash on error reporting for TS test parseUnmatchedTypeAssertion\.ts**

*A slice bounds out of range panic occurs during error reporting for the parseUnmatchedTypeAssertion.ts TypeScript test.*

 * created by **andrewbranch**
 * **andrewbranch** added label `Crash`

### [Issue microsoft/TypeScript-go#2697](https://github.com/microsoft/TypeScript-go/issues/2697) (Open, `Crash`, `Needs More Info`, **ahejlsberg**)

**Crash compiling TypeScript tests**

*Typescript-Go checker panics with index out-of-range error in TupleNormalizer.normalize during TypeScript test compilation*

 * created by **andrewbranch**
 * **andrewbranch** added label `Crash`
 * **ahejlsberg** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#2698](https://github.com/microsoft/TypeScript-go/issues/2698) (Open)

**Behavior Difference: Error TS2456: Type alias circularly references itself**

*tsgo reports StaticParamList as a non-generic circular type alias error, whereas TypeScript 6.0 compiles it without errors.*

 * created by **davidjbng**

### [Issue microsoft/TypeScript-go#2699](https://github.com/microsoft/TypeScript-go/issues/2699) (Open)

**tsgo resolves inherited include/exclude globs differently than tsc when using extends**

*tsgo resolves inherited include globs relative to the child config rather than the parent, causing a different output structure than tsc.*

 * created by **mabels**

### [Issue microsoft/TypeScript-go#2700](https://github.com/microsoft/TypeScript-go/issues/2700) (Closed)

**\`"module": "nodenext"\` no longer infers \`"target": "esnext"\` in v7\.0\.0\-dev\.20260206\.1**

*In v7.0.0-dev.20260206.1, specifying module: nodenext no longer implicitly targets ESNext, causing Set.difference to be unrecognized.*

 * created by **abrahamguo**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2700#issuecomment-3861177485) **jakebailey** explained that the target no longer depended on module to avoid a cycle and that ES2025 will become the default in a later update to include those types again

