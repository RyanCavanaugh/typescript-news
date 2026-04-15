# Report for 2026-04-11 (Saturday, April 11th, 2026)

7 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @Arlen22 reported that configuration changes did not resolve the issue and seek further assistance in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4230165560)
    * @dagangtj offered to work on the issue and submit a PR shortly in [microsoft/TypeScript#63352](https://github.com/microsoft/TypeScript/issues/63352#issuecomment-4229744543)
    * @denis-migdal reported that default generic parameters cause lazy inference and suggested a workaround in [microsoft/TypeScript#63377](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4231435840)
    * @dagangtj offered to implement the missing `es2025` option in the jsconfig.json schema in [microsoft/TypeScript#63379](https://github.com/microsoft/TypeScript/issues/63379#issuecomment-4230722185)
    * @afurm asked if charCodeAt, codePointAt, and substring out-of-bounds behaviors are documented and if corresponding documentation updates are needed in [microsoft/TypeScript#63386](https://github.com/microsoft/TypeScript/pull/63386#issuecomment-4229758174)

## Activity Summary

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`, `Domain: LS: TSServer`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4187742289) **Arlen22** described that reloading the window after closing offending tabs fixed the issue and that the TS server took longer to recognize removed files, suggesting VS Code crossover
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4187787975) **Arlen22** reproduced the issue when importing from es-arraybuffer-base64 and noted that declaration files couldn't be found and a window reload was still required without using the {} as syntax
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4188436610) **AbhinavJD7** asked to be assigned to investigate the issue, described reproducing locally with large node_modules and tracing why the InferredProject graph update hangs
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4230165560) **Arlen22** reported that adding watchOptions to tsconfig.json and VSCode settings didn't fix the issue, and that enabling project diagnostics broke intellisense
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4230346939) **Arlen22** said "The experimental tsgo vscode plugin does not have any of these problems."

### [Issue microsoft/TypeScript#63352](https://github.com/microsoft/TypeScript/issues/63352) (Closed, `Bug`, `Domain: lib.d.ts`)

**Trivial: typo**

*Corrects the misspelling of “parameter” as “paramater” in the es5.d.ts definitions file.*

 * (5 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63352#issuecomment-4229744543) **dagangtj** said "I'd like to work on this. I'll submit a PR shortly."

### [Issue microsoft/TypeScript#63377](https://github.com/microsoft/TypeScript/issues/63377) (Closed, `Question`)

**TS doesn't properly infer generic callback \`\<T\>\(x: X\<T\>\) =\> T\` when providing \`\(x\) =\> new T\(\)\` \(parameter defined without type\)**

*TypeScript does not infer a generic callback’s type when its parameter is untyped, resulting in any instead.*

 * (2 days ago) **RyanCavanaugh** added label `Question`, and removed label `Unactionable`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4221303828) **denis-migdal** thanked for the answer, described two possible inference results for createViewClass2, and asked if using a const generic parameter would select the more precise inference
 * [later](https://github.com/microsoft/TypeScript/issues/63377#issuecomment-4231435840) **denis-migdal** described that defaulting a generic type parameter can cause lazy inference and suggested removing the default as a workaround

### [Issue microsoft/TypeScript#63379](https://github.com/microsoft/TypeScript/issues/63379) (Open, `Docs`)

**\`es2025\` is not a valid enum option for \`jsconfig\.json\`'s \`compilerOptions\.target\` enum**

*The JSON schema for jsconfig.json/tsconfig.json compilerOptions.target enum doesn’t include 'es2025' as a valid option.*

 * created by **Abrifq**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63379#issuecomment-4215183885) **MartinJohns** noted the option was missing in jsconfig
 * **RyanCavanaugh** added label `Docs`
 * [today](https://github.com/microsoft/TypeScript/issues/63379#issuecomment-4230722185) **dagangtj** offered to work on the issue by adding the missing es2025 option to the jsconfig.json schema

### [Issue microsoft/TypeScript#63383](https://github.com/microsoft/TypeScript/issues/63383) (Closed, `Working as Intended`, **mjbvz**)

**Typescript 'rootDir' error**

*VSCode 1.114+ incorrectly reports TypeScript rootDir errors in a multi-package monorepo configuration despite successful CLI compilation*

 * created by **m-hall**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [later](https://github.com/microsoft/TypeScript/issues/63383#issuecomment-4231365032) **mkantor** advised explicitly setting rootDir when upgrading to TypeScript 6.0 and suggested using ts5to6 to automate the change

### [PR microsoft/TypeScript#63386](https://github.com/microsoft/TypeScript/pull/63386) (Open)

**Document charAt edge case behavior**

*Document that String.charAt returns an empty string for indexes outside the valid range to ensure consistency.*

 * created by **bwalter007**
 * [today](https://github.com/microsoft/TypeScript/pull/63386#issuecomment-4229758174) **afurm** acknowledged the clarification and asked whether charCodeAt, codePointAt, and substring out-of-bounds behaviors are documented and if documentation updates are needed

### [PR microsoft/TypeScript#63390](https://github.com/microsoft/TypeScript/pull/63390) (Closed, `For Uncommitted Bug`)

**feat: Higher\-Kinded Types prototype \(parser \+ RFC\)**

*Prototype parser support for higher-kinded types with an accompanying RFC outlining phased syntax, kind inference, and future checker integration.*

 * created by **SAY-5**

### [Issue microsoft/TypeScript#63391](https://github.com/microsoft/TypeScript/issues/63391) (Open, `Bug`, `Domain: JS Emit`, `Fix Available`)

**The module namespace object returned by \_\_importStar is not the same when import the same module multiple times**

*TypeScript’s compiled CommonJS __importStar helper creates separate namespace objects for repeated imports of the same module.*

 * created by **yanjiew1**

### [Issue microsoft/TypeScript#63392](https://github.com/microsoft/TypeScript/issues/63392) (Open, `Docs`, **RyanCavanaugh**)

**Review/update https://typescriptlang\.org/tsconfig for TS 6\.0**

*The TypeScript tsconfig documentation is outdated for version 6.0, showing incorrect defaults and options for target, types, paths, rootDir, and module.*

 * created by **mkantor**
 * [later](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4231401777) **mkantor** suggested relocating the issue to the TypeScript-Website repository while noting template and visibility concerns, and offered to refile it if desired
 * [later](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4231403772) **mkantor** offered to draft a pull request but deferred to a maintainer and asked if a first pass would be helpful
 * [later](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4231410817) **mkantor** said "If anyone spots additional items requiring attention, please post them as comments and I'll add them to my list."

