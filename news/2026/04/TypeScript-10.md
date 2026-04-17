# Report for 2026-04-10 (Friday, April 10th, 2026)

5 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @denis-migdal asked if using X<any> should cause Z's default type to be any or constrained by X's generic parameter and whether this behavior is intended in [microsoft/TypeScript#63385](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4225821954)
    * @denis-migdal asked whether TypeScript should use the defined constraint instead of any when using extends X<any> in [microsoft/TypeScript#63385](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4225875350)
    * @denis-migdal asked about the stance of TS on `extends X<any>` and potential warning options in [microsoft/TypeScript#63385](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4226079817)
    * @denis-migdal asked to consider adding a '?' keyword for unknown generic parameters in [microsoft/TypeScript#63385](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4228206481)

## Activity Summary

### [Issue microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508) (Open, `Discussion`)

**6\.0 Migration Guide**

*Placeholder issue for drafting and publishing the migration guide for version 6.0.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4152848989) **dskloetc** described that their issue matched another user's, showing the deprecated 'moduleResolution=node10' error when upgrading TypeScript without requesting node10 and noting they couldn't provide a repro
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4152939556) **cscnk52** provided guidance on using node16/nodenext/bundler for moduleResolution and linked to the TypeScript docs
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4153001690) **dskloetc** thanked cscnk52 for the information and mentioned that the error message could have been more helpful
 * [later](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4228915356) **Kimxons** noted that the solution worked okay

### [Issue microsoft/TypeScript#63384](https://github.com/microsoft/TypeScript/issues/63384) (Closed, `Won't Fix`, `7.0 LS Migration`)

**JS and TS Tasking long time to start which make the save of tsx files slower\.**

*Delays in the JavaScript and TypeScript formatter startup are slowing or blocking TSX file saves.*

 * created by **flexdevguy**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#63385](https://github.com/microsoft/TypeScript/issues/63385) (Closed, `Design Limitation`)

**\`null\`/\`undefined\` guards sometimes adds \`& \({} \| undefined\`/\`& \({} \| null\` \(out of nowhere\) to the tested variable\.**

*Null guards in generic functions introduce an unintended intersection with {} | null or undefined into the variable's type.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4225557149) **MartinJohns** explained that testing in the Playground showed the behavior changed in TypeScript 4.8 and that it is working as intended
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4225713907) **denis-migdal** explained that he reduced the issue to a minimal reproducible example and tested multiple versions, challenged the assumption that the behavior was intended, and proposed two hypotheses with supporting code examples
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4225821954) **denis-migdal** analyzed a Playground example showing X<any> leading to Z defaulting to any and asked if this behavior is intended or an oversight
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4225844441) **MartinJohns** explained that narrowing by not-undefined still allows null, producing `null | {}`, and that `Hook & unknown` is equivalent to `Hook` because unknown doesn't change the type
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4225875350) **denis-migdal** questioned whether TypeScript should use the defined constraint instead of any when using extends X<any>
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4226079817) **denis-migdal** asked if giving `any` to a constrained generic type parameter should be discouraged and whether TypeScript should warn when using `extends X<any>`, discussed workaround drawbacks, and asked for the TS team's stance on `extends X<any>`
 * [today](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4228206481) **denis-migdal** proposed a '?' keyword for unknown generic parameters with fallback behaviors, along with '*' and '??' keywords, and suggested a compiler option to detect explicit any usage in generics

### [PR microsoft/TypeScript#63386](https://github.com/microsoft/TypeScript/pull/63386) (Open)

**Document charAt edge case behavior**

*Document that String.charAt returns an empty string for indexes outside the valid range to ensure consistency.*

 * created by **bwalter007**

### [PR microsoft/TypeScript#63387](https://github.com/microsoft/TypeScript/pull/63387) (Closed)

**Document charAt edge case behavior**

*Clarify edge case behavior of String.charAt to ensure documentation consistency across String methods.*

 * created by **bwalter007**
 * (later) **bwalter007** closed the issue

### [PR microsoft/TypeScript#63388](https://github.com/microsoft/TypeScript/pull/63388) (Closed)

**Document charAt edge case behavior**

*Clarify charAt edge case behavior in documentation to ensure consistency with other String methods.*

 * created by **bwalter007**
 * (later) **bwalter007** closed the issue

### [PR microsoft/TypeScript#63389](https://github.com/microsoft/TypeScript/pull/63389) (Closed)

**fix\(lib\): correct typo in es5\.d\.ts — paramater \-\> parameter**

*Corrects a typo in the es5.d.ts JSDoc comment for Array.prototype.splice, changing 'paramater' to 'parameter'.*

 * created by **hijingsong**

