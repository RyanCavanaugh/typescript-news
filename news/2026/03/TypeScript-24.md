# Report for 2026-03-24 (Tuesday, March 24th, 2026)

18 different users commented on 531 different issues.

## Activity Summary

### [PR microsoft/TypeScript#26349](https://github.com/microsoft/TypeScript/pull/26349) (Closed, `Experiment`, `Fix Available`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Implement partial type argument inference using the \_ sigil**

*Allow using the underscore (_) sigil in TypeScript type argument lists to enable partial type inference.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/26349#issuecomment-1536633920) **weswigham** described consensus to include the change in version 5.2 and to improve error messages by suggesting use of '_' and adding specialized messaging for failed placeholder lookups
 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/26349#issuecomment-1536637769) **patroza** asked whether specifying A only would allow inference for B and C with sigil defaults
 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/26349#issuecomment-1536644350) **weswigham** noted that it did not respect sigil default and proposed shipping without it temporarily to assess the impact of the verbose syntax
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#35206](https://github.com/microsoft/TypeScript/pull/35206) (Closed, `Experiment`, `lib update`, `For Uncommitted Bug`)

**Native support for PnP**

*Add proof-of-concept native support for Yarn Plug’n’Play module resolution in TypeScript.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/pull/35206#issuecomment-2523265822) **adrian-gierakowski** requested a consolidated TS team update on the current status of the highly up-voted PR to improve clarity for passers by
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/35206#issuecomment-2603521919) **sundbry** said "Is anyone @microsoft paying attention? This PR is going on 6 years old"
 * [17 weeks ago](https://github.com/microsoft/TypeScript/pull/35206#issuecomment-3570057954) **arcanis** provided an update that a new PR implemented the full PnP specification in TypeScript-Go with technical blockers addressed, tests included, validation on Datadog completed, contributors thanked, and urged TS team collaboration
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/35206#issuecomment-4121422967) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#42104](https://github.com/microsoft/TypeScript/pull/42104) (Closed, `For Backlog Bug`, **weswigham**)

**allow unused private well\-known symbol members**

*Enable support for defining private members with well-known symbols in TypeScript even if they remain unused.*

 * **sandersn** unassigned **armanio123**
 * (3.9 years ago) **andrewbranch** assigned to **weswigham**, and unassigned **andrewbranch**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/42104#issuecomment-4121422949) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#43468](https://github.com/microsoft/TypeScript/pull/43468) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**Server commands from tsserver log file**

*Add CLI flags to tsserver to replay commands from a log and export or import request-only logs.*

 * (4.9 years ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript/pull/43468#issuecomment-4120886493) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#48092](https://github.com/microsoft/TypeScript/pull/48092) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Don't erase signature type parameters in signaturesRelatedTo**

*Ensure signaturesRelatedTo preserves signature type parameters rather than erasing them*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/48092#issuecomment-1714190620) **andrewbranch** said "@typescript-bot pack this"
 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/48092#issuecomment-1714190691) **typescript-bot** started running the tarball bundle task on the PR and shared the build monitoring link
 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/48092#issuecomment-1714194325) **typescript-bot** provided installation instructions, including an installable tgz link, package.json snippet, playground, and npm module links for testing the build
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/48092#issuecomment-4121423104) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#48228](https://github.com/microsoft/TypeScript/pull/48228) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**isArray\(\) preserve mutability and element type**

*Refine Array.isArray's type guard to preserve readonly/mutable status and element types for arrays, ArrayLike, and Iterable while maintaining any/unknown compatibility.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/48228#issuecomment-2249373802) **typescript-bot** reported new TS4104 errors in the effect package during user tests comparing main and pull request merge
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/48228#issuecomment-2249432973) **typescript-bot** provided the requested performance run results
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/48228#issuecomment-2249520768) **typescript-bot** reported the tsc regression results for top 400 repos, highlighting build failures in apollographql/apollo-client and discordjs/discord.js
 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`

### [PR microsoft/TypeScript#48388](https://github.com/microsoft/TypeScript/pull/48388) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Reuse type reference resolutions between programs when possible**

*Improve performance by reusing existing type reference resolutions across programs instead of always recalculating them*

 * (4 years ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/48388#issuecomment-4121423207) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#48433](https://github.com/microsoft/TypeScript/pull/48433) (Closed, `For Backlog Bug`, **weswigham**)

**bugfix: homomorphic mapped types when T is non\-generic, solves 27995**

*Fix homomorphic mapped tuple types resolution in the TypeScript compiler when T is a non-generic tuple, addressing issue #27995.*

 * **sandersn** assigned to **weswigham**
 * [3.9 years ago](https://github.com/microsoft/TypeScript/pull/48433#issuecomment-1091949969) **Andarist** said "Looking at the last comment here it also might fix the issue there"
 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/48433#issuecomment-1733268236) **Andarist** pushed out the requested changes and asked for feedback on whether the approach was worthwhile
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/48433#issuecomment-4121423301) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#48627](https://github.com/microsoft/TypeScript/pull/48627) (Closed, `For Backlog Bug`)

**fix\(48557\): Fix some JSDoc parameters \(source code, not lib for use\)**

*Improve JSDoc parameter comments and fix typos in TypeScript source’s cancellationToken and compiler modules*

 * created by **dev-itsheng**
 * **typescript-bot** added label `For Backlog Bug`
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/48627#issuecomment-4121423331) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#48838](https://github.com/microsoft/TypeScript/pull/48838) (Closed, `For Backlog Bug`, **weswigham**)

**Instantiate conditional types within contextual type instantiation when inference candidates are available**

*TypeScript should instantiate conditional types sooner during contextual type instantiation when inference candidates are available.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/pull/48838#issuecomment-1887899632) **typescript-bot** Provided additional TypeScript error details from the top-repos suite run
 * [2.1 years ago](https://github.com/microsoft/TypeScript/pull/48838#issuecomment-1887908173) **Andarist** said "Oh, that's not great for me 😅 I'll have to extract some test cases out of this to add as tests to the repo, and... gonna get back to the drawing board to figure out a different fix for this."
 * [46 weeks ago](https://github.com/microsoft/TypeScript/pull/48838#issuecomment-2843305943) **sandersn** said "@Andarist are you still working on this? Is it worth keeping this PR open?"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/48838#issuecomment-4121423453) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#49064](https://github.com/microsoft/TypeScript/pull/49064) (Closed, `For Backlog Bug`)

**Fixed an issue with a concrete object not being assignable to a generic mapped type with a partially concrete constraint**

*Resolved type-checking error where concrete objects could not satisfy generic mapped types with partially concrete constraints.*

 * (3.8 years ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/49064#issuecomment-4121423527) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#49107](https://github.com/microsoft/TypeScript/pull/49107) (Closed, `For Uncommitted Bug`, **weswigham**)

**Improve computed base constraint for Index type on generic IndexedAccess**

*Suggest improving TypeScript’s base constraint calculation for generic indexed access to accurately reflect allowable property keys.*

 * [3 years ago](https://github.com/microsoft/TypeScript/pull/49107#issuecomment-1439225257) **jakebailey** said "@typescript-bot pack this"
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/49107#issuecomment-1439225284) **typescript-bot** started the tarball bundle task on the PR and provided a link to monitor the build
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/49107#issuecomment-1439226335) **typescript-bot** provided an installable build tgz and instructions along with playground and npm module links for testing
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/49107#issuecomment-4121423604) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#49146](https://github.com/microsoft/TypeScript/pull/49146) (Closed, `For Backlog Bug`, **rbuckton**)

**Avoid binding readonly properties as special properties on a function symbol**

*Change the TypeScript compiler to avoid binding readonly properties as special properties on function symbols.*

 * [3.6 years ago](https://github.com/microsoft/TypeScript/pull/49146#issuecomment-1183712685) **Andarist** said "Do we have any consensus on how I should proceed here? What kind of a solution is preferred?"
 * [44 weeks ago](https://github.com/microsoft/TypeScript/pull/49146#issuecomment-2880382857) **sandersn** endorsed the proposed fix, explained why Ryan's solution fails, and asked Andarist whether to revive the proposal
 * [44 weeks ago](https://github.com/microsoft/TypeScript/pull/49146#issuecomment-2880843974) **Andarist** agreed to revive the work soon-ish and ping for re-review
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/49146#issuecomment-4121423669) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#49218](https://github.com/microsoft/TypeScript/pull/49218) (Closed, `For Backlog Bug`, **jakebailey**)

**Improve signature assignability for argument lists of different lengths**

*Enhance TypeScript's signature assignability to support functions with varying argument list lengths.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/pull/49218#issuecomment-2067252570) **typescript-bot** offered instructions for installing the build and provided links to the playground and npm module
 * [1.9 years ago](https://github.com/microsoft/TypeScript/pull/49218#issuecomment-2067273204) **typescript-bot** reported that testing of the top 400 repos comparing main and the pull request merge showed everything looked good
 * [46 weeks ago](https://github.com/microsoft/TypeScript/pull/49218#issuecomment-2842907576) **sandersn** said "This has been sitting for a while with changes requested. @Andarist do you want to keep working on it?"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/49218#issuecomment-4121423755) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#49245](https://github.com/microsoft/TypeScript/pull/49245) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Invert check for for\-in and handle generic constraints**

*Invert the for-in primitive check to better support generic constraints and improve the corresponding error message.*

 * [3.8 years ago](https://github.com/microsoft/TypeScript/pull/49245#issuecomment-1137696669) **typescript-bot** provided testing instructions with an installable tgz, playground link, and npm module reference
 * [3.8 years ago](https://github.com/microsoft/TypeScript/pull/49245#issuecomment-1137707574) **typescript-bot** posted the perf run results requested by @weswigham
 * [3.8 years ago](https://github.com/microsoft/TypeScript/pull/49245#issuecomment-1137836000) **weswigham** said "Extended test suites all seem good 💖"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/49245#issuecomment-4121423797) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#49817](https://github.com/microsoft/TypeScript/pull/49817) (Closed, `Breaking Change`, `Author: Team`, `For Uncommitted Bug`, `Rescheduled`, **weswigham**)

**Always look for tsconfig, allow command line to override tsconfig file list**

*tsc automatically uses tsconfig.json if present and allows command-line options and filenames to override tsconfig settings and included files.*

 * (2 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.5.5`, and removed from milestone `TypeScript 5.5.0`
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/49817#issuecomment-4121423873) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#49886](https://github.com/microsoft/TypeScript/pull/49886) (Closed, `Experiment`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Allow some per file compiler options**

*Enable per-file configuration of select strict type-checking options via `// @ts-option` comments in TypeScript files.*

 * **weswigham** added label `Experiment`
 * [46 weeks ago](https://github.com/microsoft/TypeScript/pull/49886#issuecomment-2843258458) **sandersn** said "@weswigham is this worth keeping open? Is it worth revisiting in Go?"
 * [43 weeks ago](https://github.com/microsoft/TypeScript/pull/49886#issuecomment-2902955727) **dwm-mcollins** suggested adding an opt-in strictness directive per file, recommended using a hashmap to cache strictness settings for performance, and highlighted challenges migrating large projects to strictNullChecks
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/49886#issuecomment-4121423922) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#50046](https://github.com/microsoft/TypeScript/pull/50046) (Closed, `For Milestone Bug`, **DanielRosenwasser**)

**Better Inference for mapped array and tuple types**

*Modify the TypeScript checker to better infer mapped array and tuple types by mapping only elements and discarding non-array properties.*

 * created by **graphemecluster**
 * (3.6 years ago) **typescript-bot** added label `For Milestone Bug`, and assigned to **DanielRosenwasser**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/50046#issuecomment-4121424007) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#50310](https://github.com/microsoft/TypeScript/pull/50310) (Closed, `Experiment`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Wrap native map to work around 2\*\*24 element limit**

*Wrap the native map to avoid crashes beyond the 2^24 element limit, causing extra comparisons and reduced performance.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/50310#issuecomment-1221057003) **typescript-bot** reported the requested performance run results comparing main and 50310 metrics
 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/50310#issuecomment-1221101090) **weswigham** added a diagnostic for source elements triggering over 1 million comparisons and explained the rationale behind the threshold and union size caps
 * **weswigham** added label `Experiment`
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/50310#issuecomment-4121424077) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#50329](https://github.com/microsoft/TypeScript/pull/50329) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Optimize comparing intersections with common members**

*Optimize TypeScript’s intersection comparison by stripping common members before normalization to reduce exhaustive union checks and improve compilation speed.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/50329#issuecomment-1738656180) **typescript-bot** posted the requested performance run results
 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/50329#issuecomment-1738842393) **typescript-bot** shared results of running the top-repos suite and reported that everything looked good
 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/50329#issuecomment-1739301887) **ahejlsberg** suggested examining origin properties of unions in intersections to optimize removal of redundant types
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/50329#issuecomment-4121424134) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#50451](https://github.com/microsoft/TypeScript/pull/50451) (Closed, `For Backlog Bug`, **sandersn**)

**lib Fix Part 3/6 – Object related methods**

*Refactor object constructor methods to require {}-typed first parameters per ECMAScript spec, fixing related type errors.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/50451#issuecomment-1246130509) **typescript-bot** reported top-repos suite results comparing main and PR merge, noted interesting changes, and listed build failures for conwnet/github1s and microsoft/vscode projects
 * [3.3 years ago](https://github.com/microsoft/TypeScript/pull/50451#issuecomment-1308101092) **graphemecluster** said "Great, TypeScript bug discovered! (Temporarily fixed with a non-null assertion)"
 * [1.8 years ago](https://github.com/microsoft/TypeScript/pull/50451#issuecomment-2107947437) **wchargin** requested revisiting the stalled PR for Object.hasOwn and suggested splitting noncontroversial changes into a separate PR
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/50451#issuecomment-4121424234) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#50452](https://github.com/microsoft/TypeScript/pull/50452) (Open, `For Backlog Bug`, **navya9singh**)

**lib Fix Part 4/6 – String\.replaceAll and related changes**

*Add String.replaceAll type definitions and update related library documentation in the fourth part of six lib fixes.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/50452#issuecomment-1246059389) **typescript-bot** notified that the diff-based user code test suite had started on the PR and provided links to monitor the build and view the results
 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/50452#issuecomment-1246074063) **typescript-bot** reported that running the user test suite comparing main and the pull request merge returned no issues
 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/50452#issuecomment-1246115902) **typescript-bot** reported results of the top-repos suite comparing main and the PR merge and identified build failures in microsoft/vscode due to TS2345 type errors
 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`

### [PR microsoft/TypeScript#50494](https://github.com/microsoft/TypeScript/pull/50494) (Closed, `For Backlog Bug`, **weswigham**)

**add \`undefined\` to declaration of constructor parameter property with…**

*Include undefined in the type declaration of constructor parameter properties when a default value is provided.*

 * created by **Zzzen**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **weswigham**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/50494#issuecomment-4121424277) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#50775](https://github.com/microsoft/TypeScript/pull/50775) (Closed, `For Backlog Bug`, **sheetalkamat**)

**Handle ambient namespace aliasing in getContainersOfSymbol**

*Ensure getContainersOfSymbol handles ambient namespace aliases so exported types use correct alias names.*

 * [3 years ago](https://github.com/microsoft/TypeScript/pull/50775#issuecomment-1464188845) **typescript-bot** started to run the perf test suite on the PR and provided build and results links
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/50775#issuecomment-1464522105) **typescript-bot** reported the performance run results
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/50775#issuecomment-1464582694) **jakebailey** said "There we go, that seems much more reasonable."
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/50775#issuecomment-4121424376) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#50777](https://github.com/microsoft/TypeScript/pull/50777) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Adjust constraint caluclation for T\[U\]**

*Modify constraint calculation for T[U] to return all properties of T assignable to U instead of only exact matches.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/50777#issuecomment-1247312034) **typescript-bot** provided installable tgz link and instructions for testing the 4.9.0-insiders build, plus playground and npm module links
 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/50777#issuecomment-1249909857) **weswigham** said "@typescript-bot perf test this faster"
 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/50777#issuecomment-1249909866) **typescript-bot** notified that the abridged perf test suite was started on this PR and shared a monitoring link
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/50777#issuecomment-4121424450) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#50782](https://github.com/microsoft/TypeScript/pull/50782) (Closed, `Author: Team`, `For Uncommitted Bug`, **amcasey**)

**Corner case: FAR triggers project load, invalidating results already computed for inferred project**

*Finding all references triggers a project load that invalidates inferred project results; checking the program state instead resolves the flaw.*

 * (3.5 years ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`
 * [51 weeks ago](https://github.com/microsoft/TypeScript/pull/50782#issuecomment-2767467747) **sandersn** said "@sheetalkamat Thiis is very old now. Is it worth working on further?"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/50782#issuecomment-4121424568) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#51386](https://github.com/microsoft/TypeScript/pull/51386) (Closed, `For Backlog Bug`, **sandersn**)

**fix JSDoc http links with custom display text**

*Add support for custom display text for HTTP links in JSDoc comments.*

 * created by **matiasosorio1999**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **sandersn**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/51386#issuecomment-4121424672) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#51695](https://github.com/microsoft/TypeScript/pull/51695) (Closed, `For Backlog Bug`, **ahejlsberg**)

**Filter signatures by matching constraints when instantiating them for instantiation signatures**

*Filter type signatures by matching constraints during instantiation to resolve TypeScript type-checking errors.*

 * [3.2 years ago](https://github.com/microsoft/TypeScript/pull/51695#issuecomment-1360073389) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #51694. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [3.2 years ago](https://github.com/microsoft/TypeScript/pull/51695#issuecomment-1360073411) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #51694. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [3.2 years ago](https://github.com/microsoft/TypeScript/pull/51695#issuecomment-1360073416) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #51694. If you can get it accepted, this PR will have a better chance of being reviewed."
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/51695#issuecomment-4121424761) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52112](https://github.com/microsoft/TypeScript/pull/52112) (Closed, `For Backlog Bug`, **ahejlsberg**)

**Apply \(Un\)Capitalize template string mappings on generic template literal types in a safe manner**

*Enable safe application of Capitalize and Uncapitalize operations to generic template literal types in TypeScript.*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/52112#issuecomment-1611827877) **jakebailey** said "@typescript-bot run dt"
 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/52112#issuecomment-1611827926) **typescript-bot** started the parallelized Definitely Typed test suite on the PR and provided build and results links
 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/52112#issuecomment-1611997172) **typescript-bot** notified that the DT test results were ready and unchanged and provided a link to the log
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52112#issuecomment-4121424862) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52244](https://github.com/microsoft/TypeScript/pull/52244) (Closed, `For Backlog Bug`, **DanielRosenwasser**)

**fix completion text of exported types**

*Adds logic to use an export symbol’s flags when computing the declared type of an exported type to fix completion text.*

 * [3.1 years ago](https://github.com/microsoft/TypeScript/pull/52244#issuecomment-1401246797) **typescript-bot** reported that the top-repos suite results looked good comparing main and the PR merge
 * [3.1 years ago](https://github.com/microsoft/TypeScript/pull/52244#issuecomment-1402230246) **Tobias-Scholz** noted changes to symbol display parts for namespaces and interfaces and reported eight failing tests after committing the change
 * **sandersn** assigned to **DanielRosenwasser**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52244#issuecomment-4121424980) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52355](https://github.com/microsoft/TypeScript/pull/52355) (Closed, `For Backlog Bug`)

**Source map with single source: Stop generating empty mappings\.**

*Automatically generate a default mapping for single-source output files to prevent empty source map entries.*

 * [3.1 years ago](https://github.com/microsoft/TypeScript/pull/52355#issuecomment-1399507003) **microsoft-github-policy-service[bot]** requested CLA agreement confirmation from the contributor
 * **typescript-bot** added label `For Backlog Bug`
 * [3.1 years ago](https://github.com/microsoft/TypeScript/pull/52355#issuecomment-1399508783) **pguilbert** said "@microsoft-github-policy-service agree"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52355#issuecomment-4121425020) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52372](https://github.com/microsoft/TypeScript/pull/52372) (Closed, `Author: Team`, `For Milestone Bug`, **navya9singh**)

**Fix\(51162\): TS Server fatal error**

*Skip invalid characters in '{|' and '<T: null | void>' contexts to prevent parser misinterpretation and TS server crashes.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/52372#issuecomment-1541175814) **typescript-bot** reported results of running the top-repos suite comparing main and the merge branch and stated everything looked good
 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/52372#issuecomment-1541289587) **typescript-bot** reported results of running the top-repos suite comparing main and the merge branch and stated everything looked good
 * [45 weeks ago](https://github.com/microsoft/TypeScript/pull/52372#issuecomment-2877574767) **sandersn** said "@navya9singh from reading the PR, it looks it's good enough to merge except that it needs a smaller repro. Does that sound correct? Is it worthwhile to do that so we can take the fix?"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52372#issuecomment-4121425120) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52483](https://github.com/microsoft/TypeScript/pull/52483) (Closed, `For Backlog Bug`, **sheetalkamat**)

**Allow nonNullAssertions on possibly\-uninitialized auto\-typed let variables**

*Allow non-null assertion operator (!) usage on auto-typed let variables considered potentially uninitialized.*

 * [3.1 years ago](https://github.com/microsoft/TypeScript/pull/52483#issuecomment-1407525836) **Tobias-Scholz** said "@microsoft-github-policy-service agree"
 * **sandersn** assigned to **sheetalkamat**
 * [46 weeks ago](https://github.com/microsoft/TypeScript/pull/52483#issuecomment-2848108762) **sandersn** said "This has been sitting for a couple of years. @Tobias-Scholz unless you want to start working on it again, I'd like to close it for housekeeping."
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52483#issuecomment-4121425204) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52495](https://github.com/microsoft/TypeScript/pull/52495) (Closed, `For Backlog Bug`, **ahejlsberg**)

**Fixed generic inference when the contextual type is a signature with properties**

*Fix generic type inference for contextual types based on function signatures with properties*

 * [3 years ago](https://github.com/microsoft/TypeScript/pull/52495#issuecomment-1480100959) **jakebailey** said "Just rechecking; could be that the diff is due to some bad baseline behavior I'm working on fixing as part of the perf overhaul."
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/52495#issuecomment-1480120011) **typescript-bot** reported the results of the requested perf run comparing main and 52495 metrics
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/52495#issuecomment-1480121168) **jakebailey** reported that it was still a performance hit and observed that the xstate test ran for only three seconds
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52495#issuecomment-4121425249) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52646](https://github.com/microsoft/TypeScript/pull/52646) (Closed, `Author: Team`, `For Milestone Bug`, **navya9singh**)

**Fix\(50751\): Undefined entity with immediate and prototype expression causing crash**

*Using an undefined entity within an immediate and prototype expression causes the TypeScript compiler to crash.*

 * [3.1 years ago](https://github.com/microsoft/TypeScript/pull/52646#issuecomment-1421385189) **typescript-bot** posted the requested perf run results
 * [3.1 years ago](https://github.com/microsoft/TypeScript/pull/52646#issuecomment-1421416207) **typescript-bot** provided results of running the top-repos suite comparing main and the pull request merge and noted an interesting change
 * [3.1 years ago](https://github.com/microsoft/TypeScript/pull/52646#issuecomment-1421445020) **typescript-bot** reported that the top-repos suite comparison between main and refs/pull/52646/merge succeeded
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52646#issuecomment-4121425302) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52737](https://github.com/microsoft/TypeScript/pull/52737) (Closed, `For Backlog Bug`, **weswigham**)

**Infer types from mapped properties other than the mapped type itself**

*Enable TypeScript to infer types for mapped types from their properties instead of only from the mapped type itself.*

 * [3 years ago](https://github.com/microsoft/TypeScript/pull/52737#issuecomment-1457129252) **gabritto** pointed out that the PR broke inference for the 'righto' package on DT and asked to investigate if it can be fixed
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/52737#issuecomment-1457221986) **Andarist** identified the need to refine inference logic for tuples/arrays and stated intent to investigate the codebase
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/52737#issuecomment-1457438096) **typescript-bot** provided the requested performance run results
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52737#issuecomment-4121425371) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [Issue microsoft/TypeScript#52791](https://github.com/microsoft/TypeScript/issues/52791) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow use of \`infer\` in the type parameter of a type declaration**

*Allow using infer directly in type parameter constraints to eliminate redundant conditional types and improve readability*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/52791#issuecomment-1594761338) **fatcerberus** noted that implementing this might change behavior because TypeScript currently does not infer type variables from constraints
 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/52791#issuecomment-3145185743) **T99** described a simpler method for extracting generic types in TypeScript using parameter constraints to avoid impossible `never` branches and cleaner generated types
 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/52791#issuecomment-3145216956) **RyanCavanaugh** suggested an alternative method to extract a generic type using indexed access on a class property
 * [today](https://github.com/microsoft/TypeScript/issues/52791#issuecomment-4122018017) **zhangyx1998** described another relevant case with working TypeScript code and noted a simpler preferred version

### [PR microsoft/TypeScript#52850](https://github.com/microsoft/TypeScript/pull/52850) (Closed, `For Backlog Bug`, **iisaduan**)

**Report elementwise elaborations on spreads too**

*Enable elementwise elaborations to be reported on spread expressions as well.*

 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **iisaduan**
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/52850#issuecomment-2227800935) **Andarist** said "@weswigham friendly 🏓 "
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52850#issuecomment-4121425427) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52866](https://github.com/microsoft/TypeScript/pull/52866) (Closed, `For Backlog Bug`, **weswigham**)

**Get apparent type for calls used directly at argument positions to aid nested inferences**

*Retrieve apparent types of call expressions used directly as arguments to improve nested type inference in TypeScript*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/52866#issuecomment-1577019099) **Andarist** explained that the discriminated contextual type check and isCallOrNewExpression guard were necessary, noted the lack of a test for this part, and showed baseline failures when using the simpler instantiation approach
 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/52866#issuecomment-1578298692) **Andarist** debugged VS Code's codebase to identify unsoundness in break handling and suggested determining the correct fix based on outer contextualType or returnMapper
 * [1.9 years ago](https://github.com/microsoft/TypeScript/pull/52866#issuecomment-2025473674) **fabian-hiller** said "Would love to see this merged to fix #57978"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52866#issuecomment-4121425468) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52944](https://github.com/microsoft/TypeScript/pull/52944) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Improve overload and generic signature inference: Inference alternatives and linked inferences**

*Improve overload and generic signature inference by choosing matches from overload lists and preserving generics to link inferences.*

 * [3 years ago](https://github.com/microsoft/TypeScript/pull/52944#issuecomment-1454244043) **gabritto** said "@typescript-bot run DT"
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/52944#issuecomment-1454244088) **typescript-bot** notified that the parallelized Definitely Typed test suite started running on the PR at commit 4b8b0a5e36b68bc25971ec6249a0084678602007 and provided links to monitor and view the results
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/52944#issuecomment-1454306691) **typescript-bot** reported DT test results and compile errors in express-paginate, ember__array, and openpgp
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52944#issuecomment-4121425573) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52972](https://github.com/microsoft/TypeScript/pull/52972) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Infer from filtering mapped types**

*Implements partial support for inferring types from filtering mapped types as requested in TypeScript issue 46602.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/52972#issuecomment-2502401858) **jakebailey** said "@typescript-bot pack this"
 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/52972#issuecomment-2502402005) **typescript-bot** announced that CI jobs had started and provided status and results links
 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/52972#issuecomment-2502407265) **typescript-bot** informed jakebailey how to install the TypeScript 5.8.0 insiders build via tgz or npm module for testing
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52972#issuecomment-4121425597) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52979](https://github.com/microsoft/TypeScript/pull/52979) (Closed, `For Backlog Bug`, **navya9singh**)

**Move to new file: handle later exports in old file**

*Exclude later-exported symbols from movedSymbols when relocating declarations to a new file to ensure accurate import adjustments.*

 * (3 years ago) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * **sandersn** assigned to **navya9singh**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52979#issuecomment-4121425636) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#52990](https://github.com/microsoft/TypeScript/pull/52990) (Closed, `For Backlog Bug`, **navya9singh**)

**\[Move to new file\] Update named re\-exports in other files**

*Centralize import and re-export filtering in filterImportOrReexport to update named re-exports after moving a file.*

 * created by **zardoy**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **navya9singh**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/52990#issuecomment-4121425693) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53017](https://github.com/microsoft/TypeScript/pull/53017) (Closed, `For Backlog Bug`, **ahejlsberg**)

**Infer type parameters from indexes on those parameters**

*Infer generic type parameters in TypeScript based on index accesses of those parameters.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3603416171) **typescript-bot** provided performance run results for the requested perf tests
 * [15 weeks ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3603562038) **typescript-bot** reported that running the top 400 repos with tsc on main versus the pull request produced no issues
 * [15 weeks ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3616509136) **Andarist** stated that the webpack break was acceptable and linked to a detailed write-up
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-4121425784) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53042](https://github.com/microsoft/TypeScript/pull/53042) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Fixed contextual types within generic tuple mapped types**

*Add a test case demonstrating correct contextual type inference within generic tuple mapped types.*

 * [3 years ago](https://github.com/microsoft/TypeScript/pull/53042#issuecomment-1462525109) **sandersn** said "This is the comment where you describe the bug, right?"
 * **sandersn** assigned to **ahejlsberg**
 * [3 years ago](https://github.com/microsoft/TypeScript/pull/53042#issuecomment-1462540110) **Andarist** said "Yep, it mentions this and related things"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53042#issuecomment-4121425875) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53203](https://github.com/microsoft/TypeScript/pull/53203) (Closed, `For Backlog Bug`, **navya9singh**)

**Creating new file from existing nodes should preserve newlines**

*Creating new files from existing code nodes should preserve original newlines and formatting*

 * created by **zardoy**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **navya9singh**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53203#issuecomment-4121425896) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53595](https://github.com/microsoft/TypeScript/pull/53595) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Cutoff reverse mapped type recursion**

*Cut off recursion in reverse mapped types to fix mapping errors and measure performance impact.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53595#issuecomment-1491094617) **weswigham** said "@typescript-bot run dt"
 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53595#issuecomment-1491094658) **typescript-bot** notified about the parallelized Definitely Typed test run on the PR and provided build and results links
 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53595#issuecomment-1491167901) **typescript-bot** notified that DT test results were ready and reported branch-only errors in convict package tests
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53595#issuecomment-4121425944) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53615](https://github.com/microsoft/TypeScript/pull/53615) (Closed, `For Backlog Bug`, **ahejlsberg**)

**Fixed an issue with spreading generic types with tuple constraints into calls**

*Restored correct behavior for spreading generic tuple-constrained types into function calls*

 * created by **Andarist**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **ahejlsberg**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53615#issuecomment-4121425999) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53618](https://github.com/microsoft/TypeScript/pull/53618) (Closed, `For Backlog Bug`, **jakebailey**)

**Supported data URLs in core paths utilities**

*Add regex-based detection of data URLs to core path utilities and explicit handling in ensureTrailingDirectorySeparator.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/53618#issuecomment-1811476738) **jakebailey** asked whether the helper is used externally or if TS internals need to handle this differently, and noted incomplete internal URI usage
 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/53618#issuecomment-1811494847) **dsherret** recalled that the issue was internal and hacked a fix in the bundled TypeScript, and mentioned that Deno used URLs with a hacky mapping layer to accommodate ts.normalizePath
 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/53618#issuecomment-1828480834) **jakebailey** said "@sheetalkamat Do you have any concerns about this one?"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53618#issuecomment-4121426061) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53631](https://github.com/microsoft/TypeScript/pull/53631) (Closed, `For Backlog Bug`, **sandersn**)

**fix\(53576\): Don't remove indentations from JSDoc tag documentation**

*Retain original indentation in JSDoc tags by preventing automatic removal of leading whitespace.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53631#issuecomment-1507795852) **typescript-bot** posted the performance run results comparing main to 53631
 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/53631#issuecomment-1751800082) **jespertheend** said "@sandersn Are the perf results ok? An increase of 1% in some of these sounds like a lot. Is there anything I should change?"
 * [46 weeks ago](https://github.com/microsoft/TypeScript/pull/53631#issuecomment-2842937032) **sandersn** suggested dropping the offside-style indentation rules entirely to simplify the PR and remove code
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53631#issuecomment-4121426141) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53700](https://github.com/microsoft/TypeScript/pull/53700) (Closed, `For Backlog Bug`, **sheetalkamat**)

**Fix incompact with frozen\-intrinsics \(\#53699\)**

*Adjust the incompact algorithm to correctly handle frozen-intrinsics and avoid related build errors.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53700#issuecomment-1515072041) **rbuckton** said "@typescript-bot perf test"
 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53700#issuecomment-1515072130) **typescript-bot** started to run the perf test suite on the PR and linked to the build and results
 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53700#issuecomment-1515144380) **typescript-bot** reported the results of the requested perf run including compiler memory, parse, bind, and check time metrics
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53700#issuecomment-4121426213) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53739](https://github.com/microsoft/TypeScript/pull/53739) (Closed, `For Backlog Bug`, **weswigham**)

**Attempt to reduce types which are about to produce a complexity error**

*Syncs with main and enhances type reduction by deferring union and intersection member construction to avoid complexity errors*

 * **sandersn** added label `For Backlog Bug`
 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/53739#issuecomment-1732106033) **sandersn** said "@weswigham Is this ready to go? I don't know whether you want to double check xstate results first or not."
 * [46 weeks ago](https://github.com/microsoft/TypeScript/pull/53739#issuecomment-2845089108) **sandersn** said "It's been a couple of years since this was finished. Is it a draft now because there's some new problem that we discovered? Or are we just waiting on Corsa work to be done?"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53739#issuecomment-4121426371) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53758](https://github.com/microsoft/TypeScript/pull/53758) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Preserve generic substitutions through instantiation more often**

*Preserve substitution type information during type variable instantiation in conditional types to retain inference context.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53758#issuecomment-1505823451) **typescript-bot** provided the requested performance run results for main..53758
 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53758#issuecomment-1505881198) **typescript-bot** notified that the DT test results were ready and unchanged
 * [2.9 years ago](https://github.com/microsoft/TypeScript/pull/53758#issuecomment-1505887274) **typescript-bot** reported top-repos suite results comparing main and the pull request merge and confirmed everything looked good
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53758#issuecomment-4121426380) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#53772](https://github.com/microsoft/TypeScript/pull/53772) (Closed, `For Backlog Bug`, **rbuckton**)

**Fix 50305**

*Include method parameter decorators in visitPropertyNameOfClassElement’s decorator check to correct computed property name hoisting inconsistency.*

 * **sandersn** assigned to **rbuckton**
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/53772#issuecomment-2257207676) **jakebailey** said "FWIW I tried this with nodeOrChildIsDecorated(legacyDecorators, member, member.parent) and I didn't find the output too unreasonable..."
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/53772#issuecomment-2276309207) **rbuckton** clarified that the call needed to use parent instead of member.parent and that parent must be passed to visitPropertyNameOfClassElement
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/53772#issuecomment-4121426515) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54006](https://github.com/microsoft/TypeScript/pull/54006) (Closed, `For Uncommitted Bug`, **weswigham**)

**Deprioritize inferences made from implicit never arrays**

*Adjust TypeScript's type inference logic to deprioritize inferences derived from arrays implicitly typed as never.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/54006#issuecomment-1800430778) **weswigham** suggested deprioritizing implicitNeverType inferences below mapped type ones by introducing a new InferencePriority
 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/54006#issuecomment-1807266792) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/54006#issuecomment-1807281196) **Andarist** pushed the requested changes and clarified the issue was about implicitNeverType[] rather than implicitNeverType, removing an earlier check after failing to use implicitNeverType as an inference source
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54006#issuecomment-4121411725) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54029](https://github.com/microsoft/TypeScript/pull/54029) (Closed, `For Backlog Bug`, **ahejlsberg**)

**Improve inference for context sensitive functions within reverse mapped types**

*Enhance TypeScript’s inference algorithm to better handle context-sensitive functions within reverse mapped types.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591701794) **typescript-bot** posted the results of the requested perf run for tsc showing comparison metrics
 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591725156) **typescript-bot** reported test results and noted a git clone failure, otherwise everything looked good
 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591736549) **typescript-bot** ran tsc on the top 400 repositories comparing main and refs/pull/54029/merge and reported everything looked good
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-4121426711) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54047](https://github.com/microsoft/TypeScript/pull/54047) (Closed, `Experiment`, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Perform partial inference with partially filled type parameter lists**

*Allow partially specified type parameter lists by inferring omitted type arguments from expressions.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/54047#issuecomment-1533799199) **weswigham** said "#26349 is once again up to date with main, since that approach doesn't break the world and is much more familiar to users of Flow, F#, and Rust."
 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/54047#issuecomment-1533812583) **Andarist** said "@weswigham since partial inference by default seems to be to be off the table - do you envision any way for library authors to opt-into that in the future in their signature declarations?"
 * **weswigham** added label `Experiment`
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54047#issuecomment-4121426807) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54096](https://github.com/microsoft/TypeScript/pull/54096) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**Add a failing test case with \`types: null\` condition**

*Add a failing test case for scenarios where `types` is null to address a related TypeScript bug*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/54096#issuecomment-1570591911) **andrewbranch** discussed that 'types: null' semantics are unintuitive and clarified that null should stop resolution but there is no existing mechanism to abort resolution with a failure
 * [1.2 years ago](https://github.com/microsoft/TypeScript/pull/54096#issuecomment-2530058664) **jaridmargolin** asked if a new issue should be created for a similar problem hiding modules with a custom browser condition
 * [1.2 years ago](https://github.com/microsoft/TypeScript/pull/54096#issuecomment-2532148471) **andrewbranch** said "Planning to fix this as a breaking change in 6.0 or 6.5, depending on whether it needs a deprecation message; I’m not sure we have the details settled."
 * (today) **andrewbranch** closed the issue
 * (today) **andrewbranch** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54096#issuecomment-4121979385) **andrewbranch** explained that the change would fail CI due to improved behavior introduced in a previous PR

### [PR microsoft/TypeScript#54110](https://github.com/microsoft/TypeScript/pull/54110) (Closed, `For Backlog Bug`, **iisaduan**)

**fix issue 53775, do not always narrow to property signature**

*Add an emit-stage transformation to split accessor symbols with mismatched getter and setter types into separate PropertySignatures.*

 * [45 weeks ago](https://github.com/microsoft/TypeScript/pull/54110#issuecomment-2878086453) **sandersn** said "@Solo-steven I know it's been about 2 years, but do you want to finish this? It seems like a useful fix. Otherwise I'll close it for housekeeping purposes."
 * [44 weeks ago](https://github.com/microsoft/TypeScript/pull/54110#issuecomment-2894840788) **Steven19Lee** said "Hi @sandersn, yes, I forgot this PR I would like to restart it, but I might need a couple of weeks to recatch the context. Is ok for you?"
 * [44 weeks ago](https://github.com/microsoft/TypeScript/pull/54110#issuecomment-2895507389) **iisaduan** said "@Solo-steven That is fine with us!"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54110#issuecomment-4121426972) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54117](https://github.com/microsoft/TypeScript/pull/54117) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Replace errorType return with Debug fail in checkExpressionWorker**

*Replace errorType return with Debug.fail in checkExpressionWorker as recommended in the Pull Request discussion*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/54117#issuecomment-1533806665) **typescript-bot** notified that DT test results were ready and unchanged and provided a link to the log
 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/54117#issuecomment-1533832119) **typescript-bot** reported that the top-repos test suite results comparing main and the pull request merge looked good
 * [45 weeks ago](https://github.com/microsoft/TypeScript/pull/54117#issuecomment-2877560509) **sandersn** said "@weswigham This looks like a strict improvement to me. Is there a reason not to merge this?"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54117#issuecomment-4121427012) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54183](https://github.com/microsoft/TypeScript/pull/54183) (Closed, `For Backlog Bug`, **ahejlsberg**)

**Add nested call and new expressions as potential intra expression inference sites**

*Use nested call and new expressions as intra-expression inference sites to ensure nested generics resolve correctly.*

 * [44 weeks ago](https://github.com/microsoft/TypeScript/pull/54183#issuecomment-2891575486) **typescript-bot** announced that build jobs started and provided links to status and results
 * [44 weeks ago](https://github.com/microsoft/TypeScript/pull/54183#issuecomment-2891588121) **typescript-bot** provided an installable tgz and installation instructions for testing and included playground and npm module links
 * [44 weeks ago](https://github.com/microsoft/TypeScript/pull/54183#issuecomment-2891640265) **TkDodo** said "Thank you @jakebailey ❤️ . @Andarist just confirmed that this PR fixes the issue, which is great news 🎉  "
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54183#issuecomment-4121427165) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54290](https://github.com/microsoft/TypeScript/pull/54290) (Closed, `For Backlog Bug`, **ahejlsberg**)

**Check the provided type argument with this argument against the similarly obtained instantiated constraint**

*Improve compiler performance by bypassing the getVariancesWorker call when a type argument's ID matches its instantiated constraint*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/54290#issuecomment-1551797080) **typescript-bot** notified that it ran the abridged perf test suite on the PR and shared build and results links
 * [2.8 years ago](https://github.com/microsoft/TypeScript/pull/54290#issuecomment-1551815777) **typescript-bot** provided the performance comparison report for main vs 54290, showing memory usage, parse time, bind time, and check time
 * **sandersn** assigned to **ahejlsberg**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54290#issuecomment-4121427310) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54513](https://github.com/microsoft/TypeScript/pull/54513) (Closed, `For Backlog Bug`, **iisaduan**)

**Fix destructuring error with nested objects**

*Adjust nested object destructuring logic to fix errors when unpacking nested object properties.*

 * created by **Zzzen**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **iisaduan**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54513#issuecomment-4121427349) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54553](https://github.com/microsoft/TypeScript/pull/54553) (Closed, `For Uncommitted Bug`, **gabritto**)

**Contextually type the right operand of logical or & nullish coalescing using non\-nullable left type**

*Contextually type the right operand of logical OR and nullish coalescing expressions using the non-nullable type of the left operand*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/54553#issuecomment-1599375505) **typescript-bot** reported test suite results comparing main and the pull request merge, noted infrastructure failures and a new TS2428 error in rxjs-src
 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/54553#issuecomment-1599459535) **typescript-bot** reported that comparing main and the PR merge with the top-repos suite succeeded with no issues
 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/54553#issuecomment-1599484244) **typescript-bot** notified that DT test results were ready and unchanged
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54553#issuecomment-4121427466) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54688](https://github.com/microsoft/TypeScript/pull/54688) (Closed, `For Backlog Bug`, **sandersn**)

**fix\(53589\): Allow newlines before extend in conditional types**

*Allow newlines before extends in conditional types by updating the parser to differentiate object type extends.*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/54688#issuecomment-1599386143) **typescript-bot** notified that DT test results were ready and unchanged
 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/54688#issuecomment-1599461477) **typescript-bot** reported that the top-repos suite results comparing main and pull request merge looked good
 * **sandersn** assigned to **sandersn**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54688#issuecomment-4121427518) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54698](https://github.com/microsoft/TypeScript/pull/54698) (Closed, `For Backlog Bug`, **ahejlsberg**)

**Remove inference mode check in \`getNarrowableTypeForrReference\`**

*Removing the inference mode check in getNarrowableTypeForReference to allow narrowing of generic return types during inference.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/pull/54698#issuecomment-1899299516) **typescript-bot** reported DT tests results with errors in the ramda package
 * [2.1 years ago](https://github.com/microsoft/TypeScript/pull/54698#issuecomment-1899304036) **jakebailey** said "Quick link to the above failure: https://github.com/DefinitelyTyped/DefinitelyTyped/blob/master/types/ramda/test/tryCatch-tests.ts#L75-L76"
 * [2.1 years ago](https://github.com/microsoft/TypeScript/pull/54698#issuecomment-1899318539) **typescript-bot** provided results of the top-repos suite comparing main and PR merge, highlighting build failures in chakra-ui
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54698#issuecomment-4121427606) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54706](https://github.com/microsoft/TypeScript/pull/54706) (Closed, `Breaking Change`, `For Uncommitted Bug`, **weswigham**)

**Do not widen computed properties with template literal types**

*Propose changes to avoid widening computed properties with template literal types and seek guidance on reviving the unmerged PR.*

 * **sandersn** assigned to **weswigham**
 * **weswigham** added label `Breaking Change`
 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/54706#issuecomment-1806861950) **Andarist** said "@weswigham if I understand correctly the only requested change here was to add a generic test case and I've just pushed out one. Could you take another look?"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54706#issuecomment-4121427688) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54718](https://github.com/microsoft/TypeScript/pull/54718) (Closed, `For Backlog Bug`, **RyanCavanaugh**)

**Remove missing type from tuple type arguments under \`exactOptionalPropertyTypes\`**

*With exactOptionalPropertyTypes enabled, omit the missing type from tuple type arguments.*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/54718#issuecomment-1704044174) **Andarist** said "I managed to clean some things further. Personally, I like the changes - some bits feel simpler to me now. Let me know what do you think. "
 * (2.3 years ago) **weswigham** assigned to **RyanCavanaugh**, and unassigned **weswigham**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54718#issuecomment-4121427728) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54739](https://github.com/microsoft/TypeScript/pull/54739) (Closed, `For Backlog Bug`, **iisaduan**)

**Add support for JSX components with conditional types**

*Support JSX components that leverage conditional types for their props in TypeScript.*

 * **sandersn** assigned to **iisaduan**
 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/54739#issuecomment-1742070945) **Zzzen** said "Thanks for the feedback. I've made the suggested changes, and it works like a charm. However, I noticed that the error message may be a bit confusing."
 * [1.8 years ago](https://github.com/microsoft/TypeScript/pull/54739#issuecomment-2113053814) **jer-sen** said "@weswigham any update on this PR ?"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54739#issuecomment-4121427800) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54750](https://github.com/microsoft/TypeScript/pull/54750) (Closed, `For Backlog Bug`, **rbuckton**)

**fix\(compiler\): synthetic comment is duplicated on class with experimental decorators**

*Prevent multiple insertions of synthetic comments on class declarations with experimental decorators in the compiler*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/54750#issuecomment-1642764208) **typescript-bot** notified that the diff-based user code test suite was run on the PR at the specified commit and provided links to the build and results
 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/54750#issuecomment-1642792126) **typescript-bot** reported test suite results comparing main and pull request merge, noted infrastructure failures and new TS2428 errors
 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/54750#issuecomment-1642862172) **typescript-bot** reported successful top-repos suite results comparing main and the pull request merge
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54750#issuecomment-4121427865) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54754](https://github.com/microsoft/TypeScript/pull/54754) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Perform structural fallbacks for reliable variance results less liberally**

*Limit structural fallbacks for variance-based type comparisons to only unreliable failures to improve performance.*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/54754#issuecomment-1604796876) **typescript-bot** provided the requested performance run results in a comparison report
 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/54754#issuecomment-1604915954) **typescript-bot** reported compilation differences and build failures for top-repos suite between main and PR merge
 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/54754#issuecomment-1604920869) **typescript-bot** reported DT test failures for backbone-relational, wordpress__admin, and alloy due to a TS2344 type constraint error
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54754#issuecomment-4121427974) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54866](https://github.com/microsoft/TypeScript/pull/54866) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Fixed some variance measurements in type aliases of generic functions**

*Experiment with improved variance measurement in generic function type aliases when intersections and unions are involved*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/pull/54866#issuecomment-1618614536) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **sandersn** assigned to **ahejlsberg**
 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/54866#issuecomment-1718367597) **Andarist** asked what tests should be used to verify progress and which parts of a referenced PR are borrowable
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54866#issuecomment-4121428033) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54884](https://github.com/microsoft/TypeScript/pull/54884) (Closed, `For Uncommitted Bug`, **rbuckton**)

**Add original filename header to more baselines**

*Add the original filename header to all baselines to simplify locating test sources during diff comparisons*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/54884#issuecomment-2261828857) **jakebailey** said "They're files in baselines/reference/transpile"
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/54884#issuecomment-2263203128) **Andarist** asked whether other baseline runners should include file name headers and suggested adding both the file name and test title to avoid duplication
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/54884#issuecomment-2277073202) **jakebailey** said "I feel like that could be fine, to include the filename and then the test name if that's easy to get. Would probably have to see an example to get a feeling."
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54884#issuecomment-4121428132) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54927](https://github.com/microsoft/TypeScript/pull/54927) (Closed, `For Backlog Bug`, **iisaduan**)

**fix: appropriate error message for out of scope label**

*Improve error message for break/continue when referencing labels that don’t exist in scope*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/54927#issuecomment-1659520993) **Mvmo** asked for @jakebailey's opinion on the attached image
 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/54927#issuecomment-1661073291) **jakebailey** suggested changing the error message to 'used before declaration' with an elaboration 'label defined here', and restricting the error range to the label only
 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/54927#issuecomment-1662429966) **Mvmo** changed the messages and created a new elaboration message while noting an alternative could be used
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54927#issuecomment-4121428555) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#54935](https://github.com/microsoft/TypeScript/pull/54935) (Closed, `For Milestone Bug`, **weswigham**)

**Extend \`addPropertyToElementList\` to differentiate get/set accessors from properties**

*Enable addPropertyToElementList to distinguish and emit get/set accessors rather than regular properties.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/54935#issuecomment-1663109722) **sandersn** said "Woops, I misread the comment history. I moved it back to Waiting on Reviewers."
 * [2.1 years ago](https://github.com/microsoft/TypeScript/pull/54935#issuecomment-1902582699) **athewsey** said "@sandersn / @weswigham any update on this? Seems like it's been waiting for review for a while and I just ran in to the same issue it's trying to solve. Thanks for your help!"
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/54935#issuecomment-3648320931) **RyanCavanaugh** criticized modifying all object type emit instead of targeting class types and warned that replacing readonly with getters could confuse users and break duplicate property equivalence logic
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/54935#issuecomment-4121428700) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55073](https://github.com/microsoft/TypeScript/pull/55073) (Closed, `Author: Team`, `For Milestone Bug`, **navya9singh**)

**Fix\(54375\) : Removing extra new lines from \`move to file\`**

*Eliminate unnecessary blank lines inserted by the move to file refactoring in TypeScript.*

 * (2.6 years ago) **typescript-bot** added labels `Author: Team`, `For Milestone Bug`, and assigned to **navya9singh**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55073#issuecomment-4121428761) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55107](https://github.com/microsoft/TypeScript/pull/55107) (Closed, `For Milestone Bug`, **rbuckton**)

**Don't emit enum members as evaluated \`Infinity\`/\`NaN\` when their symbols are shadowed**

*Prevent enum members from being emitted as Infinity or NaN when their symbols are shadowed.*

 * **sandersn** assigned to **rbuckton**
 * (14 weeks ago) **typescript-bot** added label `For Milestone Bug`, and removed label `For Backlog Bug`
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55107#issuecomment-4121428859) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55117](https://github.com/microsoft/TypeScript/pull/55117) (Closed, `For Backlog Bug`, **gabritto**)

**Add support for declaration merging with different type parameter arity**

*Add support in TypeScript for merging declarations that have different numbers of type parameters.*

 * created by **Zzzen**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **gabritto**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55117#issuecomment-4121428977) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55130](https://github.com/microsoft/TypeScript/pull/55130) (Closed, `For Backlog Bug`, **weswigham**)

**Distribute index over mapped types when normalizing types**

*Support distributing index signatures over mapped types in TypeScript’s type normalization process.*

 * **typescript-bot** added label `For Backlog Bug`
 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/55130#issuecomment-1648032168) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * **sandersn** assigned to **weswigham**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55130#issuecomment-4121429099) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55144](https://github.com/microsoft/TypeScript/pull/55144) (Closed, `For Backlog Bug`, **gabritto**)

**Discriminate JSX attributes types using spread object literals**

*Enable discrimination of JSX component props types when spreading object literals in JSX attributes.*

 * created by **Andarist**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **gabritto**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55144#issuecomment-4121429173) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55179](https://github.com/microsoft/TypeScript/pull/55179) (Closed, `For Backlog Bug`, **gabritto**)

**Fix types of super expressions in methods with this parameter**

*Adjust the type resolution of super expressions in class methods that define an explicit this parameter.*

 * created by **Andarist**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **gabritto**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55179#issuecomment-4121429249) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55226](https://github.com/microsoft/TypeScript/pull/55226) (Closed, `For Backlog Bug`, **rbuckton**)

**Allow escape characters within constructor**

*Allow escape sequences in TypeScript constructor definitions.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/55226#issuecomment-1675462198) **typescript-bot** reported that it started the regular perf test suite on the PR and shared build and results links
 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/55226#issuecomment-1675483965) **typescript-bot** posted the requested perf run results with a detailed comparison report
 * [2.6 years ago](https://github.com/microsoft/TypeScript/pull/55226#issuecomment-1678203335) **sandersn** said "No difference in performance."
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55226#issuecomment-4121429423) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55278](https://github.com/microsoft/TypeScript/pull/55278) (Closed, `For Backlog Bug`, **gabritto**)

**Fix CFA of async immediately invoked function expressions**

*Ensure TypeScript correctly performs control flow analysis on async immediately invoked function expressions.*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/55278#issuecomment-1714285327) **typescript-bot** provided links to an installable tgz, playground, and npm module along with usage instructions
 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/55278#issuecomment-1714315623) **gabritto** clarified the PR's behavior regarding floating async IIFE control flow and suggested adding a related test
 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/55278#issuecomment-1722137518) **Zzzen** added tests and opined that the property should error because it wasn’t initialized after construction
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55278#issuecomment-4121429534) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55349](https://github.com/microsoft/TypeScript/pull/55349) (Closed, `For Backlog Bug`, **navya9singh**)

**Support extract to constant in blockless arrow functions**

*Enable the extract-to-constant refactoring for blockless arrow functions.*

 * **sandersn** assigned to **navya9singh**
 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/55349#issuecomment-1742579941) **DanielRosenwasser** asked to add a test for an object literal returned from an arrow function
 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/55349#issuecomment-1743342286) **Andarist** said "@DanielRosenwasser sure thing, just pushed this extra test case out :)"
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55349#issuecomment-4121429639) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55359](https://github.com/microsoft/TypeScript/pull/55359) (Closed, `For Backlog Bug`, **rbuckton**)

**Use nodes with non\-compound assignment expressions as potential valid unique symbol declarations**

*Allow non-compound assignment expressions to be recognized as valid unique symbol declarations in TypeScript*

 * created by **Andarist**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **rbuckton**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55359#issuecomment-4121429645) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55386](https://github.com/microsoft/TypeScript/pull/55386) (Closed, `For Backlog Bug`, **weswigham**)

**Add numeric constraints to type parameters of mapped types with narrowed down array constraints**

*Allow numeric constraints on type parameters in mapped types with narrowed array constraints.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/55386#issuecomment-2375283476) **typescript-bot** provided the requested perf run results
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/55386#issuecomment-2375351928) **typescript-bot** reported tsc results for top 400 repos comparing main and pull request merge and requested review
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/55386#issuecomment-2375393934) **Andarist** noted that the error had been reported before and suggested the code was accidentally allowed in Vue types
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55386#issuecomment-4121429894) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55503](https://github.com/microsoft/TypeScript/pull/55503) (Closed, `For Backlog Bug`, **navya9singh**)

**Always error on an attempt to use \`await\` as an identifier in modules**

*TypeScript now always reports a compile error when ‘await’ is used as an identifier within modules*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/55503#issuecomment-1692317376) **typescript-bot** reported the results of running the top-repos suite comparison and indicated that everything looked good
 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/55503#issuecomment-1692391663) **typescript-bot** notified DanielRosenwasser about a failed DT test run and asked to check the log
 * **sandersn** assigned to **navya9singh**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55503#issuecomment-4121430040) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55512](https://github.com/microsoft/TypeScript/pull/55512) (Closed, `For Backlog Bug`, **rbuckton**)

**Commit to parsing a module declaration when \`declare module\` is met**

*Add support for parsing module declarations when encountering declare module statements in TypeScript*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/55512#issuecomment-1714524178) **typescript-bot** reported that they started running the perf test suite on the PR and then provided a link to the results
 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/55512#issuecomment-1714560843) **typescript-bot** provided the requested perf run results to @DanielRosenwasser
 * **sandersn** assigned to **rbuckton**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55512#issuecomment-4121430106) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55531](https://github.com/microsoft/TypeScript/pull/55531) (Closed, `For Backlog Bug`, **gabritto**)

**Fixed an issue with assignments to dynamic properties with \`exactOptionalPropertyTypes\`**

*Fix assignment errors for dynamic object properties when exactOptionalPropertyTypes compiler option is enabled.*

 * (2.5 years ago) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * **sandersn** assigned to **gabritto**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55531#issuecomment-4121430138) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55547](https://github.com/microsoft/TypeScript/pull/55547) (Closed, `Breaking Change`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Infer \`unknown\` at value positions of objects inferred from \`keyof T\`**

*Replace any with unknown for value positions in objects inferred from keyof T to prevent accidental type leaks*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/pull/55547#issuecomment-1879050326) **Andarist** acknowledged the PR's impact on Vue, critiqued its generic signature as unsafe and ambiguous, and suggested using object-based prop declarations alongside his inference change
 * [2.2 years ago](https://github.com/microsoft/TypeScript/pull/55547#issuecomment-1879069356) **jfet97** clarified that arrays of prop names were traditionally used for conciseness, noted that object syntax is also supported with a provided link, and mentioned that generics support should improve via issue #56939
 * [33 weeks ago](https://github.com/microsoft/TypeScript/pull/55547#issuecomment-3137664666) **sandersn** summarized the PR’s status and questioned whether to close it if alternative PRs are merged or if breakage is too extensive
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55547#issuecomment-4121430296) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55601](https://github.com/microsoft/TypeScript/pull/55601) (Closed, `For Uncommitted Bug`, **gabritto**)

**Avoid inferring return and yield types from unreachable statements**

*The TypeScript compiler should ignore unreachable code when inferring function return and generator yield types.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript/pull/55601#issuecomment-3544059689) **typescript-bot** provided perf run results requested by @jakebailey
 * [18 weeks ago](https://github.com/microsoft/TypeScript/pull/55601#issuecomment-3544170248) **typescript-bot** reported build failures on top repositories comparing main and the PR, highlighting TS2786 errors in TanStack/query
 * [17 weeks ago](https://github.com/microsoft/TypeScript/pull/55601#issuecomment-3547243216) **Andarist** explained that the break was expected due to return type inference change and said they would fix the code by annotating return type with never and removing unreachable code
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55601#issuecomment-4121430389) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55696](https://github.com/microsoft/TypeScript/pull/55696) (Closed, `For Uncommitted Bug`, **jakebailey**)

**Allow more things to be evaluated in enum members with template expression initializers**

*Allow enum template literal initializers to evaluate boolean and other expressions consistently.*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/pull/55696#issuecomment-1715954623) **Andarist** stated that using true in a string literal but not as an enum initializer did not seem awkward, argued that the inconsistency in template expression contexts was more problematic, and commented that enhanced compile-time error messaging and extra expression evaluations might be feasible but could be out of scope
 * **sandersn** assigned to **jakebailey**
 * [34 weeks ago](https://github.com/microsoft/TypeScript/pull/55696#issuecomment-3134209006) **sandersn** asked whether to pursue this direction or close the PR for housekeeping
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55696#issuecomment-4121430476) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55842](https://github.com/microsoft/TypeScript/pull/55842) (Closed, `For Backlog Bug`, **ahejlsberg**)

**fix\(55841\) \- Indexing with \`never\` should produce \`never\`**

*Make indexing with never return never consistently across arrays, tuples, and object types.*

 * [2 years ago](https://github.com/microsoft/TypeScript/pull/55842#issuecomment-1949338986) **typescript-bot** reported top-repos suite results comparing main and the pull request merge and noted build failures in several projects
 * [2 years ago](https://github.com/microsoft/TypeScript/pull/55842#issuecomment-1949448608) **jfet97** explained that pgSubscriberKey had type undefined, causing indexing to produce never, and noted that the PR introduced a breaking change
 * [2 years ago](https://github.com/microsoft/TypeScript/pull/55842#issuecomment-1949492490) **jfet97** explained that indexing by `never` is inherently absurd and that any resulting type is valid under ex falso quodlibet, with propagating `never` as a reasonable option
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55842#issuecomment-4121430547) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55864](https://github.com/microsoft/TypeScript/pull/55864) (Closed, `Breaking Change`, `Experiment`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Do not erase signature constraints when calculating variance**

*Retain signature constraints during variance calculations to prevent incorrect type assignments.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/55864#issuecomment-1737720250) **fatcerberus** said "It’s interesting to me that method bivariance alone isn’t enough to keep arrays covariant (though it does help with user-defined arraylikes, as pointed out by Ryan in the array subtype covariance PR)"
 * (1.6 years ago) **weswigham** added labels `Breaking Change`, `Experiment`
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/55864#issuecomment-4121430648) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#55989](https://github.com/microsoft/TypeScript/pull/55989) (Open, `For Backlog Bug`, **navya9singh**)

**Update lib\.dom\.d\.ts: \`MutationObserverInit\.attributeFilter\` can accept an iterator**

*Update lib.dom.d.ts so that MutationObserverInit.attributeFilter accepts iterators in addition to arrays.*

 * (2.3 years ago) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * **sandersn** assigned to **navya9singh**
 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`

### [PR microsoft/TypeScript#56027](https://github.com/microsoft/TypeScript/pull/56027) (Closed, `For Backlog Bug`, **weswigham**)

**Fixed a relationship check when apparent type of mapped type expands to a union**

*Corrects relationship check logic to properly handle mapped types whose apparent type expands to a union.*

 * (2.3 years ago) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * **sandersn** assigned to **weswigham**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/56027#issuecomment-4121430725) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#56100](https://github.com/microsoft/TypeScript/pull/56100) (Closed, `For Backlog Bug`, **andrewbranch**)

**Emit declarations using alias chains**

*Enable TypeScript to emit declaration files that resolve and preserve chained type aliases.*

 * [2 years ago](https://github.com/microsoft/TypeScript/pull/56100#issuecomment-2009050094) **fubhy** said "Also linked (atm. unclear if this fixes it though): https://github.com/microsoft/TypeScript/issues/55021"
 * (2 years ago) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/56100#issuecomment-4121430902) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#56165](https://github.com/microsoft/TypeScript/pull/56165) (Closed, `For Milestone Bug`, **PranavSenthilnathan**)

**Less template literal and string literal reduction**

*Evaluate the performance impact of a naive change reducing template literal and string literal handling.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/56165#issuecomment-1773397048) **typescript-bot** reported the requested perf run results
 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/56165#issuecomment-1782184877) **PranavSenthilnathan** noted that this behavior was an intentional feature and suggested implementing subtype reduction at variable declaration nodes as a compromise between eager and lazy reduction
 * [2.4 years ago](https://github.com/microsoft/TypeScript/pull/56165#issuecomment-1782201939) **jakebailey** explained that not always reducing unions led to duplicate unions and prevented fast equality checks
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/56165#issuecomment-4121431011) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#56183](https://github.com/microsoft/TypeScript/pull/56183) (Closed, `For Backlog Bug`, **iisaduan**)

**Filter out classes with private members from the contextual types for object literal nodes**

*Exclude classes with private members from contextual type inference for object literal nodes.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/pull/56183#issuecomment-1869800549) **typescript-bot** reported that the top-repos suite comparing main and the pull request merge passed with no issues
 * [2.2 years ago](https://github.com/microsoft/TypeScript/pull/56183#issuecomment-1877899317) **Andarist** explained that they applied filtering at the current level because contextual information wasn’t accessible deeper and argued that this approach is as valid as performing it in getContextualType
 * [30 weeks ago](https://github.com/microsoft/TypeScript/pull/56183#issuecomment-3217427884) **Andarist** acknowledged suggestion and moved the fix into discriminateTypeByDiscriminableItems
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/56183#issuecomment-4121431139) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

### [PR microsoft/TypeScript#56212](https://github.com/microsoft/TypeScript/pull/56212) (Closed, `Author: Team`, `For Milestone Bug`, **navya9singh**)

**Fix\(55658\): Move to file and new file syntax errors with overload functions**

*Overload function declarations are now imported only once to prevent syntax errors when moving or creating files.*

 * (2.4 years ago) **typescript-bot** added labels `Author: Team`, `For Milestone Bug`, and assigned to **navya9singh**
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/56212#issuecomment-4121431188) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates

