# Report for 2026-02-16 (Monday, February 16th, 2026)

7 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @theoludwig provided reproduction steps and confirmed a regression in TS7 in [microsoft/TypeScript-go#2797](https://github.com/microsoft/TypeScript-go/issues/2797#issuecomment-3910885285)
    * @theoludwig provided repro steps and verification that reverting the commit fixes the issue in [microsoft/TypeScript-go#2797](https://github.com/microsoft/TypeScript-go/issues/2797#issuecomment-3910984219)

## Activity Summary

### [Issue microsoft/TypeScript-go#1389](https://github.com/microsoft/TypeScript-go/issues/1389) (Open, `Domain: Editor`, `Crash`, **Copilot**)

**lsp\(vscode\): panic when formatting a file with multi\-byte characters and trailing 2\+ newlines**

*VSCode's TypeScript (Native Preview) extension panics when formatting files containing multi-byte characters and at least two trailing newlines*

 * (31 weeks ago) **jakebailey** added labels `Domain: Editor`, `Crash`, and assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1389#issuecomment-3910670391) **apendua** said "I couldn't reproduce it with the latest version from main branch. Could it be that some other fix also resolved this issue? Can you double check?"

### [Issue microsoft/TypeScript-go#2790](https://github.com/microsoft/TypeScript-go/issues/2790) (Closed, `Crash`, **ahejlsberg**)

**Panic when \`\.js\` file in composite project contains import inside JSDoc type annotation**

*A .js file containing an import in a JSDoc type annotation causes a panic in a composite project.*

 * **ahejlsberg** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2790#issuecomment-3909016238) **ahejlsberg** said "This one is sneaky. It appears that the parser's look-ahead logic isn't rewinding our JSDoc node cache, so we end up with abandoned JSDoc nodes in the cache."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2790#issuecomment-3909220615) **Andarist** said "@ahejlsberg I was just working on diagnosing this in the last hours and put up a PR here: https://github.com/microsoft/typescript-go/pull/2795"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2790#issuecomment-3909485488) **ahejlsberg** acknowledged that not rewinding the reparsed clones list was the real culprit, noted additional JSDoc cache leaks, and proposed merging the existing PR first before submitting their own fixes with tests
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2794](https://github.com/microsoft/TypeScript-go/pull/2794) (Closed, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.2 to 4\.32\.3 in the github\-actions group across 1 directory**

*Upgrades github/codeql-action from v4.32.2 to v4.32.3, adding experimental support for testing connections to private package registries.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2795](https://github.com/microsoft/TypeScript-go/pull/2795) (Closed)

**Rewind reparsed clones after speculative parsing failures**

*Rewind cloned parser state after speculative parsing failures to preserve correct parsing behavior.*

 * created by **Andarist**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2796](https://github.com/microsoft/TypeScript-go/pull/2796) (Closed)

**Record \(and possibly rewind\) JSDoc info, create JSDoc cache separately**

*Follow-up PR records and optionally rewinds JSDoc occurrences while separating cache creation to avoid storing discarded JSDoc objects.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2797](https://github.com/microsoft/TypeScript-go/issues/2797) (Closed, **ahejlsberg**)

**TS2488: Generic type parameter not inferred from JSX props, falls back to default**

*A tsgo bug prevents inferring a generic JSX component's type parameter from its selector prop, incorrectly triggering TS2488.*

 * created by **theoludwig**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2797#issuecomment-3910667304) **jakebailey** said "Can you please check against TS 6.0, not 5.9?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2797#issuecomment-3910885285) **theoludwig** tested the reproduction with TypeScript v6 beta and v7 dev, found errors only in v7 indicating a regression, and provided links to a sample repo and relevant commits
 * [today](https://github.com/microsoft/TypeScript-go/issues/2797#issuecomment-3910903910) **theoludwig** noted that the PR altered `[Symbol.iterator]()` behavior, referenced its implementation in TypeScript v6, and suggested it might help
 * [today](https://github.com/microsoft/TypeScript-go/issues/2797#issuecomment-3910984219) **theoludwig** identified the problematic commit and confirmed that reverting it resolves the errors
 * **jakebailey** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#2798](https://github.com/microsoft/TypeScript-go/issues/2798) (Closed, `Crash`)

**Panic in textDocument/diagnostics on private property assignment at "global" this**

*Assigning a private property to the global this context triggers a nil pointer dereference panic in TypeScript-Go’s LSP diagnostics*

 * created by **apendua**
 * **apendua** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2798#issuecomment-3910617702) **apendua** identified that GetSymbolNameForPrivateIdentifier requires a non-null first argument but thisType.symbol was nil when this was undefined due to export {}

### [PR microsoft/TypeScript-go#2799](https://github.com/microsoft/TypeScript-go/pull/2799) (Closed)

**Add nil assertion for thisType\.symbol**

*Add a nil assertion for thisType.symbol in GetSymbolNameForPrivateIdentifier to handle global this without a symbol.*

 * created by **apendua**

### [PR microsoft/TypeScript-go#2800](https://github.com/microsoft/TypeScript-go/pull/2800) (Closed)

**Fix crash in completion on JSX element**

*Resolve a crash in code completion when invoked on JSX elements.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2801](https://github.com/microsoft/TypeScript-go/pull/2801) (Closed)

**Parse JSDoc lazily in TS files, eliminate JSDocParsingMode**

*Eliminate the JSDocParsingMode setting and defer parsing of JSDoc in TypeScript files until needed to streamline AST caching*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2801#issuecomment-3911746991) **jakebailey** explained that the current implementation hurts check and requested a variant returning only precalculated/eager JSDoc

### [Issue microsoft/TypeScript-go#2802](https://github.com/microsoft/TypeScript-go/issues/2802) (Closed)

**JSX with generics loses type inference on \`children\` if its a callback**

*A regression in tsgo v7.0.0-dev.20260213.1 breaks type inference for generic JSX components’ callback children props but not for other callbacks.*

 * created by **Gabrola**

### [PR microsoft/TypeScript-go#2803](https://github.com/microsoft/TypeScript-go/pull/2803) (Closed)

**Fixed JSX context\-sensitive children discrimination for generic signatures**

*Fixes context-sensitive children discrimination in JSX generic signatures to address two related typescript-go issues.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#2804](https://github.com/microsoft/TypeScript-go/pull/2804) (Closed)

**Fix panic in organizeImports for \.d\.ts files with unused imports matching module augmentations**

*OrganizeImports crashes on .d.ts files with unused imports matching module augmentations.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787) (Closed)

**\`UnionToTuple\` type returns "inverted" tuple in TSGO compared to TypeScript 5\.8\.3 and gives type error**

*TSGO's UnionToTuple type generates tuples in reverse order compared to TypeScript 5.8.3, causing type errors*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3867505544) **jakebailey** said "In the 6.0 nightly, you can now also pass --stableTypeOrdering to try this sorting out early."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3872828964) **alexwork1611** thanked for the information about the --stableTypeOrdering flag
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3879428487) **RyanCavanaugh** clarified that UnionToTuple<'a'|'b'> currently yields consistent results but this behavior is unspecified and may change
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3912876412) **alexwork1611** appreciated the clarification from Ryan

