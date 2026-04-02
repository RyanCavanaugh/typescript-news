# Report for 2026-01-29 (Thursday, January 29th, 2026)

15 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @TkDodo provided a minimal reproduction and TS Playground link in [microsoft/TypeScript-go#2609](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3819956812)
    * @rubenferreira97 asked whether TypeScript 6 deprecation behavior within the same file was intended in [microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3822550361)

## Activity Summary

### [PR microsoft/TypeScript-go#2331](https://github.com/microsoft/TypeScript-go/pull/2331) (Open)

**Organize Imports**

*Implement functionality to automatically organize and sort imports within source files.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3813168824) **johnfav03** recommitted the change to CodeActionProvider and tested it locally in the editor using the VSCode codebase
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3814667929) **jakebailey** tested import organizing and found the shebang repeated before each import
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3814678385) **jakebailey** reported import reorganization and indentation loss in two TypeScript files
 * [today](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3820320228) **iisaduan** identified missing indenting logic that could affect organize imports and cause a loss of smaller indent

### [PR microsoft/TypeScript-go#2604](https://github.com/microsoft/TypeScript-go/pull/2604) (Closed)

**Some of the changes to improve \-\-build memory footprint**

*Improved build memory footprint by fixing writerPool retention, restricting source file caching to d.ts/json, and adjusting builder concurrency flag.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3816025185) **Zzzen** said "Would you mind pushing a beta build? I’d love to give it a spin."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3816055377) **jakebailey** said "We don't have a way to do that; you'd have to build from source"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3816395284) **Zzzen** reported continuing to encounter OOM errors and noticed that tsgo consumed significantly more memory compared to tsc
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3819622471) **sheetalkamat** said "@Zzzen  is it possible to share repro. What does extendedDiagnostics show.. "
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3819767115) **sheetalkamat** apologized for mistakes and asked to retry after restructuring code and to provide repro steps, pprof dump, and extendedDiagnostics if issue persisted
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3821615246) **Zzzen** explained that tsgo fully expanded DeepReadonly<LargeType> in the generated .d.ts, causing excessively large declaration files
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3821657311) **jakebailey** said "Can you try building #2459 and see if that fixes your issue?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3822178978) **Zzzen** confirmed that the emitted types and .d.ts files matched tsc output and requested a merge soon

### [PR microsoft/TypeScript-go#2605](https://github.com/microsoft/TypeScript-go/pull/2605) (Closed)

**Diff \`findAllReferences\`**

*Compute baseline diffs for findAllReferences results to streamline pull request reviews.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2606](https://github.com/microsoft/TypeScript-go/issues/2606) (Closed, **gabritto**)

**Module specifier completion icons are lazily loaded/generic until item selection**

*Module import suggestions in IntelliSense initially display generic icons and only update to actual file-type icons after selection.*

 * created by **rubenferreira97**
 * **jakebailey** assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2607](https://github.com/microsoft/TypeScript-go/issues/2607) (Closed, `Crash`, **andrewbranch**)

**no project found for URI \`file:///home/jabaile/work/DefinitelyTyped\-tools/node\_modules/\.pnpm/tar%407\.5\.7/node\_modules/tar/dist/commonjs/options\.d\.ts\`**

*Incorrect `* as tar` import in io.ts causes language server to report 'no project found for URI' for tar options.d.ts.*

 * created by **jakebailey**
 * (today) **jakebailey** added label `Crash`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2607#issuecomment-3819171640) **andrewbranch** said "Ugh, I fixed this exact scenario already, I wonder if it broke again or if the symlink or something is making this one act differently?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2607#issuecomment-3819191216) **jakebailey** said "This is very reproducible for me, though it's on a branch I haven't pushed up yet (will do shortly)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2607#issuecomment-3819223893) **jakebailey** said "Okay, I saw this at: https://github.com/jakebailey/DefinitelyTyped-tools/commit/6426bd346fb05dae4fdea446968d5ff6dda99014"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2607#issuecomment-3819283072) **andrewbranch** said "I can repro it, fix incoming"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2608](https://github.com/microsoft/TypeScript-go/pull/2608) (Closed)

**Ensure inferred project has up to date program when it might contain the requested file**

*Ensure inferred projects refresh their program when they might contain the requested file.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2609](https://github.com/microsoft/TypeScript-go/issues/2609) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Type instantiation is excessively deep and possibly infinite\.**

*tsgo throws a deep, possibly infinite type instantiation error for TanStack Form with zod that TypeScript 5.9 compiles without issue.*

 * created by **TkDodo**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3819510125) **jakebailey** said "This is a pretty large repro; do you have something that doesn't pull in a the library?"
 * **jakebailey** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3819956812) **TkDodo** removed zod and unnecessary type parameters to create a ~200-line reproduction, noted the TS2589 error still occurred in tsgo but not in tsc, and shared a TypeScript Playground link

### [PR microsoft/TypeScript-go#2610](https://github.com/microsoft/TypeScript-go/pull/2610) (Closed)

**Send path completion item detail eagerly**

*Ensure path completion items include their file extension details eagerly to display correct icons and avoid inconsistent extension determination.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2610#issuecomment-3820922520) **jakebailey** said "Popped out of the merge queue because of declarationMapsRenameWithProjectReferencesEdit, which I think is flaky?"
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2611](https://github.com/microsoft/TypeScript-go/issues/2611) (Closed)

**typeRoots behavior difference from tsc v9 \(vitest/globals\)**

*tsgo fails to recognize vitest/globals types configured via typeRoots, resulting in 'vi' name not found errors while tsc succeeds.*

 * created by **sammarks-stukent**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2611#issuecomment-3819738992) **sammarks-stukent** said "Might be related to https://github.com/microsoft/typescript-go/issues/2147"

### [Issue microsoft/TypeScript-go#2612](https://github.com/microsoft/TypeScript-go/issues/2612) (Open, `Crash`)

**tsgo crashes**

*tsgo crashes with a stack trace when running deno check on ignore_test.ts with DENO_UNSTABLE_TSGO enabled in Deno 2.6.6.*

 * created by **sigmaSd**
 * **sigmaSd** added label `Crash`

### [PR microsoft/TypeScript-go#2613](https://github.com/microsoft/TypeScript-go/pull/2613) (Closed)

**Implement telemetry reporting in extension**

*Introduce telemetry reporting in the extension and language server using @vscode/extension-telemetry to capture usage and errors.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2614](https://github.com/microsoft/TypeScript-go/pull/2614) (Closed)

**fix: use typeRoot instead of candidate when resolving types references from config**

*Modify resolveTypeReferenceDirective to use typeRoots rather than candidate paths when resolving type references from tsconfig, fixing resolution errors.*

 * created by **sammarks-stukent**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2614#issuecomment-3820300047) **sammarks-stukent** said "@microsoft-github-policy-service agree company="Stukent""
 * [later](https://github.com/microsoft/TypeScript-go/pull/2614#issuecomment-3824348781) **sammarks-stukent** said "@andrewbranch for sure! Extra tests have been removed 👍 "

### [Issue microsoft/TypeScript-go#2615](https://github.com/microsoft/TypeScript-go/issues/2615) (Closed)

**Stack overflow in handleDtsMayChangeOfFileAndExportsOfFile with incremental build cache**

*Reusing a stale incremental build cache causes tsgo to crash with a goroutine stack overflow in handleDtsMayChangeOfFileAndExportsOfFile.*

 * created by **blowery**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2615#issuecomment-3820881517) **jakebailey** pointed out that the user’s version was outdated and asked them to upgrade to include fix from #2532
 * [today](https://github.com/microsoft/TypeScript-go/issues/2615#issuecomment-3820895526) **blowery** confirmed the fix by testing version 7.0.0-dev.20260128.1 and verifying that tsgo --build ran without stack overflow on an old image with a stale incremental TypeScript cache
 * (today) **blowery** closed the issue

### [PR microsoft/TypeScript-go#2616](https://github.com/microsoft/TypeScript-go/pull/2616) (Closed)

**fix autoimports crash in js files **

*Fix autoimports crash in JavaScript files, correct miscapitalization parsing bug, and add a parsing test.*

 * created by **iisaduan**

### [PR microsoft/TypeScript-go#2617](https://github.com/microsoft/TypeScript-go/pull/2617) (Closed)

**ExplainFiles to handle duplicated files **

*Enhance ExplainFiles to detect and properly handle duplicated files to avoid conflicts or redundancy.*

 * created by **sheetalkamat**

### [Issue microsoft/TypeScript-go#2618](https://github.com/microsoft/TypeScript-go/issues/2618) (Closed, `Domain: Editor`)

**lsp panic: textDocument/completion returned ErrNeedsAutoImports even after enabling auto imports**

*TypeScript-Go LSP extension panics on textDocument/codeAction requests returning ErrNeedsAutoImports despite auto imports being enabled.*

 * created by **walkerdb**
 * **walkerdb** added label `Domain: Editor`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2619](https://github.com/microsoft/TypeScript-go/issues/2619) (Closed)

**Incorrect member resolution in merged namespaces \(parity mismatch with tsc 5\.9 & 6\.0\+\)**

*tsgo incorrectly emits unqualified identifiers for members of merged namespaces, causing runtime errors while tsc correctly qualifies them.*

 * created by **rubenferreira97**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2619#issuecomment-3821406986) **jakebailey** said "This is the same as #961."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961) (Open, `bug`, `Domain: Emit`, `Domain: Type Checking`, **jakebailey**)

**tsgo fails to resolve namespace symbols in non\-extends contexts across files**

*tsgo fails to qualify namespace symbols A and Afunc outside extends contexts across files, causing incorrect JS and runtime errors.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808175525) **jakebailey** explained typical uses of namespaces and asked for clarification on re-annotating namespace decorations
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808188925) **dtscd** described moving code between files under the same namespace and the extra annotation needed if namespaces no longer merged across files
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3817986645) **magic-akari** described expected compiler error output
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3821410388) **jakebailey** mentioned that they would reconsider the approach because they already depend on the checker for emit and tsgo is in a mixed state
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3821628137) **magic-akari** mentioned they would reconsider the enum merging decision due to checker dependency and recommended driving design by parallel emit goals rather than implementation constraints
 * [later](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3822550361) **rubenferreira97** asked whether TypeScript 6's deprecation behavior within the same file was intended and suggested finding a middle ground for namespace merging restrictions
 * [later](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3822759112) **magic-akari** highlighted that more complex cross-namespace scenarios require careful support definition and provided an example that works in TypeScript 5
 * [later](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3824394383) **dtscd** provided a code example demonstrating that a simple patch resolves nested namespace access within the same file

