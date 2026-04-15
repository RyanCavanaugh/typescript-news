# Report for 2026-04-12 (Sunday, April 12th, 2026)

8 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @afurm asked whether the trie needed to index non-prefix segments too in [microsoft/TypeScript#63343](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4234453594)

## Activity Summary

### [PR microsoft/TypeScript#63343](https://github.com/microsoft/TypeScript/pull/63343) (Open)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Optimize removeStringLiteralsMatchedByTemplateLiterals by building a prefix trie for efficient template literal matching*

 * created by **eps1lon**
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4180238308) **jakebailey** said "Is this different than https://github.com/microsoft/TypeScript/pull/59759?"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4180269841) **eps1lon** said "Looks like the same at a glance. Yours is already doing some size estimation it seems. I haven't accounted for opting out of trie-based search for small types."
 * [later](https://github.com/microsoft/TypeScript/pull/63343#issuecomment-4234453594) **afurm** asked whether the trie needed to index non-prefix segments too

### [Issue microsoft/TypeScript#63352](https://github.com/microsoft/TypeScript/issues/63352) (Closed, `Bug`, `Domain: lib.d.ts`)

**Trivial: typo**

*Corrects the misspelling of “parameter” as “paramater” in the es5.d.ts definitions file.*

 * (6 days ago) **RyanCavanaugh** added label `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63352#issuecomment-4229744543) **dagangtj** said "I'd like to work on this. I'll submit a PR shortly."
 * [later](https://github.com/microsoft/TypeScript/issues/63352#issuecomment-4234588240) **tomhamiltonlambda** said "At least one PR has been made. Closing."
 * (later) **tomhamiltonlambda** closed the issue

### [Issue microsoft/TypeScript#63385](https://github.com/microsoft/TypeScript/issues/63385) (Open, `Design Limitation`)

**\`null\`/\`undefined\` guards sometimes adds \`& \({} \| undefined\`/\`& \({} \| null\` \(out of nowhere\) to the tested variable\.**

*Null guards in generic functions introduce an unintended intersection with {} | null or undefined into the variable's type.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4225875350) **denis-migdal** questioned whether TypeScript should use the defined constraint instead of any when using extends X<any>
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4226079817) **denis-migdal** asked if giving `any` to a constrained generic type parameter should be discouraged and whether TypeScript should warn when using `extends X<any>`, discussed workaround drawbacks, and asked for the TS team's stance on `extends X<any>`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4228206481) **denis-migdal** proposed a '?' keyword for unknown generic parameters with fallback behaviors, along with '*' and '??' keywords, and suggested a compiler option to detect explicit any usage in generics
 * [later](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4236078898) **mkantor** praised the AnyX workaround, suggested using type parameter defaults and infer to extract constraints, endorsed the '?' proposal as lower priority, recommended aligning its syntax with partial type argument inference and HKT proposals, and advised opening or finding an existing issue to pitch it
 * [later](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4236340685) **denis-migdal** noted that many people use X<any> without noticing its dangers and described his surprise at how the any constraint behaved, mentioned he found no existing issues on the topic, and stated he would wait for Ryan before opening a suggestion issue
 * [later](https://github.com/microsoft/TypeScript/issues/63385#issuecomment-4236655344) **denis-migdal** suggested a fourth workaround using an Ensure<T, U> type with example and linked to a Playground; noted uncertainty about inference in complex cases and preference for variance keywords

### [PR microsoft/TypeScript#63395](https://github.com/microsoft/TypeScript/pull/63395) (Closed, `For Backlog Bug`)

**Fix MIDIMessageEvent\.data incorrectly typed as nullable**

*Update the MIDIMessageEvent.data definition to remove its erroneous nullability and match the Web MIDI API spec.*

 * created by **Nedunchezhiyan-M**
 * [today](https://github.com/microsoft/TypeScript/pull/63395#issuecomment-4232364942) **typescript-bot** notified that the pull request updated generated DOM declaration files which should not be edited and that the PR would be closed
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63396](https://github.com/microsoft/TypeScript/pull/63396) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 2 updates**

*Update GitHub Actions group by bumping actions/upload-artifact to v7.0.1 and actions/github-script.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript#63397](https://github.com/microsoft/TypeScript/issues/63397) (Open, `Suggestion`, `Needs Proposal`)

**skipLibChecks specificity**

*Enable skipLibCheck to accept glob patterns for selectively skipping type checking on specified declaration files.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript/issues/63397#issuecomment-4237637681) **dragomirtitian** said "This  is similar to https://github.com/microsoft/TypeScript/issues/30511 but that issue is specifically for just node_modules"

