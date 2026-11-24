<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Session Summary: 20261116-1930](#session-summary-20261116-1930)
- [AIPREF](#aipref)
  - [Summary](#summary)
  - [Key Discussion Points](#key-discussion-points)
    - [Chair Introduction & Agenda Review](#chair-introduction--agenda-review)
    - [Issue Triage (`draft-ietf-aipref-attach`)](#issue-triage-draft-ietf-aipref-attach)
    - [Presentation: Attaching Preferences with Cross-Vendor Policy Tokens](#presentation-attaching-preferences-with-cross-vendor-policy-tokens)
    - [Technical Discussion on the Proposal](#technical-discussion-on-the-proposal)
  - [Decisions and Action Items](#decisions-and-action-items)
  - [Next Steps](#next-steps)
- [Session Summary: 20261119-1900](#session-summary-20261119-1900)
- [AIPREF](#aipref-1)
  - [Summary](#summary-1)
  - [Key Discussion Points](#key-discussion-points-1)
    - [1. Definition of Generative AI Model and "Synthetic" (Issue #217)](#1-definition-of-generative-ai-model-and-synthetic-issue-217)
    - [2. De Minimis Content Generation (Issue #231)](#2-de-minimis-content-generation-issue-231)
    - [3. Distinguishing Access and Use (Issue #167 / PR #252)](#3-distinguishing-access-and-use-issue-167--pr-252)
    - [4. Carrying Preferences and Model Distribution (Issues #193, #245 / PR #261)](#4-carrying-preferences-and-model-distribution-issues-193-245--pr-261)
    - [5. Caching, Embeddings, and Technical Transformations (Issue #246 / PR #253)](#5-caching-embeddings-and-technical-transformations-issue-246--pr-253)
    - [6. Structuring `ai-use` Preferences & User-Directed Inputs (Issue #249, PR #254, PR #258)](#6-structuring-ai-use-preferences--user-directed-inputs-issue-249-pr-254-pr-258)
    - [7. Accessibility Exceptions (Issue #257)](#7-accessibility-exceptions-issue-257)
  - [Decisions and Action Items](#decisions-and-action-items-1)
  - [Next Steps](#next-steps-1)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



**NOTE**: _This is a non-normative, AI-generated summary supplied only for convenience; it does not necessarily represent an accurate record of the meeting. See the minutes for the authoriative record. See [the source](https://ietfminutes.org/) for more information._



# Session Summary: 20261116-1930

# [AIPREF](../wg/aipref.html)

## Summary

The AIPREF working group met at IETF 127 to discuss mechanisms for attaching AI usage preferences to web content, focusing on [`draft-ietf-aipref-attach`](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/). The chairs opened the meeting with an agenda review and a triage of open GitHub issues. Kevin Kelly presented a proposal and pull request (#260) suggesting syntactic changes to how preferences are expressed in `robots.txt` via cross-vendor policy tokens, citing compatibility edge cases in existing `robots.txt` parsers. The working group discussed the trade-offs of overloading the `User-Agent` field versus adding new line types, the extent of potential parser breakage, and alternative options such as defining a new structured format. A design team was agreed upon to analyze parser behavior and evaluate attachment options ahead of an interim meeting planned for February.

---

## Key Discussion Points

### Chair Introduction & Agenda Review
- **Chairs**: Mark Nottingham, Suresh Krishnan
- **Slides**: [Chair slides](https://datatracker.ietf.org/meeting/127/materials/slides-127-aipref-chair-slides-00)
- The chairs reminded participants of the IETF Note Well guidelines and noted that the Monday session focused exclusively on preference attachment ([`draft-ietf-aipref-attach`](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/)), while the Thursday session would cover vocabulary ([`draft-ietf-aipref-vocab`](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/)).

### Issue Triage ([`draft-ietf-aipref-attach`](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/))

- **Issue #223 (Propagation of preferences input)**:
  - Raised by Eric Rescorla regarding text governing how servers retain and propagate preferences across state-changing HTTP requests (e.g., `PUT` requests answering subsequent `GET` requests).
  - Martin Thompson noted that recent draft updates softened the text from rigid requirements to permissive guidance regarding server capabilities.
  - Eric Rescorla agreed that the updated text was acceptable. The issue was closed.

- **Issue #193 (Carrying preferences with assets)**:
  - Martin Thompson explained that the core language for tracking preferences alongside assets during processing and training is primarily being refined in [`draft-ietf-aipref-vocab`](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/). Once that text stabilizes, alignment with [`draft-ietf-aipref-attach`](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/) will be re-evaluated.

- **Issue #166 (Non-enforceability provision alignment)**:
  - Joe Salowey and Mark Nottingham reviewed the status of enforceability statements across the two core drafts. Section 3.2 of [`draft-ietf-aipref-attach`](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/) contains the current preferences application guidance. The issue was closed with the understanding that document alignment will continue to be monitored.

- **Issue #103 (Content-Usage in `robots.txt` structured field format)**:
  - Discussion deferred due to author absence and overlap with the subsequent presentation on `robots.txt` parsing.

---

### Presentation: Attaching Preferences with Cross-Vendor Policy Tokens

- **Presenter**: Kevin Kelly
- **Slides**: [Attaching Preferences with Cross-Vendor Policy Tokens](https://datatracker.ietf.org/meeting/127/materials/slides-127-aipref-sessa-attaching-preferences-with-cross-vendor-policy-tokens-00)
- **Overview & Motivation**:
  - Kevin Kelly detailed empirical testing across real-world `robots.txt` files and open-source/proprietary parser implementations.
  - Highlighted parser discrepancies under RFC 9309 rules: when encountering unknown line types (such as a hypothetical `Content-Usage:` header) or empty group definitions, deployed parsers behave inconsistently. Some parsers break group scoping, alter fallback behavior, or silently change access controls for traffic management.
- **Proposed Approach (PR #260 / `rep-namespaces`)**:
  - Proposes carrying preferences using reserved namespace-label pairs within the `User-Agent` record line (e.g., `User-Agent: __usage_ai-train`), avoiding the introduction of new top-level `robots.txt` line types.
  - Reserves the `__` prefix to prevent collisions with valid user-agent product tokens.
  - Defines explicit rules for unmatched paths, wildcard fallbacks, and precedence to prevent site operators from unintentionally opting into positive training preferences.
  - Mentioned a potential alternative (`rep2` / `ai.txt` format): defining a clean, structured JSON equivalent to `robots.txt` to bypass legacy parsing bugs entirely, though acknowledging higher deployment friction.

---

### Technical Discussion on the Proposal

- **User-Agent Overloading vs. Semantics**:
  - Ted Hardie and Nick Doty raised concerns about using the `User-Agent` position for policy tokens. Overloading `User-Agent` could lead site operators to confuse preference policy tokens with actual request user-agent headers, complicating per-vendor configuration and logging.
  - Will Hawkins and Watson Ladd noted that repurposing the `User-Agent` field creates semantic confusion for human operators reading `robots.txt` files, even if it avoids parser errors for automated tools.
- **Parser Failure Modes & Empirical Risk**:
  - Eric Rescorla emphasized the need to quantify how many unmodified, deployed parsers actually break or misbehave when encountering the existing [`draft-ietf-aipref-attach`](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/) mechanism (e.g., `Content-Usage:` lines). If the failure rate is low or easily mitigated via authoring guidelines, complex syntactic workarounds may be unnecessary.
  - Tess Rinearson supported making architectural decisions based on empirical data regarding common parser failures rather than theoretical edge cases.
- **Simplification & Compatibility**:
  - Martin Thompson noted that Kevin Kelly’s findings highlight real parsing risks. However, he suggested investigating whether strict authoring guidance for `robots.txt` could achieve the same compatibility goals without introducing full cross-vendor policy token syntax.
- **Vocabulary Scope**:
  - Rüdiger Martin confirmed that any chosen attachment mechanism must fully express all preference categories defined in [`draft-ietf-aipref-vocab`](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/). Kevin Kelly confirmed the proposed namespace syntax maps directly to the working group's vocabulary draft.

---

## Decisions and Action Items

1. **Closed Issues**:
   - Issue #223 on [`draft-ietf-aipref-attach`](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/) closed following document updates.
   - Issue #166 on [`draft-ietf-aipref-attach`](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/) closed.

2. **Design Team Formation**:
   - A design team was established to analyze deployed `robots.txt` parser behavior, assess potential failure modes of preference attachment mechanisms, and evaluate proposed solutions (including PR #260 and potential alternative formats).
   - **Coordinator**: Kevin Kelly.

---

## Next Steps

- **Design Team Execution**: Kevin Kelly will gather interested participants to collect empirical parser data and evaluate attachment options.
- **Interim Reporting**: The design team will present its findings and recommendations prior to or during the planned working group interim meeting in February.
- **Upcoming Session**: The Thursday session at IETF 127 will be devoted to [`draft-ietf-aipref-vocab`](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/).

# Session Summary: 20261119-1900

# [AIPREF](../wg/aipref.html)

## Summary

The AIPREF Working Group met to discuss open issues on [draft-ietf-aipref-vocab](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/) (A Vocabulary For Expressing AI Usage Preferences) and review progress on [draft-ietf-aipref-attach](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/) (Associating AI Usage Preferences with Content in HTTP). Mark Nottingham presented the [Chair slides](https://datatracker.ietf.org/meeting/127/materials/slides-127-aipref-chair-slides-00) to frame the agenda, open pull requests, and upcoming working group milestone schedules.

Key discussions focused on removing redundant terms in vocabulary definitions (Issue #217), distinguishing asset access from use (PR #252), conveying preferences through asset transformations and model distribution (Section 3.3 / PR #253), structuring the `ai-use` preference category (Issue #249 / PR #258), and incorporating accessibility carve-outs (Issue #257).

---

## Key Discussion Points

### 1. Definition of Generative AI Model and "Synthetic" (Issue #217)
- The group discussed whether to keep the word "synthetic" in the definition of a generative AI model ("used to generate synthetic content...").
- **Arguments against**: Martin Thomson, Chris Needham, Nate Hake, and Pablo González argued that "synthetic" is redundant alongside "generate", invites unnecessary ambiguity regarding derived or mixed content, and creates loopholes around regurgitated data.
- **Arguments for**: Kevin Kelley supported keeping the term as evocative of substitutive AI-generated content.
- **Discussion**: Eric Rescorla requested specific examples where removing or keeping "synthetic" alters the operational boundary of the definition. Pablo González and Eric Rescorla noted OCR or automated processing examples.
- **Outcome**: The group leaned toward removing "synthetic" unless proponents provide concrete examples/definitions justifying its inclusion before the next meeting.

### 2. De Minimis Content Generation (Issue #231)
- Raised previously by Erin Simon. With no further objections or edits proposed, the issue was marked for closure, with the option to re-open if new concerns arise.

### 3. Distinguishing Access and Use (Issue #167 / PR #252)
- Martin Thomson presented updates to PR #252 clarifying the distinction between asset acquisition/access and asset usage.
- Eric Rescorla and Chris Needham supported merging the PR.
- **Outcome**: PR #252 was approved to merge so the working group can review the updated text in context.

### 4. Carrying Preferences and Model Distribution (Issues #193, #245 / PR #261)
- The group reviewed Section 3.3/3.4 regarding downstream requirements for entities distributing assets or models trained on assets with expressed preferences.
- Timid Robot, Brad Silver, and Farzaneh Badii discussed crawler vs. trainer responsibilities and ensuring preferences remain attached across redistribution chains.
- Lila Bailey and Mark Nottingham emphasized that specifications cannot bind non-conforming third parties, but conforming actors must preserve preferences.
- **Outcome**: Remove the "at risk" note in Section 3.3 and merge PR text for further review in-tree.

### 5. Caching, Embeddings, and Technical Transformations (Issue #246 / PR #253)
- Martin Thomson introduced PR #253, which specifies that technical format transformations (e.g., embeddings, text simplifications) must retain original preference information.
- **Feedback**:
  - Achim suggested explicitly covering asset excerpts/chunks.
  - Pedro noted distinctions between intermediate crawling/extraction and model fine-tuning.
  - Lila Bailey cautioned against using the legal term "transformed" due to US copyright fair-use implications, suggesting terms like "converted" or "derived".
- **Outcome**: Editors will update PR #253 to use non-legal terminology (e.g., "converted") and merge for further refinement.

### 6. Structuring `ai-use` Preferences & User-Directed Inputs (Issue #249, PR #254, PR #258)
- Paul Keller presented a framework outlining three structural options for the `ai-use` vocabulary category:
  1. Single `ai-use` category covering all system and user inputs.
  2. `ai-use` category with specific user-initiated exclusions.
  3. Splitting into two distinct categories: System-initiated AI use (`AI system use`) vs. User-directed/provided inputs (`AI user-directed`).
- **Discussion**:
  - Nate Hake, Brad Silver, Achim, and Timid Robot favored Option 3, arguing that content creators require a full spectrum of granular preference expressions to choose how content is used by automated systems versus directly provided by end users.
  - Alissa Cooper and Martin Thomson advocated focusing on defining `AI system use` first via PR #258 to establish a stable baseline.
  - Farzaneh Badii expressed concerns that restricting user-directed AI inputs could harm end users, open-source developers, and access to content.
  - Tess, Erin Simon, and Chris Needham discussed technical nuances in PR #258, noting that over-indexing on raw URLs or direct byte uploads might overlook general user prompt intent or create UI friction. Francesco Moretto emphasized line drawing based on existing user entitlement rather than format/bytes.
- **Outcome**: Working group consensus leaned toward developing Option 3 (splitting system-initiated use and user-directed inputs). Editors will incorporate PR #258 as a working baseline draft with explicit caveats that it lacks final consensus.

### 7. Accessibility Exceptions (Issue #257)
- Farzaneh Badii highlighted ongoing work in W3C regarding AI accessibility (e.g., text-to-speech, automated translation, assistive format adjustments) and proposed adding an overarching accessibility carve-out in the draft introduction.
- Timid Robot supported the initiative.
- **Outcome**: Farzaneh Badii will post proposed introductory carve-out language on GitHub Issue #257 for list discussion.

---

## Decisions and Action Items

1. **Issue #217 ("Synthetic")**:
   - **Decision**: Pending concrete examples from proponents showing why "synthetic" is necessary, the word will be removed from the generative AI definition in the next draft revision.

2. **Issue #167 / PR #252 (Distinguishing Access and Use)**:
   - **Decision**: Merge PR #252 into [draft-ietf-aipref-vocab](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/).

3. **Issue #245 / Section 3.3 (Model Distribution)**:
   - **Decision**: Remove the "at-risk" marker in Section 3.3 while continuing to refine compliance and RFC 2119 wording.

4. **Issue #246 / PR #253 (Embeddings and Format Conversions)**:
   - **Action Item**: Editors to replace legal terms (e.g., "transformed") with technical terms ("converted" / "derived") and merge PR #253.

5. **Issue #249 / PR #258 (`ai-use` Category Structure)**:
   - **Decision**: Proceed with Option 3 (decoupling system-initiated use from user-directed input). Incorporate PR #258 text into the draft as an initial working framework marked without consensus.

6. **Issue #257 (Accessibility Carve-out)**:
   - **Action Item**: Farzaneh Badii to post proposed introductory text on GitHub Issue #257.

---

## Next Steps

- **Virtual Interim Meeting**: A virtual session will be scheduled in December to focus specifically on refining the definition of `ai-use` and user-directed/provided inputs.
- **Hybrid Interim Meeting**: A 4-day hybrid interim meeting is tentatively planned for early February (location TBD, tentatively Tokyo). The format will feature structured half-day plenary sessions and un-scheduled breakout design time.
- **WGLC Progress**: Chairs emphasized the need to finalize core text in [draft-ietf-aipref-vocab](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/) and [draft-ietf-aipref-attach](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/) to begin formal working group consensus calls.