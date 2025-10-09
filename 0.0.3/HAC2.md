# Choices of Habit (CAH) - A Mental Health Regulatory System

The Choices of Habit System will be developed in three main stages:

1. Solidifying the format / system as tangible, fleshing out all the details, and adding any required metrics that may help further enhance CAH
2. Creating a well developed and structured quality of life **DESIGN PLAN** for the **user experience** that:
   1. Provides a simple input format for users to enter in their details to utilize CAH, this should not be bloated or over complicated, these steps should focus on the user experience, and user Quality of Life.
   2. Translates the users input above into the Structured CAH Diagram Syntax
   3. The goal is to have a reliable, structured syntax i can build the full system off of. If i can extract and produce consistent data in the CAH Syntax Format, I can **LATER** translate/parse it into a stunning visual representation.
3. Begin development of the CAH lexer/parsing system, starting with mocking up the directory with all required files, documents, modules, code, data.

## CAH Structured Visual Representation

A complex breakdown on the subjective defintion of Happiness.

- The current goal is to create a front to back format output with the principles, rules, and representation laid out for you below. Eventually this output format will be used to further develop the system into a more application oriented experience.

### Official Version (without any documented tags or explanations)

THIS DESIGN IS THE SINGLE SOURCE OF TRUTH FOR HOW THE FORMAT SHOULD OPERATE AND BE STRUCTURED

- USES PSEUDO CODE AND NAMING TYPES TO ENSURE SPACING CONSISTENCY

`CHOICE` = `CHO`
`ACTION` = `ATN`
`DECLARE` = `DEC`
`DEFINE` = `DEF`
`ABSOLUTE` = `ABT`
`essential` = `ent`
  `emotional` = `emo`
  `physical` = `phl`
`variable example` = `var`
`variable example two` = `vb2`

```css
          ┌── [CHO] ──┐
          │     ↓     │
          │   [ACT]   │
          │     ↓     │
          │   [DEC]   │
          │     ↓     │  
┌─(emo) ← ┤     ↓     ├ → (phl)─┐
│         │     ↓     │         │
│ {vrb  ↔ ┤  [{ABT}]  ├ ↔  vrb} │
│         │     ⇓     │         │
│ {vb2  → ┤    ↓⇓↓    ├ ←  vb2} │
└─────────┤    ↓⇓↓    ├─────────┘
          └─ <!DEF!> ─┘
```

### TRAINING VERSION (added flair and tags for documentation/training purposes only)

_THIS VERSION IS EXPLANITORY, IT IS NOT THE DIRECT SYNTAX, BUT AN EXPANDED CONTEXTUAL VERSION. SOME RULES MAY NOT BE STRICTLY FOLLOWED, THIS IS TO ENSURE THE FORMAT EXPLANATION IS UNDERSTOOD IN FULL._

- INCLUDES ADDITIONAL MARKERS FOR DOCUMENT TRAINING, ADDITIONAL MARKETS NOT INCLUDED IN FINAL SPEC:
  - LINE NUMBER GUTTER
  - A,B,C TAG IDEFNTIFIERS
- INCLUDES EXAMPLE DATA

```css
01  ┌────<A>         ┌── [CHO] ──┐
02  │  ┌──           │     ↓     │
03  │  │             │   [ACT]   │
04  │  │             │     ↓     │
05  │  │             │   [DEC]   │
06  │  │             │     ↓     │  
07 <B> ┤   ┌─(emo) ← ┤     ↓     ├ → (phl)─┐
08  │  │   │         │     ↓     │         │
09  │  │   │ {vrb  ↔ ┤  [{ABT}]  ├ ↔  vrb} │
10  │  │   │         │     ⇓     │         │
11  │  │   │ {vb2  → ┤    ↓⇓↓    ├ ←  vb2} │
13  │  │   └─────────┤    ↓⇓↓    ├─────────┘
13  │  └──           │    ↓⇓↓    │ 
                     └─ <!DEF!> ─┘
```

```css
01  ┌────<A>                   [CHOICE]
02  │  ┌──                         ↓
03  │  │                       [ACTION]
04  │  │                           ↓
05  │  │                      [STABILITY]
06  │  │                      ↓    ↓    ↓
07 <B> ┤    ┌────────(emotional    ↓    physical)─────────┐
08  │  │    ↓                ↑↑    ↓    ↑↑                ↓
09  │  │    {selfworth    ↔  [({WORKOUT})]   ↔  confidence}
11  │  │    ↓                      ⇓                      ↓
12  │  │    {placeholder  →       ↓⇓↓        ← placeholder}
13  │  └──                         ⇓        
15  └────<C>                 <!HAPPINESS!>
```

$$ A + B = C$$
Where:

- ($A$) = declare
- ($B$) = Dependency
- ($C$) = Definition

<!--
FOR DIAGRAM SIMPLICITY:
($A$): CHOICE (declare)
($B$): ACTION, STABILITY (DEPENDENCY)
($C$): HAPPINESS (DEFINITION)
-->

<!--
FOR ABSOLUTE TRUTH NAMING TYPE:
($A$): Definition
($B$): Dependency
($C$): declare (Declared Outcome)
-->

### Willingness and Goals

($A$) To plan a journey, we must first be willing to go on it;
($C$) Then decide where we want to go or what we want to do when we get there;
($B$) After we have decided and sorted the foundations, is usually when we begin planning the specifics

$A$ and $C$ are boring, easily overlooked, the hardest to decide for ourselves, and the hardest to recognize. $B$ on the other hand is usually much more specific, involves things in life more closely related to instant gratification, and requires no real critical or subjective perception. (For Example; _It is much more fun to plan the details or methods of a Vacation($B$){the casinos, the beaches, the amenities}, than it is to make the concious, realistic commitment if you can really afford it or not.`

How can we make any sort of Choice($A$), if we do not have any idea of what we want as an outcome for ourselves ($C$), How can others coordinate with your plan, if you dont know it yourself?

---

### `<A>` Definition

LineRef: 01

- Represents `Identifying Choice`.
  Choices have no dependencies, but directly influence:($B$),($C$)

### `<B>` Dependencies

LineRef: 02 -> 11

- Represents `Actionable Habits`.

Dependency:($A$)
Influences:($C$)

### `<C>` Declare (Declared Outcome)

LineRef: 13
Represents a declare (Outcome) of $A+B$.
**Dependency:($A$),($B$)**

## Diagram Choice Flow

The format flow is designed to identify and Define where Choices($A$), Depend on Habits($B$) that form the Outcome($C$)

### Momentum Characters

#### Single Line Arrows(`↓,↔,→,←`)

Represent the initial momentum or effect, as Methods and Dependencies get fulfilled, the arrows update with them. This identified a tangible visual cue of progress, without cluttering the diagram by compounding in the `⇓`

- Three single line arrow methods compound into a Double Line Arrow.

  - Usually manifests as differences or changes _others_ notice in you first
- Two Way Arrow (`↔`): Indicates that the depended upon Variables both share an Absolute, this requires the new absolute to be created on the same line.

#### Double Line Arrow(`⇓`)

Represents momentum shifting with compounding effects

- Usually manifests as differences you see in yourself over time
- Used as a compounding representative of the Single Line Arrow.

  - Three Single Line Arrows(`↓`) = One Double Line Arrow (`⇓`)

_(For Large Tasks: keep a small tally near the spine—e.g., `↓×3 ⇒ ⇓×1`—to audit compounding, without altering layout.)_

### Brackets

#### `[ ]` Square (Absolutes)

- Meant for Absolutes, they represent the spine of the framework, and influence all other aspects of the framework.

#### `( )` Round (Essentials)

- Used for foundational human needs. Mental(neurological) on the left, Physical(health) on the right. These may apply broadly with variables to both Square and Curly bracket variables.
- **Nesting is scope only (no type conversion).** For example, `[({WORKOUT})]` means the `{WORKOUT}` variable operates within the `(Essentials)` lanes and under the `[STABILITY]` Absolute; it does **not** become an Essential or an Absolute.

- The Ecosystem comes full circle When an Absolute branches into Essentials, creating a new absolute, that points back to its original branch.
  Example: `To increase Physical Health, Mental Stability: emotional and physical well being can be greatly enhanced by making the active choice to workout.`

```css
05  │  │                       [STABILITY]
06  │  │                       ↓    ↓    ↓
```

[05]: Stability is declared, pointing`↓` to its dependenices and methods below it, aswell as keeping the [Continuity Spine](all arrows correctly comopounded in the centre line as per the dependencies, absolutes, essentials.)
[06]: Left Dependency Arrow for essentials (emotional), `Continuity Spine`, Right Dependency Arrow for essentials (physical)

```css
07 <B> ┤             (emotional    ↓    physical)
08  │  │             ↓       ↑↑    ↓    ↑↑       ↓
09  │  │    {selfworth    ↔  {([WORKOUT])}  ↔    confidence}
11  │  │                           ⇓
```

[07]: Emotional and physical `(essentials)` are identified
[08]: Their dependencies are pointed to `{variables}` selfworth and workout with a two way arrow.
[09]: Two Way arrow is used to identify that a WORKOUT positively influences `(essential)` emotional and physical well being by directly identifying their dependency `{variables}`. All brackets are left open on the side closest to the `Continuity Spine`, this allows `WORKOUT` Choice to close all open brackets, essentially tying the ecosystem together.
[11]: Since the dependency(essentials) arrows add up to three in [({WORKOUT})], A double line arrow is used to avoid cluttering by the use of three single line arrows. To support this fact, and properly identify and link the ecosystem,
[12]: To show an example without the (essentials) having congruent absolutes and variables, i have provided a placeholder showing the additions of its two variables to the `Continuity Spine`, adding two single line arrows in addition to the existing double line arrow(that was compounded from the previous lines dependiencies joining three single line arrows)

#### `{ }` Curly (Variables)

Act as variables and dependencies to all other aspects of the framework. Directly influences the Outcome($C$), in some cases like when the Two Way Dependency arrow is used, it can effect Absolute ($B$).

## SPACING AND ALIGNMENT

- NON TRADITIONAL ALIGNMENT ON NEWLINES. SIMILAR TO A 'CENTRED' TITLE OR FORMAT, THIS FORMAT OPERATES MORE THAN ON A TOP DOWN BASIS, IT IS AN INTERCONNECTED ECOSYSTEM DESIGNED TO BE SIMPLE TO USE AND UNDERSTAND ON ITS SURFACE, BUT IN DEPTH AND COMPREHENSIVE IN ITS UNDERLYING MECHANICS.
- PROVIDES A VISUAL IDENTIFICATION AND UNINTENDED LOGGING THROUGH THE RECOVERY PROCESS.
- THE `Continuity Spine` ALLOWS PEOPLE TO SEE EXACTLY HOW MANY / WHAT CHOICES AND HABITS ARE LAID OUT IN THE PLAN, BUT POTENTIALLY WHAT WILL BENEFIT THEM MOST.
- THE COMPREHENSIVE STRUCTURE ALLOWS USERS TO TROUBLESHOOT IF THEIR HABITS DONT MANIFEST FROM THEIR CHOICES, ALLOWING THEM TO IDENTIFY KEY ASPECTS OR SPOTS THAT DID NOT WORK.

_**THERE IS ALLIGNMENT IN THE DIAGRAM IN THE CENTRE, LEFT, AND RIGHT**_:

- THIS IS BY DESIGN, TO OPERATE INTRISICALLY, AND ADAPTABLY, AS THE HUMAN BRAIN DOES. IT IS NOT DESIGNED TO MIMIC HUMAN NEUROLOGY OR PSYCHOLOGY, BUT TO PROVIDE A FAMILIAR STRUCTURE IN A CONSUMABLE MANNER.

---
