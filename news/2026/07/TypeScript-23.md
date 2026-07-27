# Report for 2026-07-23 (Thursday, July 23rd, 2026)

5 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @matthieusieben suggested reconsidering the issue given growing support for using and pointed out misleading error message in [microsoft/TypeScript#55538](https://github.com/microsoft/TypeScript/issues/55538#issuecomment-5069593738)

## Activity Summary

### [Issue microsoft/TypeScript#55538](https://github.com/microsoft/TypeScript/issues/55538) (Closed, `Suggestion`, `Awaiting More Feedback`)

**When using disposable, typescript should never report the variable as unused**

*TypeScript should not flag variables declared with using as unused since they are implicitly used for disposal.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/55538#issuecomment-1696093660) **andrewbranch** said "I agree; I think it looks wrong enough that the _ prefix, if it was really intended to be unused by explicit code, is really valuable."
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/55538#issuecomment-1948309886) **KristjanTammekivi** referenced the discard-binding proposal and remarked that they had to wait for it
 * (2.4 years ago) **KristjanTammekivi** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/55538#issuecomment-5069593738) **matthieusieben** suggested reconsidering the issue due to growing support for using, described a workaround for non-disposable dependencies, and noted that the error message was misleading because variables were used implicitly

### [Issue microsoft/TypeScript#63673](https://github.com/microsoft/TypeScript/issues/63673) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-07\-21**

*A custom Go linting pass is being prototyped to encode TypeScript-like type guard invariants for strict nil checking and prevent nil dereferences.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Design Notes`

### [Issue microsoft/TypeScript#63674](https://github.com/microsoft/TypeScript/issues/63674) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-06\-23**

*Discuss inferring types for trivial no-return function bodies in isolatedDeclarations, addressing never-returning calls and void versus undefined.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Design Notes`

### [PR microsoft/TypeScript#63675](https://github.com/microsoft/TypeScript/pull/63675) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove twoslash\-repros workflow**

*Remove the twoslash-repros workflow from the repository since it has been disabled for some time.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63676](https://github.com/microsoft/TypeScript/issues/63676) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-07\-23**

*Design meeting to define a JavaScript emit API with flexible output options and support for custom content mappers*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Design Notes`

### [Issue microsoft/TypeScript#63677](https://github.com/microsoft/TypeScript/issues/63677) (Open)

**type parameter variance in generic call signature is incorrectly bivariant**

*TypeScript incorrectly allows bivariant assignments for invariant generic call signatures, resulting in unsound type checking.*

 * created by **ahmedajiz629**

### [Issue microsoft/TypeScript#63678](https://github.com/microsoft/TypeScript/issues/63678) (Open)

**tsc \-\-watch doesn't work on NTFS partitions on Linux**

*After upgrading to TypeScript 7, tsc --watch fails on Linux NTFS partitions due to fanotify_mark no such device errors.*

 * created by **bt7s7k7**

