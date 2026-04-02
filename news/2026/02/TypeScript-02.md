# Report for 2026-02-02 (Monday, February 2nd, 2026)

11 different users commented on 18 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#40604](https://github.com/microsoft/TypeScript/issues/40604) (Open, `Suggestion`, `Awaiting More Feedback`)

**List @deprecated strikethroughs in Problems tab**

*Add an optional setting to list TypeScript @deprecated strikethroughs in the Problems tab for easier tracking*

 * [49 weeks ago](https://github.com/microsoft/TypeScript/issues/40604#issuecomment-2677654136) **kozi** said "👍 "
 * [47 weeks ago](https://github.com/microsoft/TypeScript/issues/40604#issuecomment-2707242430) **sehrgut** said "I found this when looking for the setting I assumed to already exist to enable deprecation warnings. It's surprising to me that this isn't base functionality, and I hope we get it included."
 * [43 weeks ago](https://github.com/microsoft/TypeScript/issues/40604#issuecomment-2777729588) **AstroGD** said "I agree - Would love to see this as it would make development much easier"
 * [today](https://github.com/microsoft/TypeScript/issues/40604#issuecomment-3838839787) **X-lem** said "2026... this would be very helpful. Upgrading some dependencies and going file by file sucks."

### [Issue microsoft/TypeScript#57533](https://github.com/microsoft/TypeScript/issues/57533) (Open, `Suggestion`, `Needs Proposal`)

**Expose design\-time type information in TC39 decorator metadata when \`emitDecoratorMetadata: true\`**

*Allow emitDecoratorMetadata with TC39 decorators to expose design-time type information at runtime*

 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/57533#issuecomment-2904695784) **mlhaufe** asked for clarification about the use of this.constructor in the initializer and requested expansion on the "decorators kit" concept
 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/57533#issuecomment-2904895055) **nomagick** clarified that method/property decorators cannot access the class without an instance, acknowledged ctx.metadata as a shared data mechanism, referenced the original decorators proposal for one-way data sharing, affirmed the legitimacy of TC39 Decorators with metadata, and apologized for the disturbance
 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/57533#issuecomment-2904920548) **mlhaufe** recommended an article by @rauschma on JavaScript decorators
 * [today](https://github.com/microsoft/TypeScript/issues/57533#issuecomment-3837702624) **zookatron** argued that focusing solely on ECMAScript compatibility overlooked the need for emitting static type metadata, highlighted that most popular statically typed languages support runtime reflection of type information, and warned that without emitDecoratorMetadata TypeScript would become an outlier and force developers to use a preprocessor

### [Issue microsoft/TypeScript#62210](https://github.com/microsoft/TypeScript/issues/62210) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **weswigham**)

**Deprecate, remove support for import assertions**

*TypeScript will deprecate import assertions in 6.0 and remove them in 7.0 in favor of the 'import ... with' syntax.*

 * (2 days ago) **typescript-bot** added labels `Fix Available`, `Fix Available`, `Fix Available`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63015](https://github.com/microsoft/TypeScript/issues/63015) (Closed, `Bug`, `Fix Available`, `Domain: Crashes`, **gabritto**)

**Regression Crash: RangeError: Maximum call stack size exceeded in isThisInTypeQuery on Nightly**

*Nightly TypeScript crashes with RangeError stack overflow when type-checking a union of call signatures with differing return types*

 * **RyanCavanaugh** added to milestone `TypeScript 6.0.0`
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Crashes`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#63026](https://github.com/microsoft/TypeScript/pull/63026) (Closed, `For Milestone Bug`, **gabritto**)

**Fixed a crash caused by circularly\-reentrant \`getEffectsSignature\`**

*Restores control flow container flags to function-like type-level nodes to prevent circular recursion in getEffectsSignature.*

 * **typescript-bot** added label `For Milestone Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3790911144) **ahejlsberg** expressed unease about introducing a stopgap recursion limiter and suggested restoring original ContainerFlags.IsControlFlowContainer values to match previous behavior
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3791104920) **Andarist** said "Thanks for the feedback. I’ll work on the suggested solution"
 * [today](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3836606081) **gabritto** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3836606595) **typescript-bot** reported CI build statuses and linked results for multiple test commands
 * [today](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3836701464) **typescript-bot** reported infrastructure failures but confirmed everything else passed
 * [today](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3836716546) **typescript-bot** notified @gabritto of the DT test results being ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3836898553) **typescript-bot** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3837001077) **typescript-bot** reported that tests passed for the top 400 repos comparing main and refs/pull/63026/merge
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#63030](https://github.com/microsoft/TypeScript/pull/63030) (Closed, `Breaking Change`, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Deprecate alwaysStrict: false in TypeScript 6\.0**

*TypeScript 6.0 deprecates alwaysStrict=false, emitting warnings and requiring ignoreDeprecations to silence them ahead of its removal in 7.0.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787685188) **typescript-bot** provided results of running tsc on the top 400 repos comparing main and the pull request merge and reported that everything looked good
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3791464828) **jakebailey** noted that the PR would not detect the problem because alwaysStrict can be disabled by setting strict to false and suggested forcing alwaysStrict when strict is false
 * **jakebailey** added label `Breaking Change`
 * **DanielRosenwasser** added to milestone `TypeScript 6.0.0`

### [Issue microsoft/TypeScript#63065](https://github.com/microsoft/TypeScript/issues/63065) (Closed, `Question`)

**Is \`\`class A extends \(B\<T\>\)\<T\> {}\`\` valid code?**

*Asking whether the syntax `class A extends (B<T>)<T> {}` is valid TypeScript code without errors.*

 * **RyanCavanaugh** added label `Question`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3827912099) **fisker** asked for a more specific error message instead of the generic "Cannot find name X"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3827967756) **bradzacher** identified two problematic TypeScript behaviors related to parentheses in class heritage and invalid generic instantiation syntax
 * [today](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3838333823) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3838572718) **bradzacher** said "@typescript-bot we were waiting for the TS team to respond..."

### [Issue microsoft/TypeScript#63073](https://github.com/microsoft/TypeScript/issues/63073) (Closed, `Duplicate`)

**Argument of type 'string \| String' is not assignable to parameter of type 'string'\.**

*TypeScript does not collapse a 'string | String' union to 'string' after type checks, causing RegExp.test to error.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63073#issuecomment-3826627617) **RyanCavanaugh** said "This is basically #2361"
 * **RyanCavanaugh** added label `Duplicate`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63073#issuecomment-3826636795) **RyanCavanaugh** pointed out that since String and Boolean both undergo identical conversion in .test(), treating Boolean input as valid is as questionable as using true directly
 * [today](https://github.com/microsoft/TypeScript/issues/63073#issuecomment-3838333649) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63074](https://github.com/microsoft/TypeScript/issues/63074) (Open, `Not a Defect`)

**\`x is any\` type guard widens \`unknown\` type even after the relevant scope has been exited**

*Custom type guard isAny incorrectly widens unknown types to any beyond the guard’s scope*

 * created by **coreywoodfield**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63074#issuecomment-3827797037) **MartinJohns** said "Why would you ever write a x is any type guard?"
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63074#issuecomment-3836787790) **RyanCavanaugh** said "This is a sort of unavoidable consequence of how control flow works, and yeah there doesn't seem to be any reason to do this in the first place"

### [PR microsoft/TypeScript#63075](https://github.com/microsoft/TypeScript/pull/63075) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove ES5 references, misc cleanup**

*Remove non-test ES5 references, clean up dead code, and simplify enum identifier emission to ES2015+ in baselines.*

 * (3 days ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63076](https://github.com/microsoft/TypeScript/pull/63076) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update implied default for module based on target**

*Default module format now follows the ECMAScript target (commonjs, es2015, es2020, es2022, or esnext).*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63076#issuecomment-3827654852) **typescript-bot** posted an automated build status update
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63076#issuecomment-3827695007) **typescript-bot** notified that DT test results were ready and everything looked the same
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63076#issuecomment-3827887922) **typescript-bot** reported that TypeScript compilation results for the top 800 repositories matched between main and the pull request merge
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63077](https://github.com/microsoft/TypeScript/pull/63077) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **weswigham**, **jakebailey**)

**Deprecate import assert in favor of import with**

*Deprecate 'import assert' syntax in favor of 'import with' and update tests to cover both deprecated and non-deprecated usage.*

 * (2 days ago) **typescript-bot** added labels `For Milestone Bug`, `For Milestone Bug`
 * **jakebailey** added label `Breaking Change`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63078](https://github.com/microsoft/TypeScript/pull/63078) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 2 updates**

*Bump GitHub Actions dependencies by updating actions/cache from v5.0.2 to v5.0.3 and upgrading github/codeql-action.*

 * **dependabot[bot]** added label `github_actions`
 * (yesterday) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63080](https://github.com/microsoft/TypeScript/issues/63080) (Closed, `Needs More Info`)

**\[Bug\]: Intersection of imported conditional types becomes overly permissive and accepts invalid properties**

*Intersections of imported type aliases in TypeScript lose strictness and accept invalid properties, unlike same-file intersections.*

 * created by **Uanela**
 * [later](https://github.com/microsoft/TypeScript/issues/63080#issuecomment-3839918479) **MartinJohns** pointed out that TypeScript allows additional properties and that excess property checks are a linter feature, and suggested the issue stems from using a weak type

### [PR microsoft/TypeScript#63081](https://github.com/microsoft/TypeScript/pull/63081) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Hide omitted expression types in type baselines**

*Move suppression of omitted-expression types from tsgo-port to main to align type baselines with tsgo behavior.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#63082](https://github.com/microsoft/TypeScript/issues/63082) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add support for OSC8 hyperlinks in TTY output**

*Support OSC8 hyperlinks in TypeScript build output to enable reliable clickable file paths in terminal emulators*

 * created by **matthieusieben**

### [Issue microsoft/TypeScript#63083](https://github.com/microsoft/TypeScript/issues/63083) (Closed)

**Fixs**

*A vague request to “Fix” the issue with no further details provided.*

 * created by **gitme1-ym**

