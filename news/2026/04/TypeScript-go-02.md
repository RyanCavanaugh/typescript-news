# Report for 2026-04-02 (Thursday, April 2nd, 2026)

13 different users commented on 25 different issues.

## Recommended Actions

 * Response Recommended
    * @psznm provided reproduction steps and examples for import suggestion issue in [microsoft/TypeScript-go#2974](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-4179268991)
    * @Tangxinwei provided TypeScript version information and reproduction link in [microsoft/TypeScript-go#3321](https://github.com/microsoft/TypeScript-go/issues/3321#issuecomment-4182684367)
    * @aamoghS requested review of their pull request in [microsoft/TypeScript-go#3326](https://github.com/microsoft/TypeScript-go/pull/3326#issuecomment-4180189873)

## Activity Summary

### [Issue microsoft/TypeScript-go#2021](https://github.com/microsoft/TypeScript-go/issues/2021) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**source file binary format is not work**

*@typescript/ast’s binary format misreads AST nodes due to empty parameter slots and faulty child indexing assumptions.*

 * created by **quininer**
 * **jakebailey** added label `Domain: API and Extensibility`
 * **RyanCavanaugh** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2021#issuecomment-4179088551) **andrewbranch** said "getOrCreateChildAtNodeIndex has been fixed; empty vs. nil NodeLists are still an issue in some places, but there fixes staged at #3195 and an alternative I'm working on locally."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2437](https://github.com/microsoft/TypeScript-go/issues/2437) (Open, `Domain: Editor`, **sandersn**)

**TSGo prioritizes \`tsconfig\.json\` over \`jsconfig\.json\` in the same directory, even for file types the former excludes**

*When both config files reside in the same directory, TSGo always prioritizes tsconfig.json over jsconfig.json, disabling JavaScript type checking.*

 * created by **Bertie690**
 * **Bertie690** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **sandersn**

### [Issue microsoft/TypeScript-go#2911](https://github.com/microsoft/TypeScript-go/issues/2911) (Open, `Non-regression`)

**TS4053 happens when public class method adopts imported type from library**

*Public methods in an exported class using an imported library type cause TS4053 errors with tsgo.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-4105529495) **jakebailey** said "I'm only assigned because I assigned copilot to it, which didn't really work."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-4105652784) **jakebailey** asked if the issue wasn't a regression because it persisted in both ts6 and ts7
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-4105800838) **hkleungai** stated that the bug may be new or a rediscovery in TypeScript and offered to open an issue in the TypeScript repo if needed
 * (today) **RyanCavanaugh** added label `Non-regression`, set milestone to `Post-7.0`, and unassigned **jakebailey**, **Copilot**

### [Issue microsoft/TypeScript-go#2974](https://github.com/microsoft/TypeScript-go/issues/2974) (Open, `Domain: Editor`, **andrewbranch**)

**Missing auto\-import for subpath imports of other local packages**

*VS Code TypeScript auto-imports fail to recognize subpath imports from sibling local workspace packages.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-3999163817) **andrewbranch** said "I think this is “working as intended” because the other packages aren’t listed as dependencies. Does it work as you expect if you add them to pkg1's package.json "dependencies"?"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-3999487766) **psznm** tried the suggested changes, added the dependency and moved imports, observed the package import suggestion appear but the subpath import suggestion remain missing
 * **RyanCavanaugh** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-4179050011) **andrewbranch** noted that they investigated the issue but deferred it due to the complexity of supporting imports targets that are package names, which involve additional resolution steps and could impact performance
 * [today](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-4179268991) **psznm** described that import suggestions did not work for relative paths outside the tsconfig directory and provided examples and a workaround
 * [today](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-4179560164) **andrewbranch** explained that files from another package are resolved via node_modules specifiers without computing another name and noted uncertainty about using imports with relative paths to other packages
 * [today](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-4179659897) **psznm** described that deleting node_modules/pkg2 enabled auto imports for "#pkg4/*" but that the workaround failed without including ../pkg2 in tsconfig.json

### [Issue microsoft/TypeScript-go#3054](https://github.com/microsoft/TypeScript-go/issues/3054) (Open, `feature parity`, **jakebailey**)

**\`tsgo \-\-generateTrace\` appears unimplemented**

*The tsgo CLI’s documented --generateTrace flag requires an argument but does nothing and fails to produce trace output like tsc.*

 * created by **DorianListens**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3054#issuecomment-4035059255) **jakebailey** referred to issue #2914 and suggested trying --pprofDir . while noting it might not be specific enough
 * **RyanCavanaugh** added label `feature parity`
 * **RyanCavanaugh** assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#3121](https://github.com/microsoft/TypeScript-go/issues/3121) (Closed, `Needs More Info`)

**extension gets uninstalled after around an hour on vscodium**

*The TypeScript Native Preview extension installed in VSCodium on Linux is uninstalled after about an hour for being flagged problematic.*

 * **RyanCavanaugh** added label `Needs More Info`
 * (yesterday) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4175811753) **huseeiin** explained that they downloaded the VSIX from VSCode and installed it in VSCodium via the codium --install-extension command
 * [today](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4178958614) **RyanCavanaugh** stated that downloading the VSIX from VSCode and installing it in VSCodium was not supported

### [Issue microsoft/TypeScript-go#3312](https://github.com/microsoft/TypeScript-go/issues/3312) (Open, `Domain: Editor`)

**latest release \[0\.20260401\.1\] breaks LSP on VS code**

*Version 0.20260401.1 of the extension fails to load in VS Code 1.113.0 on Linux due to a missing typescript.native-preview-enable command*

 * created by **christophe-g**
 * **christophe-g** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3312#issuecomment-4180470533) **jakebailey** expressed inability to see how the issue could occur and asked for additional logs
 * [today](https://github.com/microsoft/TypeScript-go/issues/3312#issuecomment-4180756346) **christophe-g** thanked maintainers, reverted to version 0.20260331.1 due to no logs, and promised to report results of issue #3333 when deployed
 * [today](https://github.com/microsoft/TypeScript-go/issues/3312#issuecomment-4180780205) **jakebailey** linked the commit range and stated that only the LSP change exists which wouldn’t affect activation

### [PR microsoft/TypeScript-go#3317](https://github.com/microsoft/TypeScript-go/pull/3317) (Closed)

**Fix default cases in custom Registration UnmarshalJSONFrom**

*Add missing error handling for default cases in the custom Registration UnmarshalJSONFrom unmarshaller.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3321](https://github.com/microsoft/TypeScript-go/issues/3321) (Closed, **jakebailey**, **Copilot**)

**\#\#\# Bug Report: Optional chaining \`\(A?\.B as any\)\.C\(\)\` incorrectly transpiled as \`\(A?\.B\)\.C\(\)\`**

*tsgo 7.0.0-dev erroneously transpiles `(A?.B as any).C()` as `(A?.B).C()`, causing runtime errors when A is undefined.*

 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3321#issuecomment-4174228658) **jakebailey** disputed tsc's behavior and provided a reproducible example link
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3321#issuecomment-4182684367) **Tangxinwei** provided a playground link and noted that behavior changed in higher versions while using tsc 4.4.4

### [Issue microsoft/TypeScript-go#3323](https://github.com/microsoft/TypeScript-go/issues/3323) (Closed)

**tsgo stops reporting subsequent errors after TS2880 \(diagnostics short\-circuit vs tsc\)**

*tsgo halts error reporting after the initial TS2880 import assertion error instead of listing subsequent diagnostics.*

 * created by **bamcop**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3323#issuecomment-4174485116) **jakebailey** said "Yes, this is now a parsing error in 7.0."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3324](https://github.com/microsoft/TypeScript-go/issues/3324) (Closed, `bug`, **jakebailey**, **RyanCavanaugh**, **Copilot**)

**Different \`\-\-showConfig\` output**

*tsgo's --showConfig output differs from tsc by omitting file listings, using numeric enum values, and absolute paths.*

 * (today) **RyanCavanaugh** assigned to **jakebailey**, **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added label `bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3325](https://github.com/microsoft/TypeScript-go/issues/3325) (Closed, `Domain: Editor`, **RyanCavanaugh**, **Copilot**)

**The declaration of the deconstructing parameters of a function is marked as \`var\` instead of \`parameter\`**

*The Tsgo extension’s hover tooltip incorrectly displays destructured function parameters as var instead of parameter.*

 * **Withered-Flower-0422** added label `Domain: Editor`
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3326](https://github.com/microsoft/TypeScript-go/pull/3326) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix \`\-\-showConfig\` output: add implied compiler options**

*Support emitting implied compiler options in tsgo --showConfig output to align with tsc behavior*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3326#issuecomment-4179695414) **RyanCavanaugh** displayed tsgo --init and tsgo --showconfig output
 * [today](https://github.com/microsoft/TypeScript-go/pull/3326#issuecomment-4179940078) **RyanCavanaugh** said "@copilot address comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3326#issuecomment-4180082577) **RyanCavanaugh** said "@copilot address comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3326#issuecomment-4180189873) **aamoghS** said "Do you guys mind checking my pr, I think it would address the issue because copilot will keep going in the same loop "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3326#issuecomment-4180414881) **aamoghS** praised the architectural pivot in commit 92de5b7 for delegating to core getters to maintain a single source of truth and prevent logic drift
 * [today](https://github.com/microsoft/TypeScript-go/pull/3326#issuecomment-4180490387) **RyanCavanaugh** said "@copilot address comments"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3327](https://github.com/microsoft/TypeScript-go/pull/3327) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix destructured binding hover displaying wrong keyword \(\`var\` instead of \`\(parameter\)\`, \`const\`, or \`let\`\)**

*Update hover implementation to ascend destructured bindings and display the correct var, let, const, or parameter prefix.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3327#issuecomment-4179099864) **ahejlsberg** suggested changing the assignment to use ast.GetRootDeclaration(symbol.ValueDeclaration) for both const and let destructuring
 * [today](https://github.com/microsoft/TypeScript-go/pull/3327#issuecomment-4179133826) **Copilot** implemented the change to decl assignment, reverted to ast.IsParameter, and expanded tests for const/let/var destructuring declarations
 * [today](https://github.com/microsoft/TypeScript-go/pull/3327#issuecomment-4179684154) **Copilot** fixed test errors by updating the baselines for quickInfoForObjectBindingElementName03, 04, and 05 to show `(parameter)` instead of `var`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3328](https://github.com/microsoft/TypeScript-go/pull/3328) (Open, **andrewbranch**, **Copilot**)

**Fix auto\-imports inserting \`import\` in CJS files under node16/node20/nodenext**

*Auto-imports with Node16/20/nodenext targets incorrectly insert ES import statements into CommonJS files instead of require calls due to flawed detection logic.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#3329](https://github.com/microsoft/TypeScript-go/pull/3329) (Open, **andrewbranch**, **Copilot**)

**Add regression tests for auto\-import preferring matching type\-only declarations \(\#3244\)**

*Add regression tests ensuring auto-import correctly appends value and type imports to matching existing declarations.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3329#issuecomment-4180824824) **andrewbranch** said "@copilot looks right, but tests are unchanged, so you need to add one"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3329#issuecomment-4180877695) **Copilot** added three fourslash tests and explained the key test demonstrating the divergence between isTypeOnlyLocation and IsValidTypeOnlyAliasUseSite in an incomplete type argument position

### [PR microsoft/TypeScript-go#3330](https://github.com/microsoft/TypeScript-go/pull/3330) (Open)

**Fix \-\-showConfig output: add compileOnSave and implied compiler options**

*Add compileOnSave and implied compiler options to the output of the --showConfig flag.*

 * created by **aamoghS**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3330#issuecomment-4179950383) **aamoghS** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#3331](https://github.com/microsoft/TypeScript-go/pull/3331) (Open)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Port the trie-based implementation for removeStringLiteralsMatchedByTemplateLiterals from upstream TypeScript pull request 63343.*

 * created by **eps1lon**

### [PR microsoft/TypeScript-go#3332](https://github.com/microsoft/TypeScript-go/pull/3332) (Closed)

**Fix crash for nil child config**

*Add checks to handle nil project references returned by GetResolvedProjectReferences to avoid crashes.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3333](https://github.com/microsoft/TypeScript-go/pull/3333) (Open)

**Activate extension on typescript\.native\-preview\.enable**

*Enable extension activation when the typescript.native-preview.enable setting is enabled.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3334](https://github.com/microsoft/TypeScript-go/pull/3334) (Open)

**Implement multi\-file doc highlights**

*Implement a new VS Code LSP extension method to support document highlights across multiple files.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3335](https://github.com/microsoft/TypeScript-go/issues/3335) (Closed)

**tsgo \-\-build hangs on storybook tsconfig with ~100 story files \(possible regression of \#2678\)**

*tsgo build hangs indefinitely when typechecking a Storybook tsconfig containing around 100 story files.*

 * created by **nicolas-besnard**
 * (later) **nicolas-besnard** closed the issue

### [Issue microsoft/TypeScript-go#3336](https://github.com/microsoft/TypeScript-go/issues/3336) (Open)

**7\.0\.0\-dev\.20260403\.1 lsp diagnostic params fail to unmarshall in Helix**

*Upgrading to 7.0.0-dev.20260403.1 causes Helix LSP diagnostics to fail due to invalid null previousResultId during JSON unmarshalling.*

 * created by **kanashimia**

