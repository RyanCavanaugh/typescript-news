# Report for 2026-10-18 (Saturday, October 17th, 2026)

7 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @rf- asked if the couldStartTrivia function in Go is vestigial and should be removed in [microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6237153149)

## Activity Summary

### [Issue microsoft/TypeScript#64727](https://github.com/microsoft/TypeScript/issues/64727) (Closed)

**TS 7: declaration emit property order depends on which other files are in the program**

*TypeScript 7’s declaration emitter produces inconsistent property ordering in generated d.ts files depending on which files are included in the program.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64727#issuecomment-6099523263) **maschwenk** said "I have no idea if this is something we care about or not so please feel free to dismiss"
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64727#issuecomment-6123975636) **jakebailey** said "This is definitely something to fix yes"
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64727#issuecomment-6125491855) **maschwenk** provided a link to a possible fix in a pull request
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64728](https://github.com/microsoft/TypeScript/pull/64728) (Closed, `For Uncommitted Bug`)

**Cache undefined widening properties per symbol, not per name**

*Key the undefined-property widening cache by symbol instead of name to ensure consistent property declarations across unrelated types.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64728#issuecomment-6129506551) **jakebailey** said "Unless copilot points out something I missed, this fix seems fine"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750) (Open, `For Uncommitted Bug`)

**Add support for Jujutsu conflict markers**

*Extend TypeScript’s conflict marker detection to support Jujutsu-style markers using %, \ and + separators.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6131219606) **typescript-automation[bot]** reported the results of the requested perf run
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6150291835) **RyanCavanaugh** inquired if opening an issue was mandatory or optional and suggested using an issue to discuss conflict marker forms
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6159916825) **rf-** said "Good points, thanks @jakebailey! Apologies for not covering all of the possible formats, it definitely makes sense to do them all at once. I'll open an issue to ref in the PR."
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6237153149) **rf-** questioned whether the couldStartTrivia function was vestigial dead code in Go and suggested its removal

### [Issue microsoft/TypeScript#64852](https://github.com/microsoft/TypeScript/issues/64852) (Open)

**Support Jujutsu conflict markers**

*Add parsing support for Jujutsu's custom conflict marker syntax to prevent spurious TypeScript errors*

 * created by **rf-**

### [PR microsoft/TypeScript#64853](https://github.com/microsoft/TypeScript/pull/64853) (Open, `For Backlog Bug`)

**Support @deprecated marker on namespace aliases \(fixes \#62340\)**

*Add support for @deprecated tags on namespace aliases by updating type reference resolution to check alias deprecations.*

 * created by **prasad2512**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64853#issuecomment-6247442974) **prasad2512** addressed review suggestions in commit f2ca475, including checks for deprecated aliases in import-type qualified references, preservation of deprecation checks for merged type and value declarations, inclusion of re-exported export specifiers, and extended unit tests

### [PR microsoft/TypeScript#64854](https://github.com/microsoft/TypeScript/pull/64854) (Open, `For Backlog Bug`)

**Fix parsing of call with type arguments after left shift \(\<\<\)**

*Modify TypeScript's parser to revert speculative type-argument parsing when '<<' is followed by errors so '1 << alignof<T[]>()' parses correctly.*

 * created by **ArchiTecCTT**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64854#issuecomment-6246372087) **ArchiTecCTT** expressed agreement with the policy service

### [Issue microsoft/TypeScript#64855](https://github.com/microsoft/TypeScript/issues/64855) (Open, `Design Limitation`)

**"This expression is not callable\." false positive on union of generic functions where the call is valid for all types in the union**

*TypeScript reports a false "not callable" error when calling a union of compatible generic functions.*

 * created by **DetachHead**
 * [later](https://github.com/microsoft/TypeScript/issues/64855#issuecomment-6251795447) **jcalz** described known limitation of union call signatures allowing at most one overloaded and one generic member and noted that two generic members prevent unification

### [PR microsoft/TypeScript#64856](https://github.com/microsoft/TypeScript/pull/64856) (Open, `For Uncommitted Bug`)

**Report implicit any errors in function type binding patterns during checking**

*Enable TypeScript to detect and report implicit any types in function binding patterns during type checking.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64856#issuecomment-6248514169) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64857](https://github.com/microsoft/TypeScript/pull/64857) (Open, `For Uncommitted Bug`)

**Fix crash when global augmentations resolve pattern ambient modules with import attributes**

*Skip inherited properties to prevent compiler crash when resolving pattern ambient modules with import attributes*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64857#issuecomment-6251506059) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

