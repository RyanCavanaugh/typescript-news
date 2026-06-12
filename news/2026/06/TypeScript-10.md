# Report for 2026-06-10 (Wednesday, June 10th, 2026)

5 different users commented on 29 different issues.

## Recommended Actions

 * Response Recommended
    * @mwg-ofx asked if the change could be reconsidered after the Go migration due to speed boost in [microsoft/TypeScript#45560](https://github.com/microsoft/TypeScript/issues/45560#issuecomment-4676880644)
    * @muhammad-paksi asked if the issue would be resolved and provided a workaround in [microsoft/TypeScript#54087](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-4676219466)
    * @ibesuperv asked to review the submitted fix in [microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4679263794)

## Activity Summary

### [Issue microsoft/TypeScript#45560](https://github.com/microsoft/TypeScript/issues/45560) (Open, `Bug`, `Domain: Mapped Types`, `Fix Available`)

**Mapped types lose type information**

*Mapped types over tuple unions lose specific element types and widen indexed access to boolean instead of true.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/45560#issuecomment-1260129973) **RyanCavanaugh** noted that the straightforward fix caused unacceptable performance hits in material-ui and suggested seeking a more performant solution since the bug is infrequent
 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * [today](https://github.com/microsoft/TypeScript/issues/45560#issuecomment-4676880644) **mwg-ofx** said "I wonder if such a change could be reconsidered after the Go migration is complete, given the significant speed boost it provides."
 * [later](https://github.com/microsoft/TypeScript/issues/45560#issuecomment-4682464840) **RyanCavanaugh** said "By "unacceptable perf hits" we mean like 40%, and people are already complaining that tsgo isn't fast enough in material-ui."

### [Issue microsoft/TypeScript#54087](https://github.com/microsoft/TypeScript/issues/54087) (Open, `Needs Investigation`, **sheetalkamat**)

**TypeScript file watcher holds onto folders and causes EPERM**

*TypeScript file watcher in VSCode intermittently locks folders on Windows, causing EPERM errors when renaming files until restart.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-2058586403) **hbatalhaStch** pointed out that project-wide analysis can be enabled using the typescript.tsserver.experimental.enableProjectDiagnostics option
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-2812087903) **ahr-cw-de** said "Are there any updates as this is a really annoying problem?!"
 * [35 weeks ago](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-3377200662) **Gwynerva** listed four workarounds for the Windows issue, noting that some disable IntelliSense or autoimports and suggesting renaming folders externally or using Linux
 * [today](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-4676219466) **muhammad-paksi** asked whether the issue would be resolved and provided a workaround snippet

### [Issue microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092) (Open, `Bug`, `Help Wanted`, `Domain: check: Control Flow`)

**Crash: RangeError: Maximum call stack size exceeded in isReachableFlowNodeWorker with complex for loop headers**

*TypeScript's compiler crashes with a maximum call stack size exceeded error when analyzing reachability in complex for loop headers.*

 * **RyanCavanaugh** added label `Domain: check: Control Flow`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4655578718) **ibesuperv** said "Yo if this issue still exists can you please assign me"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4663552465) **RyanCavanaugh** referred to the contributing guidelines and reminded the user to develop in the typescript-go repo because the bug didn't meet the 6.0 patch bar
 * [later](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4679263794) **ibesuperv** submitted a fix in the typescript-go repository and asked for review

### [Issue microsoft/TypeScript#63547](https://github.com/microsoft/TypeScript/issues/63547) (Open, `Won't Fix`)

**packageId is not set when calling resolveModuleName on a directory with an index\.d\.ts file in a dependency**

*TypeScript resolveModuleName fails to set packageId when importing a directory’s index.d.ts without explicit index path*

 * created by **TheLazySquid**

