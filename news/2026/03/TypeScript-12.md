# Report for 2026-03-12 (Thursday, March 12th, 2026)

12 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @jedwards1211 asked if the setting was not working anymore even after restarting VSCode in [microsoft/TypeScript#60082](https://github.com/microsoft/TypeScript/issues/60082#issuecomment-4049066466)
    * @monsanto reported a bug and requested a fix in [microsoft/TypeScript#62200](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4054811294)
    * @ekalkutin asked how to configure Temporal to resolve the 'Cannot find name Temporal' error in VSCode in [microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4050062146)
    * @ekalkutin reported that they couldn't get it working in the IDE and suspected an issue with the VSCode language server in [microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4050248778)
    * @shahanahmed86 provided repro steps and root cause analysis in [microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4054861901)
    * @paigefletcher1282-code reported that issues persisted under watch mode in [microsoft/TypeScript#63228](https://github.com/microsoft/TypeScript/issues/63228#issuecomment-4048157480)
    * @paigefletcher1282-code reported that the issue hasn't been reproduced and linked to the original issue in [microsoft/TypeScript#63244](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4055854137)

## Activity Summary

### [Issue microsoft/TypeScript#60082](https://github.com/microsoft/TypeScript/issues/60082) (Open, `Needs Investigation`)

**autoImportSpecifierExcludeRegexes needs a window refresh for changes to take effect**

*Changes to autoImportSpecifierExcludeRegexes in VSCode settings only apply after reloading the window instead of immediately.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/60082#issuecomment-2460713543) **kafumanto** mentioned having the same issues and shared a workaround using autoImportSpecifierExcludeRegexes
 * [48 weeks ago](https://github.com/microsoft/TypeScript/issues/60082#issuecomment-2780630473) **tusharsnx** noted that restarting the TS server also applied autoImportSpecifierExcludeRegexes changes
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/60082#issuecomment-4049066466) **jedwards1211** asked if the setting did not work anymore even after restarting VSCode

### [Issue microsoft/TypeScript#62200](https://github.com/microsoft/TypeScript/issues/62200) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**)

**Deprecate, remove \`\-\-moduleResolution node10\`**

*Remove the outdated --moduleResolution node/node10 flag in TypeScript 7.0, advising nodenext for Node.js and esnext with bundler for web.*

 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-3348049368) **sallf** corrected the second code block to include moduleResolution as "bundler"
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-3536829117) **Adesoji1** said "so what's the solution?"
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-3543611338) **RyanCavanaugh** said "Depends on the problem, we usually say"
 * [later](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4054811294) **monsanto** reported encountering TS2351 errors with default class exports in NodeNext, hypothesized a TypeScript bug, offered to share a repro, and requested a fix before removing moduleResolution: node

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987851804) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.1-rc for you."
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4010254515) **HolgerJeromin** suggested mentioning the deprecation of `module=none` in the 6.0-rc1 announcement blog post
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4013218539) **DanielRosenwasser** said "The RC is published to npm, the release page is available here, and we'll have the blog post up shortly."
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4050062146) **ekalkutin** asked how to use Temporal in TypeScript and reported a VSCode TS Language Server error saying 'Cannot find name Temporal'
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4050203670) **jakebailey** said "You need lib set to esnext."
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4050248778) **ekalkutin** explained that they had already set lib to esnext and still couldn’t get it working, suspecting a VSCode language server issue
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4050263019) **jakebailey** said "You'd need the nightly extension, or to set the tsdk VS Code option to point to your local repo."
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4050281506) **ekalkutin** thanked jakebailey and reported that he got it working with a settings.json configuration
 * [later](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4055902206) **paigefletcher1282-code** thanked and confirmed that the issue was fixed

### [Issue microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195) (Open, `Needs More Info`)

**Debug Failure: "No error for last overload signature" crash when CustomTypeOptions\.resources uses typeof on a large \(~10k line\) JSON file**

*TypeScript crashes with 'No error for last overload signature' when using typeof on a large JSON for i18next CustomTypeOptions.resources.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-3967758768) **RyanCavanaugh** said "We need a concrete repro we can run ourselves"
 * **RyanCavanaugh** added label `Needs More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-3996641257) **shahanahmed86** said "@RyanCavanaugh don't close issue, It will take me some time but I will share the concrete repro, honestly, super busy since the day I post this issue."
 * [later](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4054861901) **shahanahmed86** apologized for not providing a minimal repro, identified that the crash occurs when TypeScript hits the 5-million type-instantiation limit processing i18next’s types over a large translation JSON, and provided reproduction details and code snippets

### [Issue microsoft/TypeScript#63214](https://github.com/microsoft/TypeScript/issues/63214) (Open, `Discussion`)

**Google feedback on TS 6\.0\-beta**

*Google’s TypeScript team finds the TS 6.0-beta upgrade manageable with minor code tweaks for strict defaults and deprecated namespace syntax while anticipating deprecation challenges in TS 7.0.*

 * created by **cecilyhunt**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63214#issuecomment-4015049709) **DanielRosenwasser** asked whether upgrading to TS 6.0 would still be difficult without the ignoreDeprecations option
 * **RyanCavanaugh** added label `Discussion`
 * [today](https://github.com/microsoft/TypeScript/issues/63214#issuecomment-4050685218) **cecilyhunt** noted that the largest impact change in TS 7.0 was the deprecation of esModuleInterop=false, which broke about 0.2% of libraries (mostly those using export = in their typings), and mentioned support efforts to unblock TS7

### [Issue microsoft/TypeScript#63228](https://github.com/microsoft/TypeScript/issues/63228) (Closed, `Needs Investigation`, **jakebailey**)

**TypeScript 6 API Bug \- \`isSourceFileDefaultLibrary\` false negative on program structure reuse**

*In TypeScript 6.0.0-beta, isSourceFileDefaultLibrary incorrectly returns false for default library files when reusing program structure.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63228#issuecomment-4041547524) **jakebailey** said "@StyleShit I think https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4041195460 should fix it."
 * [today](https://github.com/microsoft/TypeScript/issues/63228#issuecomment-4044993165) **StyleShit** said "@jakebailey works for me in the ts-eslint PR 👍 "
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63228#issuecomment-4048157480) **paigefletcher1282-code** noted that problems occurred under watch mode

### [Issue microsoft/TypeScript#63233](https://github.com/microsoft/TypeScript/issues/63233) (Closed, `Duplicate`)

**Typescript**

*TypeScript intentionally disregards type narrowings in callbacks and does not reset them after function calls.*

 * created by **angelgsbrielruano**
 * **angelgsbrielruano** added label `Duplicate`
 * (today) **angelgsbrielruano** closed the issue

### [PR microsoft/TypeScript#63239](https://github.com/microsoft/TypeScript/pull/63239) (Closed)

**Fix missing lib files in reused programs**

*Reintroduce omitted library files in reused programs and cherry-pick the fix to the 6.0 branch.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4041169687) **typescript-bot** reported build job status and provided links to started and completed results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4041195460) **typescript-bot** provided installation instructions and testing links for the PR build
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4047982610) **jakebailey** said "@typescript-bot cherry-pick this to release-6.0"
 * [today](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4047983416) **typescript-bot** reported that the cherry-pick workflow started and failed due to unexpected inputs in the workflow dispatch event
 * [today](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4048111534) **jakebailey** said "@typescript-bot cherry-pick this to release-6.0"
 * [today](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4048112868) **typescript-bot** posted CI status update indicating the cherry-pick job start and results
 * [today](https://github.com/microsoft/TypeScript/pull/63239#issuecomment-4048125110) **typescript-bot** said "Hey, @jakebailey! I've created #63246 for you."

### [Issue microsoft/TypeScript#63241](https://github.com/microsoft/TypeScript/issues/63241) (Closed)

**دمج**

*Request to merge the awesomeWM 4.3 release tag into the main codebase.*

 * created by **asd585140-glitch**
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63242](https://github.com/microsoft/TypeScript/issues/63242) (Closed)

**04bea1e3cdab4cad52569b7995071a08ec267b12ضبط**

*A GitHub issue linking commit 1429c7e80cb9b2b00c426387db1ec24f7fb50e8e in TooTallNate/proxy-agents related to ضبط*

 * created by **asd585140-glitch**
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63244](https://github.com/microsoft/TypeScript/issues/63244) (Open, `Needs Proposal`)

**bug\(lib\): Explicitly stating wrong return type of \`Promise\.then\` without arguments results in no error**

*Current TypeScript versions fail to report a type mismatch when Promise<string> is assigned from Promise.resolve(1).then() with no arguments.*

 * created by **iluha168**
 * [today](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4046207682) **jcalz** suggested retyping Promise.then using the NoInfer utility type to improve typing
 * [today](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4047353571) **iluha168** suggested splitting the PromiseLike.then and Promise.then definitions into two overloads to avoid the NoInfer breaking change and maintain return type hints
 * [today](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4050549212) **Andarist** mentioned another instance of .then's typing affecting a scenario negatively and linked to a related TypeScript issue
 * [later](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4055854137) **paigefletcher1282-code** reported that the issue hadn't yet been reproduced and linked to issue #62071

### [PR microsoft/TypeScript#63246](https://github.com/microsoft/TypeScript/pull/63246) (Closed, **DanielRosenwasser**)

**🤖 Pick PR \#63239 \(Fix missing lib files in reused pro\.\.\.\) into release\-6\.0**

*Cherry-pick PR #63239 into the release-6.0 branch to restore missing library files.*

 * created by **typescript-bot**
 * **typescript-bot** assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript#63247](https://github.com/microsoft/TypeScript/issues/63247) (Closed, `Duplicate`)

**Tor**

*TypeScript intentionally ignores type narrowings inside callbacks and does not reset them after function calls.*

 * created by **angelgsbrielruano**
 * **angelgsbrielruano** added label `Duplicate`

### [PR microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248) (Open)

**Add lib types for JSON\.rawJSON, JSON\.isRawJSON, and reviver context**

*Add TypeScript declarations for ES2025’s JSON.rawJSON, JSON.isRawJSON, and JSON.parse reviver context*

 * created by **VedantMadane**
 * [later](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4054871416) **Renegade334** corrected MDN, noting that although the feature has stage 4 approval, it is not in the ES2025 draft

