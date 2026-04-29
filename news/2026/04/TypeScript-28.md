# Report for 2026-04-28 (Tuesday, April 28th, 2026)

7 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @christopher-buss reported that the import from 'typescript/lib/tsserverlibrary' in createProjectService.ts broke their update in [microsoft/TypeScript#63422](https://github.com/microsoft/TypeScript/issues/63422#issuecomment-4339232110)
    * @MARIUAM asked if there was any workaround for monorepo module resolution or if compiler logic limits lookups to standard node resolution in [microsoft/TypeScript#63448](https://github.com/microsoft/TypeScript/issues/63448#issuecomment-4343147401)

## Activity Summary

### [Issue microsoft/TypeScript#63422](https://github.com/microsoft/TypeScript/issues/63422) (Closed)

**@typescript/typescript6 does not proxy subpath imports**

*@typescript/typescript6@6.0.0 omits a subpath exports map and tsserverlibrary file, so requiring typescript/lib/tsserverlibrary fails.*

 * created by **christopher-buss**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63422#issuecomment-4297927484) **RyanCavanaugh** provided an auto-generated list of similar issues and suggested closing duplicates
 * [today](https://github.com/microsoft/TypeScript/issues/63422#issuecomment-4339074443) **RyanCavanaugh** said "What do you need specifically from tsserverlibrary.js that isn't in typescript.js?"
 * [today](https://github.com/microsoft/TypeScript/issues/63422#issuecomment-4339232110) **christopher-buss** mentioned that the import type from 'typescript/lib/tsserverlibrary' in createProjectService.ts was breaking their update
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63441](https://github.com/microsoft/TypeScript/issues/63441) (Open, `Bug`)

**\`symbolToNode\` stack overflow when using recursive types and functions with type parameters**

*Recursive generic functions and types cause TypeScript's symbolToNode to exceed the maximum call stack size.*

 * created by **StyleShit**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63441#issuecomment-4328571967) **RyanCavanaugh** provided an automated list of similar issues
 * **RyanCavanaugh** added label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/63441#issuecomment-4338973674) **RyanCavanaugh** said "Repros in tsgo as well"
 * [today](https://github.com/microsoft/TypeScript/issues/63441#issuecomment-4339631166) **RyanCavanaugh** shared a Go stack trace from the typescript-go checker

### [PR microsoft/TypeScript#63443](https://github.com/microsoft/TypeScript/pull/63443) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 5 updates**

*Update five GitHub Actions packages in the root directory to newer versions.*

 * (2 days ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63443#issuecomment-4342434504) **G-11-P** said "Merge approval granted"

### [Issue microsoft/TypeScript#63447](https://github.com/microsoft/TypeScript/issues/63447) (Open, `Duplicate`)

**5\.9 regression: Union types served by mutually exclusive function overloads not working**

*TypeScript 5.9 fails to apply mutually exclusive overloads for functions accepting ArrayBuffer or Uint8Array.*

 * created by **hyperair**
 * [today](https://github.com/microsoft/TypeScript/issues/63447#issuecomment-4333882436) **hyperair** provided a workaround by checking if data was a Uint8Array before calling bar
 * [today](https://github.com/microsoft/TypeScript/issues/63447#issuecomment-4333955742) **MartinJohns** explained that the behavior change was due to type narrowing changes in TypeScript 5.9 and recommended removing the overload in favor of a union type parameter
 * [today](https://github.com/microsoft/TypeScript/issues/63447#issuecomment-4337372133) **RyanCavanaugh** provided an automated list of similar issues
 * **RyanCavanaugh** added label `Duplicate`
 * [later](https://github.com/microsoft/TypeScript/issues/63447#issuecomment-4342003676) **hyperair** thanked MartinJohns for explaining that the change in lib.d.ts narrowed types and broke the usecase, and noted that modifying the Buffer.from signature in @types/node is difficult

### [Issue microsoft/TypeScript#63448](https://github.com/microsoft/TypeScript/issues/63448) (Open)

**\`libReplacement: true\` lookup folder should be configurable \(via \`typeRoots\` ?\)**

*Enable configuring the module resolution path for @typescript/lib-dom when using libReplacement via typeRoots*

 * created by **freshp86**
 * [later](https://github.com/microsoft/TypeScript/issues/63448#issuecomment-4341653294) **MartinJohns** said "Shouldn't it work if you point to your local package via devDependencies in your packages.json file?"
 * [later](https://github.com/microsoft/TypeScript/issues/63448#issuecomment-4343147401) **MARIUAM** asked whether there was a workaround or if the compiler restricted @typescript/lib- lookups to standard node resolution

