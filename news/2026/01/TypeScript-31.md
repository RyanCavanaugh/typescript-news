# Report for 2026-01-31 (Saturday, January 31st, 2026)

4 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @bahrus suggested amending the proposal to specify recognizing importmap JSON file patterns in [microsoft/TypeScript#43326](https://github.com/microsoft/TypeScript/issues/43326#issuecomment-3828844701)

## Activity Summary

### [Issue microsoft/TypeScript#3841](https://github.com/microsoft/TypeScript/issues/3841) (Open, `Suggestion`, `In Discussion`)

**T\.constructor should be of type T**

*Suggest typing instance.constructor as the class type rather than Function to enable direct static property access without casting.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3612212409) **snarbles2** clarified that `this` and `typeof this` yield the same instance type and that `typeof this` does not refer to the constructor
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3612606091) **FrameMuse** apologized for confusion and clarified that typeof this does not refer to the constructor inside the class body but does in static methods
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3613012288) **ExE-Boss** corrected the type of C.constructor by explaining it’s globalThis.Function and provided a correct TypeScript definition
 * [later](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3831017529) **OldStarchy** explained that constructor signatures and call signatures cannot be inherited, suggested using static factory methods as a workaround, and demonstrated typing constructors by picking static members via Pick

### [Issue microsoft/TypeScript#43326](https://github.com/microsoft/TypeScript/issues/43326) (Open, `Suggestion`, `Needs Proposal`, **weswigham**)

**Support import maps and bare import specifiers**

*Enable import maps and bare import specifiers in TypeScript to map package names to file paths via HTML import maps*

 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/43326#issuecomment-1324167022) **matthew-dean** asked if TypeScript could pick up Node.js import key resolution
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/43326#issuecomment-1674747582) **CMCDragonkai** said "It seems that at the moment one has to still specify paths mapping in tsconfig.json to get tsc to understand the #internal paths that now exists in package.json for NodeJS packages."
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/43326#issuecomment-3698641039) **HolgerJeromin** critiqued making importmap support part of TypeScript due to diverse data sources and questioned its practicality
 * [today](https://github.com/microsoft/TypeScript/issues/43326#issuecomment-3828844701) **bahrus** suggested amending the proposal to specify recognizing importmap JSON file patterns (*.importmap.json) and described integration methods

### [Issue microsoft/TypeScript#62210](https://github.com/microsoft/TypeScript/issues/62210) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **weswigham**)

**Deprecate, remove support for import assertions**

*TypeScript will deprecate import assertions in 6.0 and remove them in 7.0 in favor of the 'import ... with' syntax.*

 * (25 weeks ago) **DanielRosenwasser** added label `Committed`, set milestone to `TypeScript 6.0`, and assigned to **weswigham**
 * (today) **typescript-bot** added labels `Fix Available`, `Fix Available`, `Fix Available`

### [PR microsoft/TypeScript#63046](https://github.com/microsoft/TypeScript/pull/63046) (Open, `For Backlog Bug`)

**Introduce ES2025 target & Add missing ScriptTargetFeatures**

*Introduce ES2025 compilation target and add missing type definitions for RegExp.escape and Intl.DurationFormat in TypeScript.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3813940828) **jakebailey** said "We have a lot of these lib related PRs; it's absolutely our intention to review all of them as soon as we can, we've just had a bunch of other stuff that has been a bit more pressing."
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3813947467) **jakebailey** noted that mixing esnext and ES2025 changes in a single PR made it hard to distinguish new work from moves and suggested reviewing individual ESNext PRs and creating a dedicated ES2025 PR
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3814011569) **petamoriken** explained that only two files were added and offered to split the PR if preferred
 * [later](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3830973432) **petamoriken** said "@jakebailey For now, I can remove the additions of es2025.intl.d.ts and es2025.regexp.d.ts from this PR, but should I do so? Please let me know your thoughts."

### [PR microsoft/TypeScript#63077](https://github.com/microsoft/TypeScript/pull/63077) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **weswigham**, **jakebailey**)

**Deprecate import assert in favor of import with**

*Deprecate 'import assert' syntax in favor of 'import with' and update tests to cover both deprecated and non-deprecated usage.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `Author: Team`, `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, and assigned to **jakebailey**, **weswigham**
 * **jakebailey** added label `Breaking Change`

