# Report for 2026-06-18 (Thursday, June 18th, 2026)

2 different users commented on 2 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508) (Open, `Discussion`)

**6\.0 Migration Guide**

*Placeholder issue for drafting and publishing the migration guide for version 6.0.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4228915356) **Kimxons** noted that the solution worked okay
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4331983425) **linnbenton** highlighted inconsistent baseUrl deprecation warnings in TS 6+ monorepo setups and asked whether this is intended as an early signal for TS 7 or if the migration strategy for monorepos is still evolving
 * [today](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4743768229) **sahin52** pointed out that the default value of "strict" became true and linked the related pull request and issue
 * [today](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4744398238) **sahin52** said "Also various other changes can be found in the milestone: https://github.com/microsoft/TypeScript/milestone/218?closed=1"

### [Issue microsoft/TypeScript#63565](https://github.com/microsoft/TypeScript/issues/63565) (Open, `Bug`)

**\`export\` modifier on \`enum\` disables \`This condition will always return \* ts2845\`**

*Adding the export modifier to an enum prevents TypeScript from reporting a ts2845 error on an always-true condition.*

 * created by **eps1lon**
 * [later](https://github.com/microsoft/TypeScript/issues/63565#issuecomment-4751644133) **mkantor** explained that enums can be declaration-merged and that external modules might define the same enum, causing pessimistic analysis
 * [later](https://github.com/microsoft/TypeScript/issues/63565#issuecomment-4751672793) **mkantor** clarified that they misread the condition and that the second part only checks the truthiness of AdapterOutputType.PAGES

