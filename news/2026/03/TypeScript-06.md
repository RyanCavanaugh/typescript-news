# Report for 2026-03-06 (Friday, March 6th, 2026)

9 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @yhaskell provided a real-world example clarifying the desired behavior in [microsoft/TypeScript#4881](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4014984624)
    * @yhaskell provided a real-world example clarifying the desired behavior in [microsoft/TypeScript#4881](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4014984624)
    * @juhort asked for a link to the particular issue in [microsoft/TypeScript#63216](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016309249)
    * @juhort asked the maintainer to review the issue again in [microsoft/TypeScript#63216](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016348082)
    * @denis-migdal reported inconsistent readonly behavior based on extends order in [microsoft/TypeScript#63218](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4015967785)

## Activity Summary

### [Issue microsoft/TypeScript#4881](https://github.com/microsoft/TypeScript/issues/4881) (Open, `Suggestion`, `Needs Proposal`)

**Request: Class Decorator Mutation**

*Enable TypeScript to correctly type-check class decorators that add properties for mixins.*

 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-3436455409) **pjeby** argued that disallowing type changes in decorators is unfounded because decorators are merely syntax sugar and naturally allow type alteration
 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-3438211558) **matthew-dean** argued that TypeScript's class and decorator restrictions reflect maintainers' bias towards C#-style syntax and limit JavaScript's dynamic capabilities
 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-3438211558) **matthew-dean** argued that TypeScript's class and decorator restrictions reflect maintainers' bias towards C#-style syntax and limit JavaScript's dynamic capabilities
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4014984624) **yhaskell** illustrated that Zod validation in function form works correctly and expressed expectation that decorator form should behave similarly, providing code examples
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4014984624) **yhaskell** illustrated that Zod validation in function form works correctly and expressed expectation that decorator form should behave similarly, providing code examples

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987822011) **typescript-bot** posted an automated build status update for bump release-6.0
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987851804) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.1-rc for you."
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4010254515) **HolgerJeromin** suggested mentioning the deprecation of `module=none` in the 6.0-rc1 announcement blog post
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4013218539) **DanielRosenwasser** said "The RC is published to npm, the release page is available here, and we'll have the blog post up shortly."

### [Issue microsoft/TypeScript#63212](https://github.com/microsoft/TypeScript/issues/63212) (Open, `Docs`)

**Add JSX\.ElementChildrenAttribute change to TypeScript 5\.8 release notes**

*Document the breaking change in TS 5.8 requiring explicit JSX.ElementChildrenAttribute for children inference*

 * created by **nmattia**
 * (today) **RyanCavanaugh** added label `Docs`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63213](https://github.com/microsoft/TypeScript/issues/63213) (Closed)

**Closed by author**

*The author retracted the issue and closed it because it was opened in error.*

 * created by **ScienceArtist**
 * [today](https://github.com/microsoft/TypeScript/issues/63213#issuecomment-4012562199) **MartinJohns** said "Kids, don't forget to report comments and users like this."
 * (today) **ScienceArtist** closed the issue

### [Issue microsoft/TypeScript#63214](https://github.com/microsoft/TypeScript/issues/63214) (Open, `Discussion`)

**Google feedback on TS 6\.0\-beta**

*Google’s TypeScript team finds the TS 6.0-beta upgrade manageable with minor code tweaks for strict defaults and deprecated namespace syntax while anticipating deprecation challenges in TS 7.0.*

 * created by **cecilyhunt**
 * [today](https://github.com/microsoft/TypeScript/issues/63214#issuecomment-4015049709) **DanielRosenwasser** asked whether upgrading to TS 6.0 would still be difficult without the ignoreDeprecations option

### [PR microsoft/TypeScript#63215](https://github.com/microsoft/TypeScript/pull/63215) (Open)

**Fix stack overflow in error generation for recursive mapped types**

*Break infinite recursion causing stack overflow in recursive mapped type error messaging by eagerly caching the error type.*

 * created by **hamzax180**
 * [today](https://github.com/microsoft/TypeScript/pull/63215#issuecomment-4014993816) **hamzax180** agreed with microsoft-github-policy-service
 * (today) **hamzax180** closed the issue
 * (today) **hamzax180** reopened the issue

### [Issue microsoft/TypeScript#63216](https://github.com/microsoft/TypeScript/issues/63216) (Open, `Duplicate`)

**\`keyof\` behaves differently with index signatures created using \`Record\`**

*The keyof operator returns string|number for an explicit {[x: string]: unknown} index signature but only string for Record<string, unknown> despite both supporting numeric indexing.*

 * created by **juhort**
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016292886) **MartinJohns** said "This is working as intended. Just use these search terms and look through the existing issues: record keyof in:title"
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016309249) **juhort** said "@MartinJohns Umm...I went through that actually but couldn't find anything. If you don't mind, can you please link any particular issue?"
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016315863) **MartinJohns** said "Did you check the closed issues?"
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016327719) **juhort** said "Yeah, I tried checking them."
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016342472) **MartinJohns** attached an image and referenced issue #45447
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016348082) **juhort** clarified that this issue differs from microsoft/TypeScript#45447 and that both keyof forms should return string | number, then asked the maintainer to revisit the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016506590) **mkantor** clarified that Record is a mapped type rather than an index signature, illustrated the difference with examples, noted the unexpected divergence in keyof behavior on infinite key domains, proposed generalizing the issue to mapped types, and asked why no issue template was used
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016522630) **juhort** acknowledged that the QuickInfo tooltip shouldn’t display the type as an index signature and confirmed that the issue generalizes to string index signatures
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016524048) **juhort** acknowledged not using an issue template
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016548263) **mkantor** expressed agreement with not displaying the type as an index signature and suggested opening a separate issue since the current behavior was misleading
 * [later](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016764287) **MartinJohns** clarified that issue #45447 was not the same, explained that keyof {[x: string]: any} and keyof Record<string, any> return different results, and noted confusion due to a display issue

### [Issue microsoft/TypeScript#63218](https://github.com/microsoft/TypeScript/issues/63218) (Open, `Suggestion`, `Awaiting More Feedback`)

**Error \(2320\) when extending interfaces where a property is both readonly and readwrite\.**

*Extending two interfaces that declare the same property as readonly and writable erroneously triggers a conflict error*

 * created by **denis-migdal**
 * [later](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4015967785) **denis-migdal** noticed that a property’s readonly status varied depending on the order of extends and provided a playground example

### [Issue microsoft/TypeScript#63219](https://github.com/microsoft/TypeScript/issues/63219) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow primitive LHS to \`instanceof\` operator if RHS is a custom \`hasInstance\`**

*Enable using instanceof with primitive left-hand values when the right-hand side defines a custom Symbol.hasInstance method.*

 * created by **xuld**
 * [later](https://github.com/microsoft/TypeScript/issues/63219#issuecomment-4016296812) **MartinJohns** said "Duplicate of #59492."

