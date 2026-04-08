# Report for 2026-04-05 (Sunday, April 5th, 2026)

13 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @FranjoMindek requested an option to turn this on in [microsoft/TypeScript#42853](https://github.com/microsoft/TypeScript/issues/42853#issuecomment-4193049923)
    * @eduardocque asked whether to wait for #26242 instead of reopening the current issue in [microsoft/TypeScript#63348](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4189992468)
    * @Uanela provided debugging details about tsc restarting despite chokidar ignoring node_modules in [microsoft/TypeScript#63355](https://github.com/microsoft/TypeScript/issues/63355#issuecomment-4189474839)
    * @denis-migdal noted a regression introduced after version 5.3.3 in [microsoft/TypeScript#63363](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4192072558)

## Activity Summary

### [Issue microsoft/TypeScript#42853](https://github.com/microsoft/TypeScript/issues/42853) (Open, `Needs Investigation`, **weswigham**)

**Preserve interfaces in generated declaration files for augmentation**

*Provide a compiler option to preserve original interfaces in generated declaration files to support augmentation.*

 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/42853#issuecomment-968258953) **talks2much** referenced zardoy's initial report and provided workaround examples, noting the feature's rare usage
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/42853#issuecomment-968275925) **theKashey** said "Interesting solution, not sure I can afford it in monorepo. Currently the best workaround seems to be keeping some d.ts manually written 😔"
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/42853#issuecomment-1328235219) **jaulz** said "Unfortunately, this is still an issue. It would be really nice instead of running a script after the build. "
 * [later](https://github.com/microsoft/TypeScript/issues/42853#issuecomment-4193049923) **FranjoMindek** requested an option to enable automatic type merging for user and package types

### [Issue microsoft/TypeScript#63348](https://github.com/microsoft/TypeScript/issues/63348) (Closed, `Working as Intended`)

**Inference is not working properly**

*TypeScript fails to infer the path generic type in useStoreByPath from its string argument.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184115596) **RyanCavanaugh** provided a standard workaround using a curried function with TypeScript generics
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184124618) **eduardocque** asked if a change request or suggestion could be made without breaking TypeScript generics
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184174580) **MartinJohns** noted that the relevant issue #26242 had already been linked
 * [today](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4189938986) **typescript-bot** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4189992468) **eduardocque** asked whether they should wait for issue #26242 instead of reopening the current one

### [Issue microsoft/TypeScript#63352](https://github.com/microsoft/TypeScript/issues/63352) (Open, `Bug`, `Domain: lib.d.ts`)

**Trivial: typo**

*Corrects the misspelling of “parameter” as “paramater” in the es5.d.ts definitions file.*

 * created by **tomhamiltonlambda**
 * [today](https://github.com/microsoft/TypeScript/issues/63352#issuecomment-4188736423) **deepnav4** expressed interest in working on the issue
 * (later) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63355](https://github.com/microsoft/TypeScript/issues/63355) (Closed)

**\[Bug\]: tsc \-\-watch \-\-noEmit not respecting tsconfig\.json\.watchOptions\.excludedDirectories**

*tsc --watch --noEmit ignores tsconfig.json watchOptions.excludedDirectories and continues watching node_modules directories*

 * created by **Uanela**
 * [today](https://github.com/microsoft/TypeScript/issues/63355#issuecomment-4189470600) **MartinJohns** said "--listFiles lists the files that are part of the compilation. This has nothing to do with any directories excluded for the file watcher."
 * [today](https://github.com/microsoft/TypeScript/issues/63355#issuecomment-4189474839) **Uanela** explained that tsc restarted on node_modules changes despite chokidar ignoring them when using --listFiles for debugging
 * [today](https://github.com/microsoft/TypeScript/issues/63355#issuecomment-4189480842) **Uanela** said "Thanks, just looked closesly and found out what was actually happening https://github.com/Uanela/tsx-strict/blob/0b4437bce95ca2466cf4bdc83226d01d6d4c89bc/src/index.ts#L154"
 * (today) **Uanela** closed the issue

### [Issue microsoft/TypeScript#63357](https://github.com/microsoft/TypeScript/issues/63357) (Open, `Domain: check: Contextual Types`, `Possible Improvement`)

**Error on function return is less useful than it should be**

*TypeScript reports return-type mismatches on function assignments rather than at the actual return statement, making errors harder to diagnose.*

 * created by **pfgithub**
 * [later](https://github.com/microsoft/TypeScript/issues/63357#issuecomment-4193147732) **RyanCavanaugh** said "This is basically because of #241, but maybe we could special case it? Not sure"
 * (later) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Dormant`

### [Issue microsoft/TypeScript#63358](https://github.com/microsoft/TypeScript/issues/63358) (Open, `Bug`, `Domain: JSX/TSX`)

**TSX error location error with location and JSX comment**

*A preceding JSX comment causes TypeScript to report a non-ReactNode type error on the comment instead of the expression.*

 * created by **RobertSandiford**

### [Issue microsoft/TypeScript#63361](https://github.com/microsoft/TypeScript/issues/63361) (Closed, `Question`)

**\`Flatten\<O\>\` does not merge union object fields — distributes instead**

*Flatten<O> merges root-level object unions correctly but fails to recursively flatten nested object union fields, leaving them distributed.*

 * created by **kevalcodezee**
 * [later](https://github.com/microsoft/TypeScript/issues/63361#issuecomment-4192309871) **jcalz** explained why the type failed due to union distribution, provided an alternative implementation, and directed to Stack Overflow or Discord for further discussion
 * **RyanCavanaugh** added label `Question`

### [PR microsoft/TypeScript#63362](https://github.com/microsoft/TypeScript/pull/63362) (Closed)

**fix\(checker\): allow unknown\[\] as valid mixin constructor rest param type**

*Update the TypeScript compiler to accept unknown[] rest parameters in mixin constructors and adjust diagnostics accordingly.*

 * created by **0xkhass**
 * [later](https://github.com/microsoft/TypeScript/pull/63362#issuecomment-4191989288) **0xkhass** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63362#issuecomment-4193218391) **RyanCavanaugh** said "See https://github.com/microsoft/TypeScript?tab=readme-ov-file#contribute - bugfixes should be in typescript-go repo"
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63363](https://github.com/microsoft/TypeScript/issues/63363) (Open, `Needs Investigation`)

**Inside a generic function with a remapped type as parameter, elements are wrongfully inferred as {}\.**

*Indexed access of remapped generic type properties in a generic function leads to them being inferred as {} instead of their defined type.*

 * created by **denis-migdal**
 * [later](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4192072558) **denis-migdal** noted that the behavior was introduced after version 5.3.3 and previously produced a TypeScript index signature error
 * [later](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4193188506) **RyanCavanaugh** said "Why are you writing the function signature this way in the first place?"

### [PR microsoft/TypeScript#63364](https://github.com/microsoft/TypeScript/pull/63364) (Open)

**Fix: parameter typo in es5 definitions \#63352**

*Corrects a misleading parameter name in src/lib/es5.d.ts to improve TypeScript definition accuracy.*

 * created by **rishabh1230**

