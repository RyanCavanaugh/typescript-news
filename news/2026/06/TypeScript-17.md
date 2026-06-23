# Report for 2026-06-17 (Wednesday, June 17th, 2026)

3 different users commented on 3 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508) (Open, `Discussion`)

**6\.0 Migration Guide**

*Placeholder issue for drafting and publishing the migration guide for version 6.0.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4153001690) **dskloetc** thanked cscnk52 for the information and mentioned that the error message could have been more helpful
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4228915356) **Kimxons** noted that the solution worked okay
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4331983425) **linnbenton** highlighted inconsistent baseUrl deprecation warnings in TS 6+ monorepo setups and asked whether this is intended as an early signal for TS 7 or if the migration strategy for monorepos is still evolving
 * [later](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4743768229) **sahin52** pointed out that the default value of "strict" became true and linked the related pull request and issue

### [Issue microsoft/TypeScript#63564](https://github.com/microsoft/TypeScript/issues/63564) (Closed)

**Generic type to \`json\` method of \`fetch\`**

*Enable specifying the JSON return type by adding a generic type parameter to the fetch Response.json method.*

 * (today) **rtritto** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63564#issuecomment-4730245004) **rtritto** asked if the issue would still be rejected given that response.json uses JSON.parse and other issues refer to JSON.type
 * [today](https://github.com/microsoft/TypeScript/issues/63564#issuecomment-4730271134) **MartinJohns** stated that it would still be rejected, noted similar past issues, argued that it adds no safety and misleads users about type checking, and suggested using declaration merging as a workaround
 * [today](https://github.com/microsoft/TypeScript/issues/63564#issuecomment-4734195934) **nmain** said "Duplicate of https://github.com/microsoft/TypeScript/issues/44000 / https://github.com/microsoft/TypeScript/issues/33037"

### [Issue microsoft/TypeScript#63565](https://github.com/microsoft/TypeScript/issues/63565) (Open, `Bug`)

**\`export\` modifier on \`enum\` disables \`This condition will always return \* ts2845\`**

*Adding the export modifier to an enum prevents TypeScript from reporting a ts2845 error on an always-true condition.*

 * created by **eps1lon**

