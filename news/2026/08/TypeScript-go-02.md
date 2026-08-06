# Report for 2026-08-02 (Sunday, August 2nd, 2026)

4 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @Mad-Kat asked if a sidecar model would be on the table and offered to prototype plugins in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5166713919)
    * @talkstream provided detailed memory leak growth data and environment information in [microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-5166782518)

## Activity Summary

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5108341014) **remcohaszing** asked whether any instances exist where a single non-TS file maps into multiple distinct files and noted that Volar supports this via the language server but not the TS plugin, mentioning HTML module scripts as an example and suggesting module declarations
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5108638364) **Princesseuh** clarified that Astro supports script tags of multiple languages within a file, works like HTML, and noted it was a blocker
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5109564324) **DanielRosenwasser** asked if resources or examples were available for multiple TS/JS blocks in an Astro file and what an importer received when handling them
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5166713919) **Mad-Kat** described migrating TS Server plugins and distribution challenges, contrasted current tsconfig-based integration with LSP-plus-editor extensions, and asked if a sidecar model would be on the table

### [Issue microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520) (Open, `Domain: Editor`)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*Enabling the TypeScript Native Preview extension in an empty folder without package.json causes a persistent memory leak until VS Code is closed.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4869534469) **KostyaTretyak** confirmed no memory leak when moving folder to a directory without other git repositories and suggested a service might misdetect neighboring repositories as part of the monorepo
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4952534039) **Skykill** reported that their three.js case reproduced with a minimal CLI setup, filed issue #4612 with repro steps and analysis, and suggested cross-linking due to a potential common underlying cause
 * **RyanCavanaugh** added to milestone `Need More Info`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-5166782518) **talkstream** provided an additional data point for the memory leak issue, including environment details and OS-level snapshot measurements showing a tsgo process growing from 163 MB to over 3 GB across five days

### [PR microsoft/TypeScript-go#4790](https://github.com/microsoft/TypeScript-go/pull/4790) (Closed)

**Skip stale overlay paths in markProjectsAffectedByConfigChanges**

*markProjectsAffectedByConfigChanges panics when stale overlay paths in affectedFiles cause nil pointer dereference*

 * created by **blixt**
 * (later) **blixt** closed the issue

### [Issue microsoft/TypeScript-go#4815](https://github.com/microsoft/TypeScript-go/issues/4815) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**\[API\] Expose globals declared by a source file**

*Expose SourceFile.Locals in the TypeScript JS API to more reliably retrieve global symbols declared in a source file.*

 * created by **Gerrit0**
 * (later) **RyanCavanaugh** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4818](https://github.com/microsoft/TypeScript-go/issues/4818) (Open, `Needs Investigation`, **gabritto**)

**internal/ls: getContextNodeForNodeEntry returns nil for module\-specifier literals \(stock returns the enclosing import statement\)**

*getContextNodeForNodeEntry returns nil for module-specifier literals in tsgo, unlike stock TypeScript which returns the enclosing import statement.*

 * created by **johnsoncodehk**

### [Issue microsoft/TypeScript-go#4819](https://github.com/microsoft/TypeScript-go/issues/4819) (Closed)

**tsgo never terminates on a single three\.js TSL method call \(works in 5\.9\.3 and 6\.0\.3\)**

*tsgo 7.x hangs indefinitely on a single three.js TSL vec3(...).mul(2) call, while TypeScript 5.9.3 and 6.0.3 complete quickly*

 * created by **alexcz-a11y**

