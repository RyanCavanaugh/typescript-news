# Report for 2026-04-15 (Wednesday, April 15th, 2026)

16 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @staticvariablejames provided reproduction steps and error details in [microsoft/TypeScript#30408](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-4254816118)
    * @janpaepke asked if the PR would be ported to 7.0 in [microsoft/TypeScript#62737](https://github.com/microsoft/TypeScript/issues/62737#issuecomment-4257479631)
    * @OldStarchy asked for clarification on default inclusion of legacy decorators in [microsoft/TypeScript#63346](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4257328096)
    * @Hamzaa6296 asked which repository to target and whether community contributions are accepted in [microsoft/TypeScript#63380](https://github.com/microsoft/TypeScript/issues/63380#issuecomment-4257893741)
    * @snarbles2 asked what the user would expect to happen differently in [microsoft/TypeScript#63398](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4260408230)
    * @fredericbahr reported slow and crashing language server after upgrading to TypeScript 6 in [microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253846712)
    * @matthew-lo-housing asked whether the issue only occurs with the MUI + Vite combination in [microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4256720363)
    * @matthew-lo-housing asked if they should install TypeScript 7 globally in [microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4256731040)

## Activity Summary

### [Issue microsoft/TypeScript#13569](https://github.com/microsoft/TypeScript/issues/13569) (Closed, `Suggestion`, `Revisit`, `Domain: lib.d.ts`)

**DOM: Font Loading API**

*Developer requests inclusion of FontFace, FontFaceSet and document.fonts typings for the CSS Font Loading API in TypeScript.*

 * [5 years ago](https://github.com/microsoft/TypeScript/issues/13569#issuecomment-802591857) **wereHamster** noted that the CSS side had reached Candidate Recommendation while the JS API remained a Working Draft and shared relevant links
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/13569#issuecomment-913143701) **s-h-a-d-o-w** noted that draft status hasn’t prevented including types by comparing web audio and font APIs and pointed out 96% JS API support via caniuse.com
 * [yesterday](https://github.com/microsoft/TypeScript/issues/13569#issuecomment-4247506804) **freshp86** said "Is this still relevant? Looking at node_modules/typescript/lib/lib.dom.d.ts it seems to already include some of the APIs that were previously missing (for example FontFace#load)."
 * [today](https://github.com/microsoft/TypeScript/issues/13569#issuecomment-4253786391) **RyanCavanaugh** said "Yep, this seems to work now."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#30408](https://github.com/microsoft/TypeScript/issues/30408) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Effort: Moderate`, `Domain: Error Messages`, `Experience Enhancement`)

**Confusing error message for labels used before definition**

*A continue to a label defined after a for loop incorrectly triggers a confusing TS1007 error.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-3685142380) **mhughes2012** said "I can take this on, I have a fix for it. Please assign me."
 * (1 week ago) **RyanCavanaugh** removed labels `Domain: Related Error Spans`, `PursuitFellowship`
 * [today](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-4254816118) **staticvariablejames** reported encountering a similar issue with a typo in the label and still getting TS1107 error in version 7.0.0-dev.20260415.1

### [Issue microsoft/TypeScript#62737](https://github.com/microsoft/TypeScript/issues/62737) (Open, `Suggestion`, `Help Wanted`, `Experimentation Needed`)

**Show incompatible union members in discriminated union discriminator errors**

*Enhance TypeScript's discriminated union error messages to identify which union members in the discriminator cause assignment failures.*

 * **RyanCavanaugh** added label `Help Wanted`
 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/62737#issuecomment-3597562402) **alpha2420** said "Hi @jankeape, I’d like to start working on this issue. Please let me know if there are any guidelines or initial steps I should follow."
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/62737#issuecomment-3611083699) **janpaepke** suggested following the contributing guidelines, referenced a prior discussion and playground link, and offered to provide further context or testing
 * [today](https://github.com/microsoft/TypeScript/issues/62737#issuecomment-4257479631) **janpaepke** expressed disappointment at the PR being closed due to the 6.0 cut-off and asked about porting it to 7.0

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4121568642) **buley** suggested that PR #63290 meets the first criterion for post-6.0 patches and asked the team for confirmation
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4121592927) **jakebailey** rejected the PR as not meeting the bar for TS 6.0 due to low usage, rare failures, and its broken state
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4133933446) **HolgerJeromin** expressed happiness about testing with Visual Studio, requested a NuGet release referencing issue #62236, provided a package link, and noted it was done a day ago
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4256022056) **DanielRosenwasser** said "@typescript-bot bump release-6.0"
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4256022474) **typescript-bot** provided a CI jobs progress update with command, status, and results links
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4256102755) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.3 for you."

### [PR microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248) (Open, `For Backlog Bug`)

**Add lib types for JSON\.rawJSON, JSON\.isRawJSON, and reviver context**

*Add TypeScript declarations for ES2025’s JSON.rawJSON, JSON.isRawJSON, and JSON.parse reviver context*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4121543687) **RyanCavanaugh** said "Reopening as this is still valid (minus commandlineParser.ts)"
 * (3 weeks ago) **RyanCavanaugh** reopened the issue
 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`
 * **typescript-bot** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#63346](https://github.com/microsoft/TypeScript/issues/63346) (Closed, `Question`)

**Experimental \(deprecated\) decorators are included by default**

*The ESNext library includes legacy experimental decorator types by default, causing conflicts with new decorator definitions.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4200850258) **RyanCavanaugh** said "The error message means what it says; you are missing the export modifier on your type alias"
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4219297379) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (6 days ago) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4257328096) **OldStarchy** clarified that '*.d.ts' files are included globally without imports and that adding an export does not address the default inclusion of legacy decorators, and pointed out the specific type name conflict
 * [today](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4257346566) **OldStarchy** identified issue 29828 as the closest match and suggested removing types instead of fixing, noting that replacing legacy decorator types could invert the problem for projects relying on the legacy syntax

### [Issue microsoft/TypeScript#63380](https://github.com/microsoft/TypeScript/issues/63380) (Open, `Bug`, `Domain: check: Type Inference`)

**Wrong inference for defaulted generic in nested call**

*TypeScript fails to infer the correct return type for nested calls to a generic function with a default type parameter.*

 * (6 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: check: Type Inference`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63380#issuecomment-4257893741) **Hamzaa6296** asked which repository to target and whether community contributions were accepted, and provided reproduction details and a suspected fix location

### [Issue microsoft/TypeScript#63398](https://github.com/microsoft/TypeScript/issues/63398) (Closed, `Unactionable`)

**Two ExpressionStatements allowed on one line with no semicolon\!**

*TypeScript incorrectly accepts two expression statements on a single line without a semicolon instead of throwing a parse error.*

 * **RyanCavanaugh** added label `Unactionable`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4244940165) **RyanCavanaugh** clarified that the issue was a misunderstanding and that TypeScript cannot permit invalid syntax
 * (yesterday) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4260319722) **conartist6** argued that TypeScript treats all character sequences as valid programs and relies on ESLint and Prettier to catch syntax errors, otherwise it would legalize any syntax
 * [later](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4260408230) **snarbles2** pointed out that TypeScript is producing syntax errors for the invalid class syntax and asked what the user would expect to happen differently
 * [later](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4260722010) **mkantor** suggested using the noEmitOnError option and clarified that the discussion pertained to code emission rather than error reporting

### [PR microsoft/TypeScript#63401](https://github.com/microsoft/TypeScript/pull/63401) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Also check package name validity in InstallPackageRequest**

*Add package name validation to the InstallPackageRequest code action, extending previous checks without altering security boundaries.*

 * (yesterday) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63401#issuecomment-4254589630) **jakebailey** said "@typescript-bot cherry-pick this to release-6.0"
 * [today](https://github.com/microsoft/TypeScript/pull/63401#issuecomment-4254590056) **typescript-bot** posted CI jobs start and completion status with links to actions runs and results
 * [today](https://github.com/microsoft/TypeScript/pull/63401#issuecomment-4254847938) **typescript-bot** said "Hey, @jakebailey! I've created #63407 for you."

### [Issue microsoft/TypeScript#63405](https://github.com/microsoft/TypeScript/issues/63405) (Open, `Question`)

**VSCode's TypeScript Language Server Keeps Crashing on a Project**

*VSCode's TypeScript server repeatedly crashes with “TSServer exited. Code: 134” when opening a basic Vite React MUI project.*

 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253390323) **hikeeba** stated that they tested on a Windows 11 laptop, offered to try on other machines later, and guessed that the previous test either didn’t wait long enough or didn’t include MUI lib usage
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253431817) **RyanCavanaugh** said "Yeah, I forgot I had the TypeScript-go LS (7.0) enabled. In 6.0 I'm seeing tsserver repeatedly spawn and exit, but I'm also seeing this in TypeScript 5.9. What changed for y'all?"
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253505723) **hikeeba** said "Unfortunately I don't have anything to point to here as for what changed. I have older projects that work, but I haven't spun up any new ones in a while until just now."
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253587623) **RyanCavanaugh** said "Repros in 5.7 as well. How did three of you land here, on the same day, for an issue that's likely been present for over a year? Maybe something in VS Code changed? That would be a useful first clue."
 * **RyanCavanaugh** removed label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4253846712) **fredericbahr** noted updates to the VSCode Language Server and JS/TS settings and reported slow and crashing behavior after upgrading to TypeScript 6
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4254729016) **RyanCavanaugh** diagnosed that the recently-shipped Material-UI v9 version interacted poorly with auto-import, observed that reverting @mui packages to v7 or disabling package.json auto-import resolved the memory issue, and recommended upgrading to TS 7 or turning off package.json enumeration
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4256720363) **matthew-lo-housing** noted no issues in other projects, mentioned this was their first time using MUI, and asked if the issue only occurred with the MUI + Vite combination
 * [today](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4256731040) **matthew-lo-housing** asked if they should install TypeScript 7 globally
 * [later](https://github.com/microsoft/TypeScript/issues/63405#issuecomment-4261291709) **RyanCavanaugh** said "Yes, TypeScript provides language features in JavaScript projects"

### [PR microsoft/TypeScript#63407](https://github.com/microsoft/TypeScript/pull/63407) (Closed, `For Uncommitted Bug`, **DanielRosenwasser**)

**🤖 Pick PR \#63401 \(Also check package name validity in\.\.\.\) into release\-6\.0**

*Cherry-pick PR #63401, adding package name validity checks, into the release-6.0 branch for review and merge.*

 * created by **typescript-bot**
 * (today) **typescript-bot** added label `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/63407#issuecomment-4254848468) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63408](https://github.com/microsoft/TypeScript/pull/63408) (Open, `For Uncommitted Bug`)

**fix: remove unused legacy decorator types**

*Remove unused legacy decorator types and associated definitions from the TypeScript codebase.*

 * created by **OldStarchy**
 * **typescript-bot** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63409](https://github.com/microsoft/TypeScript/issues/63409) (Closed, `Duplicate`)

**Abstarct members of abstarct mixin is allowed to call**

*Calling an abstract method on a class returned by an abstract mixin does not trigger a compiler error.*

 * created by **olegdunkan**
 * [later](https://github.com/microsoft/TypeScript/issues/63409#issuecomment-4259894246) **snarbles2** clarified that the error should be on `const u = new UL;` and that `u.log()` should succeed because abstract classes cannot be instantiated
 * [later](https://github.com/microsoft/TypeScript/issues/63409#issuecomment-4260085807) **MartinJohns** said "Essentially a duplicate of #32122. Mixins and abstract classes don't mix well."
 * **RyanCavanaugh** added label `Duplicate`

