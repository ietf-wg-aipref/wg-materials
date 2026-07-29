<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Session Summary: 20260724-1200](#session-summary-20260724-1200)
- [AIPREF](#aipref)
  - [Summary](#summary)
  - [Key Discussion Points](#key-discussion-points)
    - [Working Group Status and Meeting Schedule](#working-group-status-and-meeting-schedule)
    - [PR 213: Section 3.2 (Applicability and Scope of Preferences)](#pr-213-section-32-applicability-and-scope-of-preferences)
    - [PR 211: AI Training Definition](#pr-211-ai-training-definition)
    - [AI Use and Inference Category](#ai-use-and-inference-category)
    - [Machine Readability](#machine-readability)
  - [Decisions and Action Items](#decisions-and-action-items)
  - [Next Steps](#next-steps)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



**NOTE**: _This is a non-normative, AI-generated summary supplied only for convenience; it does not necessarily represent an accurate record of the meeting. See the minutes for the authoriative record. See [the source](https://ietfminutes.org/) for more information._



# Session Summary: 20260724-1200

# [AIPREF](../wg/aipref.html)

## Summary

The AIPREF Working Group met during IETF 126 to discuss updates to the AI usage preferences vocabulary, focusing on `draft-ietf-aipref-vocab`. The discussion centered around refining the scope and applicability language in Section 3.2 (via Pull Request 213), clarifying the "AI Training" definition (via Pull Request 211), and exploring the definition of an "AI Inference" or "AI Use" category. Additionally, the group discussed plans for upcoming interim meetings and introduced a new individual submission on machine readability.

## Key Discussion Points

### Working Group Status and Meeting Schedule
The chairs (Mark Nottingham and Suresh Krishnan) reviewed the working group's progress, referencing the [Chair slides](https://datatracker.ietf.org/meeting/126/materials/slides-126-aipref-chair-slides-00). They noted that significant progress has been made during interim meetings, such as the recent one in Toronto. 
* **Future Interims**: An interim meeting is scheduled for late August/early September in London. The chairs are also planning future interims in October and potentially January to maintain momentum.

---

### PR 213: Section 3.2 (Applicability and Scope of Preferences)
The working group discussed PR 213, which aims to pare down the scope of Section 3.2 in `draft-ietf-aipref-vocab` to avoid overstepping into policy or legislative domains while clearly outlining the specification's limitations.

* **Draft Text & Policy Concerns**: Timid Robot noted that the impact of this work intersects with existing legislation, making it critical to clarify that this document is purely a technical protocol definition. Glenn Deen expressed a desire to keep the text free of policy-loaded terms like "legal," "ethical," or "public interest" to prevent misinterpretation and "cherry-picking" of words downstream.
* **Alternative Proposals**: 
  * Sebastian Posth proposed alternative text for the final paragraph:
    > "An entity that receives usage preferences has a choice whether to follow those preferences. This specification does not determine how that choice is made. Whether and under which circumstances a preference is followed is outside the scope of this specification."
  * Martin Thomson proposed a slightly tighter alternative:
    > "An entity that receives usage preferences has a choice whether to follow those preferences. External factors could influence that decision, but the decision itself is outside the scope of this document."
* **Enforcement Nuances**: Mirja Kühlewind raised concerns that the first bullet point in the PR (touching on enforcement) might erroneously imply that an enforcement mechanism *should* exist, and suggested that the text should more clearly state that ignoring preferences under valid circumstances is not necessarily misconduct. Eric Rescorla agreed that conformance simply means properly parsing the vocabulary; what an implementation does after parsing is entirely out of scope.
* **Consensus Path**: The group agreed that the discussion was converging on editorial nuances rather than fundamental disagreements. The discussion will continue on the mailing list to finalize the text.

---

### PR 211: AI Training Definition
Kevin Kelley presented PR 211, which introduces refinements to the training definition in `draft-ietf-aipref-vocab`.

* **Learned Parameters**: The proposal replaces the phrase "common parameters" with "learned parameters" (e.g., weights and biases modified during training) to be more technically precise. Nate Hake expressed concern that "learning" is a loaded term, but Kevin Kelley clarified that "learned parameters" has a distinct technical definition separating training from inference-time context (like context window operations).
* **Removal of "Made Available to Use"**: Kevin Kelley removed this phrase from the PR, noting that concerns regarding how preferences persist with a model after training are better handled at the binding/attachment layer rather than the vocabulary definition itself. Farzaneh Badiei supported this change, noting it addressed her earlier concerns about the definition being too broad.
* **"Synthetic" Content**: Kevin Kelley retained the term "synthetic content" to capture model-produced output that serves as a substitute. Martin Duke asked if this would exclude non-synthetic use (e.g., serving unmodified photos), which he suggested would make the term "synthetic" highly relevant. Glenn Deen recommended defining these terms of art clearly in a terminology section to ensure the document's longevity.

---

### AI Use and Inference Category
The group revisited the ongoing debate regarding how to define an "AI Use" or "AI Inference" category, referring to the historical proposals tracked on the WG wiki.

* **Nate Hake's Proposal**: Nate Hake proposed an "AI Inference" definition:
  > "AI-Inference: The act of using an asset for inference by an AI model that can generate content in one or more modalities (text, image, audio, etc...). Inference means all use beyond the production or refinement of an AI model."
  Under this model, any use by a generative AI system beyond the training boundary would fall under inference, allowing asset owners to express a clean preference.
* **User-Contributed vs. Autonomous Fetching**: 
  * Paul Keller and Sebastian Posth pointed out a critical distinction between two scenarios: when an AI model autonomously fetches content versus when an end-user directly uploads/inputs an asset (e.g., pasting a URL or uploading a PDF for translation). 
  * Paul Keller suggested that the vocabulary should allow expressing these as separate, addressable preferences, as some stakeholders want to allow user-driven uploads but prohibit autonomous crawling.
  * Farzaneh Badiei strongly objected to applying preferences to user-uploaded content, arguing it amounts to content moderation, harms consumers, limits open-source developers, and restricts general utility features like translation.
  * Eric Rescorla noted that trying to enforce preferences on user-provided content is practically ineffective, as users can easily strip preferences from assets before uploading them.
  * Timid Robot supported having the broad ability to express preferences across the entire scope of AI usage and planned to submit a proposal to address these boundaries.

---

### Machine Readability
Thom Vaughan introduced `draft-vaughan-machine-readability-00` (co-authored with Hank Birkholz), which attempts to define "machine readability" as referenced in various policy and technical documents. He requested feedback on the mailing list as they work toward a `-01` revision to make the definitions more robust.

---

## Decisions and Action Items

* **PR 213**: The chairs directed the working group to the mailing list to finalize the choice-of-preference text in Section 3.2, choosing between the proposals from Sebastian Posth and Martin Thomson.
* **PR 211**: The group will continue list discussion on the terminology of "learned parameters" and the use of the term "synthetic."
* **AI Inference / AI Use**: Nate Hake and Paul Keller agreed to collaborate on a unified proposal that potentially splits the AI Inference category into distinct, addressable modes (such as autonomous fetching vs. user-provided input) to address outstanding concerns.
* **Issue Cleanup**: The chairs will conduct a review of the GitHub issue tracker to close out obsolete issues or combine related ones ahead of the next interim meeting.

## Next Steps

* The working group will focus on achieving asynchronous consensus on PR 213 and PR 211 via the mailing list.
* The next formal session of the working group will be the interim meeting in London (scheduled for late August/early September). Agenda planning will begin in the coming weeks.