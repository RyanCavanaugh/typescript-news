# Report for 2026-01-18 (Sunday, January 18th, 2026)

8 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @OliverJAsh provided bisect result and reproduction steps in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3765712414)
    * @OliverJAsh provided the first bad commit hash in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3767082349)
    * @MartinCura provided repro steps and heap profile as requested in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3768557703)

## Activity Summary

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Closed, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3758010438) **talldan** attached heap and alloc profiles from before and after restarting the language server
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3761933622) **OliverJAsh** reported facing the same issue and attached a screenshot
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3764459330) **chesterbait88** reported that TSGO consumed 60 GB, crashed the system, and asked if maintainers were investigating
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3765712414) **OliverJAsh** identified that the issue began with extension version 0.20260111.1 and reproduced it by opening multiple files and switching between commits
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3765814777) **jakebailey** said "If so, can you bisect the repo itself and use the typescript.native-preview.tsdk option to point it at built/local?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3767082349) **OliverJAsh** said "The first bad commit is 38353bd4d704efd6d00ec277087bbca5a7d050ff."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3767242958) **dream2333** said "same"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3768557703) **MartinCura** described experiencing increasing memory usage in tsgo on each save, tested it, attached a heap profile and screenshot, and suggested periodic restarts

### [PR microsoft/TypeScript-go#2421](https://github.com/microsoft/TypeScript-go/pull/2421) (Closed, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.31\.8 to 4\.31\.9 in the github\-actions group across 1 directory**

*Bump github/codeql-action from 4.31.8 to 4.31.9 in the GitHub Actions configuration.*

 * (3 weeks ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * [later](https://github.com/microsoft/TypeScript-go/pull/2421#issuecomment-3768011091) **dependabot[bot]** said "Looks like github/codeql-action is updatable in another way, so this is no longer needed."
 * (later) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#2522](https://github.com/microsoft/TypeScript-go/issues/2522) (Open, `Domain: Declaration Emit`, `Crash`, **weswigham**)

**Reexporting @types/micromatch@4\.0\.10 from a \.cjs file crashes**

*Re-exporting @types/micromatch@4.0.10 from a .cjs file crashes the TypeScript declaration transformer with a ‘Diagnostic emitted without context’ panic.*

 * created by **Knagis**
 * **Knagis** added label `Crash`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2522#issuecomment-3759406281) **Knagis** mentioned that version 7.0.0-dev.20251027.1 compiled without crashes but version 7.0.0-dev.20251029.1 crashed
 * (today) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2540](https://github.com/microsoft/TypeScript-go/issues/2540) (Open)

**Should handle \`FORCE\_COLOR\` environment variable**

*Support the FORCE_COLOR environment variable to override TTY detection and enable colored output for exec calls*

 * created by **so1ve**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3765354673) **jakebailey** questioned why this was needed now given the old codebase didn't do it
 * [today](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3765403442) **so1ve** described the difference between vue-tsc and vue-tsgo and requested colored and formatted tsgo help text appended to the CLI's help text like tsx
 * [today](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3765440078) **jakebailey** noted that picocolors, chalk, and Node support this, but TypeScript has never supported it, so it was surprising to require it now

### [PR microsoft/TypeScript-go#2541](https://github.com/microsoft/TypeScript-go/pull/2541) (Open)

**Update CHANGES\.md to reflect \#2513**

*Update CHANGES.md to reflect changes introduced by pull request #2513*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#2542](https://github.com/microsoft/TypeScript-go/pull/2542) (Closed)

**Fix stack overflow caused by circular destructuring**

*Resolve a stack overflow crash in strict mode caused by circular destructuring of a typed object*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2542#issuecomment-3766046757) **DanielRosenwasser** said "What was the stack trace? Even the other PR doesn't link back to anything."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2542#issuecomment-3766073619) **DanielRosenwasser** said "Okay, this is the original issue: https://github.com/microsoft/TypeScript/issues/62993"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2542#issuecomment-3766086193) **DanielRosenwasser** reported a recurring TypeScript stack trace during object literal checking
 * [today](https://github.com/microsoft/TypeScript-go/pull/2542#issuecomment-3766289662) **ahejlsberg** recommended back-porting the fix to 6.0
 * (today) **ahejlsberg** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/2542#issuecomment-3767108948) **Andarist** mentioned having an open PR in Strada, using a different approach, and reported that an experiment confirmed they could remove NodeCheckFlags.InCheckIdentifier

### [PR microsoft/TypeScript-go#2543](https://github.com/microsoft/TypeScript-go/pull/2543) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Update GitHub Actions in the root directory by bumping actions/setup-node to v6.2.0 and upgrading github/codeql-action.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

