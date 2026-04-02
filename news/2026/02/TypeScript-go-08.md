# Report for 2026-02-08 (Sunday, February 8th, 2026)

3 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @Knagis pointed out a contradiction between the TypeScript documentation and a previous statement by @jakebailey in [microsoft/TypeScript-go#2699](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3872036706)

## Activity Summary

### [PR microsoft/TypeScript-go#2331](https://github.com/microsoft/TypeScript-go/pull/2331) (Closed)

**Organize Imports**

*Implement functionality to automatically organize and sort imports within source files.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3820320228) **iisaduan** identified missing indenting logic that could affect organize imports and cause a loss of smaller indent
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3825049874) **johnfav03** updated the code to account for the shebang issue, changed textwriter.go to use ls.formatOptions.indentSize instead of hardcoded spaces, noted the LSP still didn’t sync indentSize settings, and explained that require statements are sorted separately following TypeScript’s import order
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3825234891) **jakebailey** said "I think there's a bug in the way we load indent size out of the settings; it's some discrepency i noticed when working on my user prefs refactor. VS Code's setting has a different name than we do."
 * (later) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#2699](https://github.com/microsoft/TypeScript-go/issues/2699) (Open)

**tsgo resolves inherited include/exclude globs differently than tsc when using extends**

*tsgo resolves inherited include globs relative to the child config rather than the parent, causing a different output structure than tsc.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861930896) **mabels** noted that there was no app in a specific directory and suggested a link to the large app repository
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861948071) **jakebailey** provided a link to the repro directory, suggested setting rootDir to "../../", and noted that includes are not inherited
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861987821) **mabels** ran builds with tsc and tsgo and demonstrated that tsgo scattered .js and .js.map files throughout the monorepo
 * [later](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3872036706) **Knagis** highlighted a contradiction between the TypeScript tsconfig inheritance docs and @jakebailey’s earlier statement

### [PR microsoft/TypeScript-go#2712](https://github.com/microsoft/TypeScript-go/pull/2712) (Open)

**Replace unsafe\.Pointer for seen symbol tables with unique ID**

*Use existing Node or Symbol IDs plus metadata instead of unsafe.Pointer to optimize symbol table tracking.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2713](https://github.com/microsoft/TypeScript-go/pull/2713) (Closed, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.0 to 4\.32\.2 in the github\-actions group across 1 directory**

*Upgrade github/codeql-action from 4.32.0 to 4.32.2 to update the default CodeQL bundle to v2.24.1.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787) (Closed)

**\`UnionToTuple\` type returns "inverted" tuple in TSGO compared to TypeScript 5\.8\.3 and gives type error**

*TSGO's UnionToTuple type generates tuples in reverse order compared to TypeScript 5.8.3, causing type errors*

 * (43 weeks ago) **alexwork1611** closed the issue
 * [40 weeks ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-2844237064) **LukeAbby** explained that uncommenting a declaration changes the tuple order produced by UnionToTuple, and that adding types elsewhere can lead to inconsistent ordering
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3866952237) **juhort** asked whether the union order would always be the same given identical generic inputs, avoiding issues like the one mentioned by LukeAbby
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3867504473) **jakebailey** said "Yes, correct."
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3867505544) **jakebailey** said "In the 6.0 nightly, you can now also pass --stableTypeOrdering to try this sorting out early."

