# Report for 2026-05-31 (Sunday, May 31st, 2026)

9 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @hkleungai asked for documentation on .d.ts files taking priority over .js files in [microsoft/TypeScript#63523](https://github.com/microsoft/TypeScript/issues/63523#issuecomment-4592123266)

## Activity Summary

### [Issue microsoft/TypeScript#62257](https://github.com/microsoft/TypeScript/issues/62257) (Open, `Bug`, `Domain: Declaration Emit`, `Fix Available`, **DanielRosenwasser**, **weswigham**, **Copilot**)

**Declaration file emits symbol property keys without importing them**

*TypeScript’s declaration file emitter omits imports for unique symbol property keys, causing undefined symbol errors in consumer d.ts files.*

 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * (16 weeks ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/62257#issuecomment-4589043826) **akbarim1689-wq** attached an image to the comment

### [Issue microsoft/TypeScript#63515](https://github.com/microsoft/TypeScript/issues/63515) (Closed, `Not a Defect`)

**Excess property check on nested object literals dropped in 6\.0 when parameter is a generic "Exact" mapped\-type guard**

*TypeScript 6.0 stops reporting nested excess properties in object literals when using a generic Exact mapped-type guard.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63515#issuecomment-4576549268) **snarbles2** analyzed type inference differences between TS 5.9.3 and 6.0 and concluded the issue wasn't with EPC
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63515#issuecomment-4577630364) **RyanCavanaugh** explained that simulated exact types aren't perfect and that two different function signatures having different behavior isn't a bug
 * [today](https://github.com/microsoft/TypeScript/issues/63515#issuecomment-4588976504) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63517](https://github.com/microsoft/TypeScript/pull/63517) (Closed, `For Backlog Bug`)

**fix: \`ReadonlySet\` lacks documentation for \`has\`, \`forEach\` and \`size\`**

*Added missing JSDoc comments for ReadonlySet’s forEach, has, and size and ReadonlyMap’s methods to ensure consistency with the mutable interfaces*

 * created by **arnavnagzirkar**
 * (today) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63517#issuecomment-4587815329) **arnavnagzirkar** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63517#issuecomment-4587975021) **mkantor** noted that the diff duplicated existing proposals and lacked disclosure of AI coding tools
 * [today](https://github.com/microsoft/TypeScript/pull/63517#issuecomment-4588771313) **arnavnagzirkar** closed the PR as a duplicate of existing issues and apologized for the noise, noting AI assistance
 * (today) **arnavnagzirkar** closed the issue

### [PR microsoft/TypeScript#63518](https://github.com/microsoft/TypeScript/pull/63518) (Closed, `For Backlog Bug`)

**fix: Inconsistencies in ESM\-style imports of accessibility\-modified proper\.\.\.**

*Resolve inconsistencies in ESM-style imports of accessibility-modified class exports by updating checker logic and related documentation.*

 * created by **arnavnagzirkar**
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#63519](https://github.com/microsoft/TypeScript/pull/63519) (Closed, `For Backlog Bug`)

**fix: \`silentNeverType\` leak in contextual parameter types coming from anon\.\.\.**

*Propagate NonInferrableType flags to anonymous object type instantiations to prevent silentNeverType leaking in contextual parameter types.*

 * created by **arnavnagzirkar**
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#63520](https://github.com/microsoft/TypeScript/pull/63520) (Closed, `For Backlog Bug`)

**fix: Deprecation error message reporting method type as deprecated instead\.\.\.**

*Add an identifier check in addDeprecatedSuggestionWithSignature to display the deprecated method name instead of its full signature in deprecation messages.*

 * created by **arnavnagzirkar**
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#63521](https://github.com/microsoft/TypeScript/pull/63521) (Closed, `For Backlog Bug`)

**fix: Incorrect report of self\-referencing type for static fields**

*Prevent false circularity errors when inferring static property initializer types in generic class expressions by detecting in-progress symbol resolutions.*

 * created by **arnavnagzirkar**
 * **typescript-bot** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#63522](https://github.com/microsoft/TypeScript/issues/63522) (Open, `Bug`)

**Declarations that shadow global \`Symbol\`  break emit for \`using\` declarations**

*Declaring a local Symbol class that shadows the global Symbol breaks using declaration emissions and leads to runtime Symbol.dispose errors.*

 * created by **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript/issues/63522#issuecomment-4592215906) **nmain** said "Similar to https://github.com/microsoft/TypeScript/issues/61150."

### [Issue microsoft/TypeScript#63523](https://github.com/microsoft/TypeScript/issues/63523) (Open, `Working as Intended`)

**tsc may fail to report error when \`file\.js\` & \`file\.d\.ts\` coexist, even when \`@ts\-check\` is added on \`file\.js\`\.**

*After TypeScript 4.5 update, JavaScript files with @ts-check ignore errors if a corresponding .d.ts file is present.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript/issues/63523#issuecomment-4591680219) **MartinJohns** explained that .d.ts files took priority over .js files and suggested enabling --skipLibCheck or generating .d.ts from .js
 * [later](https://github.com/microsoft/TypeScript/issues/63523#issuecomment-4592123266) **hkleungai** noted skipLibCheck was enabled but the bug persisted, questioned that .d.ts files took priority over .js files, and suggested documentation clarification, highlighting a tsc ordering inconsistency

### [PR microsoft/TypeScript#63524](https://github.com/microsoft/TypeScript/pull/63524) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**feat\(lib\): add Math\.sumPrecise type definition \(ES2026\)**

*Add Math.sumPrecise type definition to TypeScript library declarations for ES2026.*

 * created by **godfengliang**
 * **typescript-bot** added label `For Backlog Bug`

