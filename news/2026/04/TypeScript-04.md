# Report for 2026-04-04 (Saturday, April 4th, 2026)

7 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @Arlen22 provided repro steps as requested in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4187787975)
    * @AbhinavJD7 asked to be assigned to investigate the issue in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4188436610)
    * @deepnav4 expressed interest in working on the issue in [microsoft/TypeScript#63352](https://github.com/microsoft/TypeScript/issues/63352#issuecomment-4188736423)

## Activity Summary

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`, `Domain: LS: TSServer`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3961671540) **Arlen22** said "Ok, this doesn't happen in every project, so it might be more on the typescript side of things. "
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3985103294) **Arlen22** described being unable to rename generic type parameters in one part of the project and expressed confusion about an underlying dependency or type issue
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4187180248) **Arlen22** described that intellisense broke whenever opening JavaScript or TypeScript files outside the project and mentioned a workaround using a separate workspace
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4187742289) **Arlen22** described that reloading the window after closing offending tabs fixed the issue and that the TS server took longer to recognize removed files, suggesting VS Code crossover
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4187787975) **Arlen22** reproduced the issue when importing from es-arraybuffer-base64 and noted that declaration files couldn't be found and a window reload was still required without using the {} as syntax
 * [later](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4188436610) **AbhinavJD7** asked to be assigned to investigate the issue, described reproducing locally with large node_modules and tracing why the InferredProject graph update hangs

### [Issue microsoft/TypeScript#63311](https://github.com/microsoft/TypeScript/issues/63311) (Closed, `Not a Defect`)

**\`typescript\.d\.ts\` uses ES2015\+ globals \(\`Map\`, \`ReadonlyMap\`\) without \`/// \<reference lib\>\` directive**

*typescript.d.ts uses ES2015 Map and ReadonlyMap without a /// <reference lib='es2015' /> directive, causing type errors outside ES2015 contexts.*

 * **RyanCavanaugh** added label `Not a Defect`
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63311#issuecomment-4154354423) **RyanCavanaugh** said "TypeScript itself doesn't run in environments that predate these values, so if anything this is helpful for indicating that your config is wrong in some way."
 * (5 days ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63311#issuecomment-4188391751) **baraknaveh** said "Sorry folks for the trouble, it turns it it was my misconfiguration at fault, and then my misdiagnosis of the issue."

### [Issue microsoft/TypeScript#63332](https://github.com/microsoft/TypeScript/issues/63332) (Closed, `Duplicate`)

**instanceof narrowing should respect type parameter bounds for covariant types**

*TypeScript’s instanceof narrowing of generic covariant classes defaults type parameters to any instead of their bounded unions*

 * created by **ethanresnick**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63332#issuecomment-4179453589) **MartinJohns** said "Duplicate of #17473."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63332#issuecomment-4188069311) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63333](https://github.com/microsoft/TypeScript/issues/63333) (Closed, `Duplicate`)

**JSON\.stringify should disallow BigInt value**

*Restrict JSON.stringify’s parameter type to disallow BigInt values and prevent runtime errors.*

 * created by **wyattscarpenter**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63333#issuecomment-4176413347) **nmain** inquired what type the argument to JSON.stringify would have and referenced issues #1897 and #4196
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63333#issuecomment-4188069273) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63352](https://github.com/microsoft/TypeScript/issues/63352) (Open, `Bug`, `Domain: lib.d.ts`)

**Trivial: typo**

*Corrects the misspelling of “parameter” as “paramater” in the es5.d.ts definitions file.*

 * created by **tomhamiltonlambda**
 * [later](https://github.com/microsoft/TypeScript/issues/63352#issuecomment-4188736423) **deepnav4** expressed interest in working on the issue

### [Issue microsoft/TypeScript#63353](https://github.com/microsoft/TypeScript/issues/63353) (Closed)

**Declaration emit references imported type without importing it when inheriting static methods via CommonJS \`require\`**

*Declaration emitter omits import for a referenced typedef and emits an unused require import when inheriting static methods via CommonJS.*

 * created by **avivkeller**

