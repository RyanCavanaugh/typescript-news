# Report for 2026-03-03 (Tuesday, March 3rd, 2026)

8 different users commented on 20 different issues.

## Recommended Actions

 * Response Recommended
    * @arkhipovdenis provided a suggestion and link for the ts-remote tool in [microsoft/TypeScript#28985](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-3996676287)
    * @denis-migdal asked if it would be possible to make a VSCode extension using the TS language server to offer a PoC in [microsoft/TypeScript#62634](https://github.com/microsoft/TypeScript/issues/62634#issuecomment-3993576433)
    * @shahanahmed86 asked to keep the issue open until repro steps are provided in [microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-3996641257)
    * @denis-migdal asked whether TypeScript has a principle to require explicit intent for potentially dangerous assignments in [microsoft/TypeScript#63206](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3995817875)
    * @denis-migdal asked if the contributing guidelines about regressions and reactions were originally present in [microsoft/TypeScript#63209](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3992087945)
    * @denis-migdal asked whether the team still reads old open issues in [microsoft/TypeScript#63209](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3993285780)

## Activity Summary

### [Issue microsoft/TypeScript#28985](https://github.com/microsoft/TypeScript/issues/28985) (Open, `Suggestion`, `Awaiting More Feedback`)

**Remote declaration file**

*Enable referencing and importing TypeScript declaration (.d.ts) files directly from remote URLs.*

 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-866751031) **kaaninel** said "Deno deals with this partially but afaik on typescript side there is no development so far. @BahaaZidan "
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-871908738) **pixelamit** asked how to share common logic via Single-spa utility and requested a working POC link
 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-1546494579) **alshdavid** described embedding client scripts via tamper monkey, lacking IDE type info for remote utilities, and suggested that the language server resolve remote .js files for JSDoc or adjacent d.ts type information
 * [later](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-3996676287) **arkhipovdenis** shared a tool called ts-remote for generating and fetching consolidated remote TypeScript definitions in microfrontend projects and invited feedback

### [Issue microsoft/TypeScript#41154](https://github.com/microsoft/TypeScript/issues/41154) (Open, `Suggestion`, `Awaiting More Feedback`)

**lib\.dom\.d\.ts: HTMLInputElement::type should be more specific than just 'string'**

*Update HTMLInputElement.type in lib.dom.d.ts to a union of valid HTML input type literals instead of a generic string.*

 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/41154#issuecomment-712273043) **tjjfvi** observed that the change only breaks assignments to specific string literals and would not be an impactful breaking change if the code never sets those values
 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/41154#issuecomment-713081329) **ArcticZeroo** suggested that most code sets input element type with a known literal rather than a generic string, noted common dynamic use cases like password toggling, and questioned how often unknown-string assignments occur
 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/41154#issuecomment-1177380271) **antsif-a** explained that defining `type: string` conflicts with React's JSX-specific `type` declaration and demonstrated a TSX compile error
 * [today](https://github.com/microsoft/TypeScript/issues/41154#issuecomment-3992534987) **skyfighteer** explained that reading the input property only returns predefined strings and that unknown values are auto-corrected to 'text'

### [Issue microsoft/TypeScript#43553](https://github.com/microsoft/TypeScript/issues/43553) (Open, `Suggestion`, `Awaiting More Feedback`)

**Different types based on visibility**

*Enable class properties and getters/setters to have distinct types depending on access visibility levels.*

 * [4.9 years ago](https://github.com/microsoft/TypeScript/issues/43553#issuecomment-814637677) **Jet132** suggested keeping order from most to least visible for consistency with function overloads and considered omitting type inference to align with TypeScript’s inference order
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/43553#issuecomment-2477426114) **Fasteroid** said "Hate to necro this, but I'd really love to see this too.  I'm running into Jet's exact problem with "dumb" getter/setters that shouldn't have to exist.  Any plans for this yet?"
 * [34 weeks ago](https://github.com/microsoft/TypeScript/issues/43553#issuecomment-3042042801) **denis-migdal** said "+1 this would indeed be a quite useful feature."
 * [today](https://github.com/microsoft/TypeScript/issues/43553#issuecomment-3993282168) **denis-migdal** discussed a similar feature and described two workarounds using identity functions or internal interfaces to handle readonly-to-mutable conversions

### [Issue microsoft/TypeScript#62634](https://github.com/microsoft/TypeScript/issues/62634) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: make hover tooltips more readable by showing the generic parameters names instead of their value \(in some cases\)\.\.**

*Show generic parameter names instead of their full types by default in hover tooltips to improve readability.*

 * (19 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62634#issuecomment-3874832301) **Ayoub-glitsh** praised the proposal’s DX improvements and offered to help implement a prototype
 * [today](https://github.com/microsoft/TypeScript/issues/62634#issuecomment-3993576433) **denis-migdal** thanked the respondent and suggested creating a VSCode extension using the TS language server as a proof of concept

### [Issue microsoft/TypeScript#63192](https://github.com/microsoft/TypeScript/issues/63192) (Open, `Bug`, `Domain: check: Type Circularity`)

**RangeError: Maximum call stack size exceeded when trying to infer type of a variable reassigned in a loop**

*TypeScript crashes with a maximum call stack size exceeded error when inferring types for a variable reassigned in a loop.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63192#issuecomment-3962608814) **RyanCavanaugh** provided a simplified reproducer that repros in TS7
 * (6 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Type Circularity`

### [Issue microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195) (Open, `Needs More Info`)

**Debug Failure: "No error for last overload signature" crash when CustomTypeOptions\.resources uses typeof on a large \(~10k line\) JSON file**

*TypeScript crashes with 'No error for last overload signature' when using typeof on a large JSON for i18next CustomTypeOptions.resources.*

 * created by **shahanahmed86**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-3967758768) **RyanCavanaugh** said "We need a concrete repro we can run ourselves"
 * **RyanCavanaugh** added label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-3996641257) **shahanahmed86** said "@RyanCavanaugh don't close issue, It will take me some time but I will share the concrete repro, honestly, super busy since the day I post this issue."

### [Issue microsoft/TypeScript#63206](https://github.com/microsoft/TypeScript/issues/63206) (Open, `Bug`, `Help Wanted`, `Domain: Error Messages`)

**Confusing error message \(2322\), should use \(2741\) and \(2322\) error message when this\["XXX"\] = {\.\.\.} has a missing \(or mispelled\) key or an incompatible value\.**

*Improve TypeScript error messaging for this['XXX'] assignments by distinguishing missing property errors (2741) from type mismatches (2322).*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3989336812) **denis-migdal** analyzed subclass property assignment under TS error 2322 and argued that no error should be raised
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3990439265) **MartinJohns** explained that accepting 'this.foo' assignments is an intentional unsoundness in TypeScript's type system and clarified that type assertions serve as escape hatches for this limitation
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3990552026) **denis-migdal** observed TS's differing treatment of the `this[XXX]` and generic cases and asked if the `this[XXX]` case could have more explicit messages
 * (today) **RyanCavanaugh** added labels `Help Wanted`, `Bug`, `Domain: Error Messages`, and set milestone to `Dormant`
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3995817875) **denis-migdal** asked whether TypeScript could enforce explicit casts to signal intent for potentially unsafe assignments

### [Issue microsoft/TypeScript#63207](https://github.com/microsoft/TypeScript/issues/63207) (Open)

**tsserver hangs indefinitely when inferring return type of class method that passes this to a function with deeply nested conditional return type**

*tsserver hangs when inferring a class method’s return type using remeda.pick without an explicit annotation due to circular type inference*

 * created by **kkirby**
 * [today](https://github.com/microsoft/TypeScript/issues/63207#issuecomment-3994012407) **RyanCavanaugh** explained that the hang was caused by an undetected type-checking cycle, linked to a relevant FAQ, and suggested annotating return types or using type assertions to unblock work

### [Issue microsoft/TypeScript#63209](https://github.com/microsoft/TypeScript/issues/63209) (Closed)

**Enable \`declare public readonly\` \+ \`protected\` declaration merge in classes**

*Enable `declare public readonly` + `protected` declaration merge in classes*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3991896628) **MartinJohns** disputed mention of opening new issues for triage and noted duplicates remained open
 * [today](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3991951606) **denis-migdal** stated not having seen any mention of requiring new issues for triage, noted possibly seeing a pinned issue by Ryan, and asked if old open issues are still watched by the team
 * [today](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3992026253) **MartinJohns** referred to issue #62827 about LS bug issues and confirmed that old issues remain generally watched by the team
 * [today](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3992087945) **denis-migdal** recalled docs advising to open new issues for regressions and use reactions instead of 'me too' and asked if they misremembered
 * [today](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3992313124) **nmain** asked if the issue referred to a specific TypeScript issue then acknowledged missing the prior response
 * [today](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3993141963) **RyanCavanaugh** requested closure of duplicate issue or clarification if different
 * [today](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3993285780) **denis-migdal** asked whether the team still reads old open issues
 * (today) **denis-migdal** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63209#issuecomment-3993321329) **RyanCavanaugh** confirmed that the team still reads old opened issues

### [Issue microsoft/TypeScript#63211](https://github.com/microsoft/TypeScript/issues/63211) (Closed, `Duplicate`)

**switch case does not create separate block scope for let declarations**

*The TypeScript compiler fails to enforce block scoping for let declarations in switch cases, allowing variables to leak across branches.*

 * created by **duanshixuan**
 * [later](https://github.com/microsoft/TypeScript/issues/63211#issuecomment-3996505247) **MartinJohns** said "Duplicate of #19503. Used search terms: switch let in:title"

