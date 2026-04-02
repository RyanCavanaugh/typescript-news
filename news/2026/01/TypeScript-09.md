# Report for 2026-01-09 (Friday, January 9th, 2026)

12 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @zacaj reported that TS silently ignores `satisfies` when using spreads in [microsoft/TypeScript#39998](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-3730376223)
    * @nstringham asked for JSDoc syntax to export types from modules in [microsoft/TypeScript#48104](https://github.com/microsoft/TypeScript/issues/48104#issuecomment-3730837719)

## Activity Summary

### [Issue microsoft/TypeScript#39998](https://github.com/microsoft/TypeScript/issues/39998) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: perform excess property checks when spreading an inline object literal**

*Add excess property checks for inline object literals spread within other object literals to catch invalid properties.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-2024878251) **megaboich** mentioned encountering the issue, noted TypeScript ignored the error, and expressed disappointment that it remained unresolved since 2017
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-2110801768) **vtgn** expressed disappointment about TypeScript's inability to catch validation errors early, noting they encountered the issue in a simple case
 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-3223170523) **dpeter99** said "I have just run into this at work, while trying to figure out whay I wasn't getting "may only specify known properties" warnings."
 * [today](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-3730376223) **zacaj** critiqued the lack of validation for `satisfies` when spreads were used

### [Issue microsoft/TypeScript#42219](https://github.com/microsoft/TypeScript/issues/42219) (Open, `Suggestion`, `Awaiting More Feedback`)

**\[Feature\] Import non\-js content as const string**

*Enable importing non-JS file content as const string with compile-time TypeScript types via import.meta.content.*

 * **RyanCavanaugh** added label `Suggestion`
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-849032239) **mariusGundersen** said "I think with #42539 and the support for go-to-definition for text files then this feature would be a nice next step. "
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-1400486580) **nsaunders** supported the idea and described a CSS workaround using a `*.css.ts` module with build tool extraction, syntax highlighting and Prettier limitations, and linked a demo project
 * [later](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-3732822567) **valler** said "This should be compatible with type stripping, so it should be a JS feature really. The request is not so much about typing, but to reduce the need for custom loaders and/or intermediary build steps."

### [Issue microsoft/TypeScript#48104](https://github.com/microsoft/TypeScript/issues/48104) (Open, `Suggestion`, `Awaiting More Feedback`)

**JSDoc export type support**

*Support JSDoc export type syntax to share typedefs like AjaxStatus across modules.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/48104#issuecomment-2225903671) **nmss** suggested adding an @export syntax and noted inability to re-export types imported with @import
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/48104#issuecomment-3090071171) **doox911-opensource** said "Need to re-export types"
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/48104#issuecomment-3288918049) **boneskull** described that using alias-style @typedefs was limiting because it couldn't handle multiple types and created duplicate types, and said they used type-only .ts sources with conditional subpath exports instead
 * [today](https://github.com/microsoft/TypeScript/issues/48104#issuecomment-3730837719) **nstringham** suggested adding a JSDoc syntax for exporting types analogous to TypeScript's `export type`

### [Issue microsoft/TypeScript#60704](https://github.com/microsoft/TypeScript/issues/60704) (Closed, `Needs Investigation`, **andrewbranch**)

**Rethink AutoImportProvider automatic limits**

*Propose replacing the ten-entrypoint cap on auto-import provider with depth-based module resolution limits to accommodate multi-export packages.*

 * (33 weeks ago) **andrewbranch** set milestone to `TypeScript 5.9.0`, and removed from milestone `TypeScript 5.8.0`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/60704#issuecomment-3613577715) **jedwards1211** questioned whether transitive module exports were being added to the auto import index and suggested limiting scans to only explicit dependencies' exposed modules
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#60726](https://github.com/microsoft/TypeScript/pull/60726) (Open, `For Uncommitted Bug`)

**Merge trivially mergeable intersection types for identity comparison**

*Enable TypeScript’s isTypeIdenticalTo checker to recognize trivially mergeable intersections like {a:1}&{b:2} as identical to {a:1; b:2}.*

 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60726#issuecomment-2564236697) **som-sm** explained that the difference stems from two cases mentioned in a linked issue
 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60726#issuecomment-2564324382) **mrazauskas** asked if the patch could be packaged for testing and noted they replaced .isTypeRelatedTo() with a custom type walker in TSTyche
 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60726#issuecomment-2564645897) **MichaelMitchell-at** noted that the longer definition of IsEqual failed for nested types and recommended using the shorter definition, offering two alternative options
 * [later](https://github.com/microsoft/TypeScript/pull/60726#issuecomment-3732920869) **mrazauskas** clarified that the intersection of two identical union types expands to all pairwise intersections and thus doesn’t equal the original union

### [Issue microsoft/TypeScript#62787](https://github.com/microsoft/TypeScript/issues/62787) (Closed, `Bug`, `Help Wanted`, **Copilot**)

**"Never nullish" checks miss "never nullish" through parens**

*TypeScript’s never-nullish checks inconsistently fail to flag parenthesized never-nullish expressions.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/62787#issuecomment-3598073776) **RyanCavanaugh** provided an automated list of similar issues for potential duplicates
 * (5 weeks ago) **RyanCavanaugh** added labels `Bug`, `Help Wanted`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62789](https://github.com/microsoft/TypeScript/pull/62789) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Fix "never nullish" diagnostic missing expressions wrapped in parentheses**

*The never-nullish TS2881 diagnostic was not reported for operands wrapped in parentheses in nullish coalescing expressions*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3726604843) **RyanCavanaugh** said "@typescript-bot test top800"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3726604982) **typescript-bot** reported test top800 job start and completion statuses with links
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3726927034) **typescript-bot** reported results of running the top 800 repos with tsc comparing main and the PR merge, noting that everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3730119857) **jakebailey** said "Oh, I opened this, so I can't review it, and now neither can you"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62829](https://github.com/microsoft/TypeScript/issues/62829) (Closed, `Needs Investigation`, **andrewbranch**)

**How to trace/debug auto import suggestions?**

*Enable tsserver debug logging to diagnose why auto-import suggestions are missing for an ESM package*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3614138523) **jedwards1211** asked whether auto imports would dynamically look things up and include an OOM bail-out when too many dependencies exceed memory
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3614193302) **andrewbranch** explained why the rewrite’s auto-imports system uses separate buckets for project and node_modules files, avoids retaining ASTs for memory efficiency, and aligns with user expectations
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3614579761) **jedwards1211** mentioned building an auto import server for Flow that indexed import statements and exports, which led to high memory usage while offering advanced sorting and suggestion features
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#62941](https://github.com/microsoft/TypeScript/issues/62941) (Open, `Bug`, `Help Wanted`, `Domain: check: Contextual Types`)

**Crash: RangeError: Maximum call stack size exceeded during contextual typing of object literal with yield in computed property name**

*TypeScript throws a stack overflow when contextual typing an object with a generator yielding in a computed property name.*

 * (4 days ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: check: Contextual Types`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/62941#issuecomment-3730076709) **RyanCavanaugh** said "Also repros in 7.0"

### [Issue microsoft/TypeScript#62944](https://github.com/microsoft/TypeScript/issues/62944) (Closed, `Suggestion`, `Declined`)

**Allow inferred object literal optional properties**

*Introduce syntax for inferring optional object literal properties (e.g. prop2?) to allow marking certain properties optional during type inference.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3719568811) **MartinJohns** clarified that using z.optional in a transform with renaming lost optionality and that the proposed b?: syntax wouldn’t change the outcome, then acknowledged in an edit that the suggestion could apply to the transform argument
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3719611102) **rtcpw** clarified that zod already handles optionality for simple use cases and that the proposed syntax only changes types and is relevant in transforms where validation is skipped
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3720167739) **guillaumebrunerie** clarified usage of zod transform and demonstrated that the two code examples differ at runtime in including or omitting optional fields
 * [today](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3731345071) **typescript-bot** said "This issue has been marked as "Declined" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#62958](https://github.com/microsoft/TypeScript/pull/62958) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Test updates for strict initialization**

*Modifies tests to prevent 'variable used before assignment' errors under default strict initialization through declarations, assertions, initializers, or toggling strictness.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62958#issuecomment-3721595033) **DanielRosenwasser** said "@copilot please review"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62958#issuecomment-3721595574) **Copilot** said "@DanielRosenwasser I've opened a new pull request, #62964, to work on those changes. Once the pull request is ready, I'll request review from you."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62958#issuecomment-3721596279) **DanielRosenwasser** said "no no no no"
 * [today](https://github.com/microsoft/TypeScript/pull/62958#issuecomment-3730512167) **jakebailey** said "I am sort of confused why these changes are needed to switch strict; can you give an example of changes to look at or why they differ?"
 * [today](https://github.com/microsoft/TypeScript/pull/62958#issuecomment-3730818713) **DanielRosenwasser** listed four solutions for addressing test suite issues with strictNullChecks and strictPropertyInitialization
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#62962](https://github.com/microsoft/TypeScript/issues/62962) (Closed, `Duplicate`)

**Monorepo support**

*Allow TypeScript compiler to recognize monorepo package boundaries and skip type checking of node_modules during noEmit builds*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3726518341) **valler** clarified that they meant tsc -b with automatic inference of references and emphasized its importance
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3726691945) **valler** added a workaround suggesting use of `tsc --build` with references mirroring `package.json` dependencies to minimize full builds
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3727161649) **valler** proposed updating the composite config to an enum with values false, true, and package to eliminate references and leverage package.json for monorepo builds
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3729859200) **RyanCavanaugh** said "This is a duplicate of #25376, then. Everything you said there (e.g. don't rebuild downstream projects if .d.ts didn't change) is already true of tsc -b"
 * (today) **RyanCavanaugh** added label `Duplicate`, and removed labels `Suggestion`, `Needs Proposal`
 * [later](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3732365532) **valler** acknowledged the similarity to an existing issue, thanked the pointer, and explained that they already knew about tsc -b behavior and suggested an enum for composite might suffice for some setups

### [Issue microsoft/TypeScript#62967](https://github.com/microsoft/TypeScript/issues/62967) (Open, `Suggestion`, `Help Wanted`, `Experience Enhancement`)

**JSDoc comments for async\_hooks are confusing/misleading**

*JSDoc comments in the async_hooks module misleadingly discourage its use while recommending AsyncLocalStorage, causing confusion in TypeScript.*

 * created by **a-non-a-mouse**

### [PR microsoft/TypeScript#62968](https://github.com/microsoft/TypeScript/pull/62968) (Open, `For Backlog Bug`)

**fix\(checker\): Allow element access expressions in computed property names if argument is literal **

*Relax computed property name checks to permit element access expressions with static literal arguments in type literals.*

 * created by **kairosci**
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#62969](https://github.com/microsoft/TypeScript/pull/62969) (Closed, `For Uncommitted Bug`)

**Remove unnecessary type assertions**

*Remove unnecessary type assertions found during testing of the @typescript-eslint/no-unnecessary-type-assertion lint rule without affecting runtime or TS errors.*

 * created by **ulrichstark**
 * [today](https://github.com/microsoft/TypeScript/pull/62969#issuecomment-3730722389) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62969#issuecomment-3730722397) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#62970](https://github.com/microsoft/TypeScript/issues/62970) (Open, `Bug`, `Domain: lib.d.ts`)

**\`Intl\.CollatorOptions\['collation'\]\` is missing value \`'default'\`**

*TypeScript's Intl.CollatorOptions type omits the 'default' collation value.*

 * created by **quisido**

### [PR microsoft/TypeScript#62971](https://github.com/microsoft/TypeScript/pull/62971) (Open, `For Backlog Bug`)

**add \`collation\` to \`Intl\.CollatorOptions\`**

*Add the collation property to Intl.CollatorOptions to enable specifying string comparison rules for different locales*

 * created by **quisido**
 * **typescript-bot** added label `For Uncommitted Bug`

