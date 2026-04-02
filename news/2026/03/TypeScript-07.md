# Report for 2026-03-07 (Saturday, March 7th, 2026)

8 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @asd585140-glitch requested to merge Android 13 in [microsoft/TypeScript#59029](https://github.com/microsoft/TypeScript/issues/59029#issuecomment-4018333450)
    * @denis-migdal provided playground examples to illustrate expected compiler error behavior in [microsoft/TypeScript#63218](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4017183362)

## Activity Summary

### [Issue microsoft/TypeScript#59029](https://github.com/microsoft/TypeScript/issues/59029) (Closed, `Domain: LS: Type Display`, `Domain: LS: Quick Info`, `Fix Available`, **gabritto**)

**Support Expandable Quick Info/Hover Verbosity**

*Enable expandable quick info hover in the editor for toggling detailed type references and elided content*

 * (49 weeks ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * (46 weeks ago) **gabritto** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/59029#issuecomment-4018330776) **asd585140-glitch** said "دمج القالب المتوافق مع نسخه اندرويد ١٣"
 * [today](https://github.com/microsoft/TypeScript/issues/59029#issuecomment-4018333450) **asd585140-glitch** said "دمج اندرويد ١٣"

### [Issue microsoft/TypeScript#63211](https://github.com/microsoft/TypeScript/issues/63211) (Closed, `Duplicate`)

**switch case does not create separate block scope for let declarations**

*The TypeScript compiler fails to enforce block scoping for let declarations in switch cases, allowing variables to leak across branches.*

 * created by **duanshixuan**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63211#issuecomment-3996505247) **MartinJohns** said "Duplicate of #19503. Used search terms: switch let in:title"
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63211#issuecomment-4017909852) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63216](https://github.com/microsoft/TypeScript/issues/63216) (Open, `Duplicate`)

**\`keyof\` behaves differently with index signatures created using \`Record\`**

*The keyof operator returns string|number for an explicit {[x: string]: unknown} index signature but only string for Record<string, unknown> despite both supporting numeric indexing.*

 * [today](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016524048) **juhort** acknowledged not using an issue template
 * [today](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016548263) **mkantor** expressed agreement with not displaying the type as an index signature and suggested opening a separate issue since the current behavior was misleading
 * [today](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016764287) **MartinJohns** clarified that issue #45447 was not the same, explained that keyof {[x: string]: any} and keyof Record<string, any> return different results, and noted confusion due to a display issue
 * [today](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4017187645) **jcalz** said "Duplicate #31013"

### [Issue microsoft/TypeScript#63218](https://github.com/microsoft/TypeScript/issues/63218) (Open, `Suggestion`, `Awaiting More Feedback`)

**Error \(2320\) when extending interfaces where a property is both readonly and readwrite\.**

*Extending two interfaces that declare the same property as readonly and writable erroneously triggers a conflict error*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4015967785) **denis-migdal** noticed that a property’s readonly status varied depending on the order of extends and provided a playground example
 * [today](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4017183362) **denis-migdal** provided two code examples illustrating missing TypeScript errors for getter/setter implementations

### [PR microsoft/TypeScript#63220](https://github.com/microsoft/TypeScript/pull/63220) (Closed)

**Fix silentNeverType leak through keyof in return type inference**

*Prevent the silentNeverType sentinel from leaking through keyof during return type inference by adding an identity check in getIndexType.*

 * created by **srobinson**
 * [today](https://github.com/microsoft/TypeScript/pull/63220#issuecomment-4018001745) **srobinson** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63220#issuecomment-4018036438) **jakebailey** said "This is the same as https://github.com/microsoft/TypeScript/pull/62825"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63221](https://github.com/microsoft/TypeScript/pull/63221) (Closed)

**fix: suppress TS4055/TS4073 for protected methods using typeof parameter**

*Suppress TS4055 and TS4073 errors for protected class methods using typeof parameter types.*

 * created by **umeshmore45**
 * [later](https://github.com/microsoft/TypeScript/pull/63221#issuecomment-4018796052) **umeshmore45** said "@microsoft-github-policy-service agree"
 * (later) **umeshmore45** closed the issue
 * (later) **umeshmore45** reopened the issue
 * (later) **umeshmore45** closed the issue

### [PR microsoft/TypeScript#63222](https://github.com/microsoft/TypeScript/pull/63222) (Open)

**fix: suppress TS4055/TS4073 for protected methods using typeof parameter**

*Suppress TS4055/TS4073 in protected methods by treating parameters as accessible when using typeof in return types.*

 * created by **umeshmore45**

### [Issue microsoft/TypeScript#63223](https://github.com/microsoft/TypeScript/issues/63223) (Open, `Bug`)

**Toggling \`isolatedModules\` in \`tsconfig\.json\` while running the compiler in \`watch\` mode, doesn't re\-emit \`const enums\`, unlike toggling \`preserveConstEnums\`, which does**

*Unlike preserveConstEnums toggles, changing isolatedModules in watch mode does not re-emit const enums until a full rebuild.*

 * created by **rotemdan**

