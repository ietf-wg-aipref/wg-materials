<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Session Summary: 20251103-2200](#session-summary-20251103-2200)
  - [Summary](#summary)
  - [Key Discussion Points](#key-discussion-points)
    - [Working Group Context and Editor's Update (Martin Thomson)](#working-group-context-and-editors-update-martin-thomson)
    - [Top-Level Category: Automated Processing](#top-level-category-automated-processing)
    - [Foundation Model Production](#foundation-model-production)
    - [Search (previously nested under AI output)](#search-previously-nested-under-ai-output)
    - [AI Output](#ai-output)
  - [Decisions and Action Items](#decisions-and-action-items)
  - [Next Steps](#next-steps)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



**NOTE**: _This is a non-normative, AI-generated summary supplied only for convenience; it does not necessarily represent an accurate record of the meeting. See the minutes for the authoriative record. See [the source](https://ietfminutes.org/) for more information._



# Session Summary: 20251103-2200



## Summary

The AIPREF working group met to review and discuss the latest revisions to the core drafts, which were developed following extensive discussions at the Zurich meeting. The primary goal was to gather preliminary feedback on the new conceptual framework and definitions, particularly for "Foundation Model Production," "AI Output," "Search," and the top-level "Automated Processing" category. It was acknowledged that the working group is effectively "back to square one" after a failed WG Last Call, and new milestones are set for August 2026 to reflect ongoing uncertainties. Discussions revealed significant contention and areas requiring further clarification for all proposed terms, with a notable consensus reached to un-nest "Search" from "AI Output."

## Key Discussion Points

### Working Group Context and Editor's Update (Martin Thomson)

*   **Current Status:** The working group experienced strong disagreements after the Brussels meeting, leading to a failed WG Last Call and a reset of milestones to August 2026.
*   **Zurich Discussions & New Drafts:** Recent drafts attempt to reflect extensive discussions from the Zurich meeting, but are considered "tentative ideas" for preliminary feedback. The goal is to determine if this new direction is fruitful for ongoing work.
*   **Previous Model Challenges:** The prior model, with categories like "AI training" and "generative AI training," faced issues due to differing understandings of "search" and the extent of AI involvement. Search providers indicated they not only use but also train models in the process of generating search results.
*   **New Conceptual Framework:**
    *   "AI training" and "generative AI training" are collapsed into "producing a foundation model."
    *   "Search" is now distinct, alongside a new "AI output" category, though its nesting within "AI output" is currently uncertain.
*   **Four Major Terms for Discussion:** "Foundation Model Production," "Search," "AI Output," and the top-level "Automated Processing."

### Top-Level Category: Automated Processing

*   This overarching category remains highly contested.
*   A key point of disagreement revolves around its role in addressing "unexpected uses" or "unintended consequences." Some desire a top-level category to explicitly allow or disallow unknown future uses, while others view this as problematic.

### Foundation Model Production

*   **Intent:** To focus on the *output* (the foundation model itself) rather than internal system processes, avoiding the difficult distinction between simple machine learning and "AI training." Foundation models are generally better understood than "generative AI training."
*   **Scope:** There was a question of whether "AI output" combined with "AI model production" covers the entire universe of AI systems. The editor indicated it covers much of the space but could not definitively guarantee completeness.
*   **"Fine-tuning" Definition:** The current definition includes "fine-tuning," but this term is ambiguous. It encompasses various techniques (e.g., prompt engineering, LoRA) and is not clearly understood or uniformly applied.
*   **Reusing Existing Definitions:** A suggestion was made to leverage widely agreed-upon definitions for foundation models where possible, noting variations primarily in parameter count or specific training methods (e.g., self-supervised learning).
*   **"Why" vs. "How":** Ted Hardy emphasized focusing on *why* a user would express a preference (e.g., for citations, answers, or interactions) in understandable terms, rather than complex technical "hows" of model creation.
*   **Declarant Clarity:** Fars highlighted the need for clarity on who the "declarant" is (e.g., WordPress, social media platforms) and the transparency required when preferences are declared on behalf of others.
*   **Preference & IP:** Timit Robot cautioned against tying AI preferences directly to intellectual property status, as it might limit efficacy or duplicate existing legal frameworks.

### Search (previously nested under AI output)

*   **Original Intent:** "Search" was initially included as an exception to prevent general AI restrictions from inadvertently disabling search, a widely accepted application.
*   **Nesting Controversy:** Strong feedback indicated that nesting "Search" under "AI Output" is confusing and illogical, given the broad scope of "AI output" and the distinct nature of search expectations.
*   **User Understanding:** Meredith Jacob noted that while "search" is a concept users understand, they primarily care about *why* a tool is used (e.g., for competitive/substitutional purposes vs. assistive uses), not the tool itself. She questioned the ability to distinguish these uses, especially with open-weight models.
*   **Definition Challenges:** Mikaela argued that the term "search" itself is problematic due to continuously evolving user expectations. The current definition's focus on "reference and link back" and "verbatim excerpts" was highlighted as key, but the "verbatim excerpts" point was debated as still potentially enabling substitutive use (Brad).
*   **Alternative Categorization:** Mallory Nodal suggested a broader "derivative works" category that would encompass search, allowing for other forms of content reuse beyond traditional search.
*   **Granularity:** Alyssa noted that Krishna's draft offered more granular categories (indexing, retrieval, display length, image, video, exact match) which could address some of the current definition's shortcomings. The working group's charter scope for such detail was a consideration.
*   **Clarity for Creators:** Nate Haig, a small blogger, found the proposed definition (especially the verbatim excerpt bullet) useful and explainable to other creators, seeing it as addressing the "fair exchange" concern by ensuring traffic returns to the source.
*   **Pro-social Uses:** Victoria Noble emphasized that current definitions risk sweeping up pro-social uses (e.g., accessibility, translation) that content producers would likely want to authorize.

### AI Output

*   **Core Idea:** To focus *solely* on the observable output of systems, independent of their internal AI operations.
*   **"Automated Clients" Ambiguity:** Aaron Simon pointed out that referring to "outputs presented to automated clients" reintroduces the complexity of internal system operations, which the definition aimed to avoid. He argued it should be limited to human users.
*   **Agentic Browsing/System Boundaries:** A significant challenge is defining where the "obligation" from a preference ends when content is consumed by an AI agent or passed between systems across administrative domains. It's unclear how downstream systems can ensure compliance with upstream preferences.
*   **Conceptual vs. Nitpicking:** Ecker and Roberta raised concerns that the current problems might be fundamental conceptual design issues rather than mere linguistic nitpicking, especially given the industry's move towards autonomous AI agents with little human intervention and the resulting liability questions.
*   **Broadness and Clarity:** Alain described the definition as "very broad and confusing," particularly the sentence regarding outputs presented to "human users and outputs da-da-da-da-da."
*   **Use Cases for Clarity:** Alyssa suggested using concrete use cases to distinguish between "human outputs" and "organizational boundary" concerns, for example, regarding internal SaaS company operations.
*   **Testing Compliance:** The question of "what tests would we apply to determine if a preference was being followed" was debated. While the group shouldn't prescribe specific tests, the editor clarified the intent was for a system operator to internally determine compliance for a given system and preference.
*   **Output vs. Internal Use:** Alyssa also questioned if the definition implies that an asset could be used in an AI system for *any purpose other than generating outputs*, and if the group is comfortable with that implication.
*   **Policy vs. Technical:** Ted Hardy and Victoria Noble reiterated that balancing the costs/benefits of preferences for users vs. publishers, and addressing issues like substitutive use, are fundamentally policy or legislative tasks, not suitable for a technical standards body. They stressed that this document isn't meant to be a legislative tool.
*   **Penultimate Paragraph:** The paragraph discussing "model training" within the AI output category was questioned, especially given the decision to un-nest search. It was suggested it might need removal or significant re-evaluation.

## Decisions and Action Items

*   **Decision:** The "Search" category will be separated from "AI Output" and will not be nested.
*   **Action Item:** The chairs will coordinate on compiling a set of concrete use cases to test the proposed definitions against, drawing on existing discussions and community input.
*   **Action Item:** Editors and chairs will continue to review Krishna's draft and the existing issues list to ensure all relevant concepts are considered and captured.
*   **Action Item:** Participants are encouraged to continue discussions on the mailing list, especially for brainstorming and refining the draft terms.

## Next Steps

*   The working group will reconvene to discuss the "Automated Processing" (top-level) category.
*   Further refinement of "Foundation Model Production," "AI Output," and "Search" definitions will proceed, incorporating feedback received in this meeting.