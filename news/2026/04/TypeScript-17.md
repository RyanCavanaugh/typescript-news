# Report for 2026-04-17 (Friday, April 17th, 2026)

6 different users commented on 16 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#62584](https://github.com/microsoft/TypeScript/issues/62584) (Closed, `Discussion`)

**Experimental TypeScript fork with operator overloading and overload dispatch—documenting a working implementation**

*Documenting a proof-of-concept TypeScript fork enabling operator overloading and type-based function overload dispatch.*

 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/62584#issuecomment-3398424206) **RyanCavanaugh** clarified that type-directed emit is not a good idea despite its feasibility, citing slow emit, broken single-file transpile, non-working generics, runtime surprises, as-any failures, and TC39 alignment issues
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62584#issuecomment-4264758521) **GageSorrell** asked if the type-directed emit performance issue remained in version 7, questioned whether the generics limitation warranted avoiding operator overloading, and wondered if the native TS release brought operator overloading closer to feasibility
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62584#issuecomment-4264811910) **jakebailey** said "No, type-directed emit continues to be a non-goal. Note the date on that comment, long after we announced the port."
 * [today](https://github.com/microsoft/TypeScript/issues/62584#issuecomment-4269698543) **RyanCavanaugh** said "Closing for housekeeping as this is not in scope for TS"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248) (Open, `For Backlog Bug`)

**Add lib types for JSON\.rawJSON, JSON\.isRawJSON, and reviver context**

*Add TypeScript declarations for ES2025’s JSON.rawJSON, JSON.isRawJSON, and JSON.parse reviver context*

 * (3 weeks ago) **RyanCavanaugh** reopened the issue
 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4270116628) **RyanCavanaugh** said "@afurm future automated comments will result in a block; any automated activity we want to occur in this repo we will set up ourselves or already have"

### [PR microsoft/TypeScript#63310](https://github.com/microsoft/TypeScript/pull/63310) (Closed, **RyanCavanaugh**, **Copilot**)

**Mark class property initializers as outside of CFA containers**

*Restore PropertyDeclaration as a control flow container to isolate class property initializer type inference and prevent module-level narrowing leaks*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4163848637) **jakebailey** said "@typescript-bot cherry-pick this to release-6.0"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4163849118) **typescript-bot** posted a status update about CI jobs starting and linking to results
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4163862108) **typescript-bot** said "Hey, @jakebailey! I've created #63327 for you."
 * (today) **DanielRosenwasser** set milestone to `TypeScript 6.0.3`, and removed from milestone `TypeScript 6.0.2`

### [PR microsoft/TypeScript#63327](https://github.com/microsoft/TypeScript/pull/63327) (Closed, **DanielRosenwasser**)

**🤖 Pick PR \#63310 \(Mark class property initializers as\.\.\.\) into release\-6\.0**

*Cherry-pick PR #63310 marking class property initializers into the release-6.0 branch for review and merge*

 * created by **typescript-bot**
 * **typescript-bot** assigned to **DanielRosenwasser**
 * (1 week ago) **RyanCavanaugh** closed the issue
 * **DanielRosenwasser** added to milestone `TypeScript 6.0.3`

### [PR microsoft/TypeScript#63368](https://github.com/microsoft/TypeScript/pull/63368) (Closed, **jakebailey**)

**Harden ATA package name filtering**

*Restrict ATA package names to alphanumeric characters, underscores, periods, and hyphens to prevent shell-related validation issues.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63368#issuecomment-4200840842) **jakebailey** said "@typescript-bot cherry-pick this to release-6.0"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63368#issuecomment-4200841325) **typescript-bot** reported that CI jobs started and completed for the 'cherry-pick this to release-6.0' command and provided status and result links
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63368#issuecomment-4200853561) **typescript-bot** said "Hey, @jakebailey! I've created #63372 for you."
 * **DanielRosenwasser** added to milestone `TypeScript 6.0.3`
 * **typescript-bot** assigned to **jakebailey**

### [PR microsoft/TypeScript#63372](https://github.com/microsoft/TypeScript/pull/63372) (Closed, **DanielRosenwasser**)

**🤖 Pick PR \#63368 \(Harden ATA package name filtering\) into release\-6\.0**

*Apply PR #63368’s hardened ATA package name filtering to the release-6.0 branch pending review and merge.*

 * created by **typescript-bot**
 * **typescript-bot** assigned to **DanielRosenwasser**
 * (1 week ago) **jakebailey** closed the issue
 * **DanielRosenwasser** added to milestone `TypeScript 6.0.3`

### [PR microsoft/TypeScript#63401](https://github.com/microsoft/TypeScript/pull/63401) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Also check package name validity in InstallPackageRequest**

*Add package name validation to the InstallPackageRequest code action, extending previous checks without altering security boundaries.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63401#issuecomment-4254589630) **jakebailey** said "@typescript-bot cherry-pick this to release-6.0"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63401#issuecomment-4254590056) **typescript-bot** posted CI jobs start and completion status with links to actions runs and results
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63401#issuecomment-4254847938) **typescript-bot** said "Hey, @jakebailey! I've created #63407 for you."
 * **DanielRosenwasser** added to milestone `TypeScript 6.0.3`

### [Issue microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405) (Closed, `Question`)

**VSCode's TypeScript Language Server Keeps Crashing on a Project**

*VSCode's TypeScript server repeatedly crashes with “TSServer exited. Code: 134” when opening a basic Vite React MUI project.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4256720363) **matthew-lo-housing** noted no issues in other projects, mentioned this was their first time using MUI, and asked if the issue only occurred with the MUI + Vite combination
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4256731040) **matthew-lo-housing** asked if they should install TypeScript 7 globally
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4261291709) **RyanCavanaugh** said "Yes, TypeScript provides language features in JavaScript projects"
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4271511013) **Takichih** said "Disabling Json auto imports worked for me too, thx @RyanCavanaugh "
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4272466307) **himhimlo** thanked RyanCavanaugh, confirmed both solutions worked, and stated that they had started using TypeScript 7

### [Issue microsoft/TypeScript#63406](https://github.com/microsoft/TypeScript/issues/63406) (Closed, `Not a Defect`)

**TS incorrectly downgrades class fields**

*TypeScript compiler incorrectly hoists class field initializations before the super call, violating subclass initialization order.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4252904980) **dangreen** said "@mkantor we want to transpile it to es2021 "
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4253193942) **RyanCavanaugh** noted limitations in the downleveler and suggested using other tools for downleveling arbitrary third-party code
 * [today](https://github.com/microsoft/TypeScript/issues/63406#issuecomment-4272317455) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63407](https://github.com/microsoft/TypeScript/pull/63407) (Closed, `For Uncommitted Bug`, **DanielRosenwasser**)

**🤖 Pick PR \#63401 \(Also check package name validity in\.\.\.\) into release\-6\.0**

*Cherry-pick PR #63401, adding package name validity checks, into the release-6.0 branch for review and merge.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63407#issuecomment-4254848468) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (2 days ago) **jakebailey** closed the issue
 * **DanielRosenwasser** added to milestone `TypeScript 6.0.3`

### [PR microsoft/TypeScript#63412](https://github.com/microsoft/TypeScript/pull/63412) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Update CONTRIBUTING\.md with comment automation policy**

*Propose adding a comment automation policy to CONTRIBUTING.md to reduce low-value summarization comments.*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63413](https://github.com/microsoft/TypeScript/pull/63413) (Closed, `For Uncommitted Bug`)

**Improve error message for invalid continue target label**

*Update TypeScript compiler to provide a clearer error message when a continue statement targets a label outside an enclosing loop or switch scope.*

 * created by **Jah-yee**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4273544308) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **Jah-yee** closed the issue
 * (later) **Jah-yee** reopened the issue
 * [later](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4273656495) **Jah-yee** thanked for feedback and explained that the PR addressed issue #30408 by improving the diagnostic error message
 * [later](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4273921308) **jakebailey** asked to disclaim what tool was used to send the PR

### [PR microsoft/TypeScript#63414](https://github.com/microsoft/TypeScript/pull/63414) (Closed, `For Uncommitted Bug`)

**Sort JSDoc parameter suggestions by argument position**

*Sort JSDoc @param completion suggestions by parameter position using unique index-based sortText instead of alphabetical order.*

 * created by **Jah-yee**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63414#issuecomment-4274030847) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63414#issuecomment-4274036241) **jakebailey** asked to disclaim what tool was used to send the PR

