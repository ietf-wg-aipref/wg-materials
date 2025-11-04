

**NOTE**: This is a non-normative, AI-generated summary supplied only for convenience; it does not necessarily represent an accurate record of the meeting. See the minutes for the authoriative record. See [the source](https://ietfminutes.org/) for more information.


# Session Summary: 20251103-2200



## Summary

The AIPREF Working Group met to discuss the current status of its documents and gather preliminary feedback on newly published drafts, which attempt to address issues raised during a failed Working Group Last Call (WGLC). Milestones have been extended to August 2026, reflecting the significant work still needed to reach consensus. The session focused on an editor's update and detailed discussion of four key vocabulary terms: Foundation Model Production, Search, AI Output, and the top-level "Automated Processing" category. No final decisions were made, with the meeting serving as a starting point for further deliberation. Key themes included the clarity and scope of definitions, the challenges of distinguishing between different AI uses, and the need for definitions understandable to end-users.

## Key Discussion Points

### General Context and Status

*   The previous Working Group Last Call (WGLC) for drafts failed due to strong disagreements within the group.
*   Working Group milestones have been updated to August 2026, reflecting the significant uncertainties and progress needed for consensus.
*   New drafts were recently published, incorporating discussions from the Zurich meeting, but these are tentative and require preliminary feedback.
*   This meeting aimed to gauge if the new direction is fruitful, rather than making final decisions.

### Foundation Model Production

*   **Intent:** The goal was to shift focus to the *output* (the foundation model itself) rather than the internal processes of "AI training," which proved difficult to define. Foundation models are generally well-understood as having generative capabilities.
*   **Concerns:**
    *   The definition of "producing a foundation model" currently includes "fine-tuning," which is an unclear term with various interpretations (e.g., prompt engineering vs. weight changes). There was a call to consider fine-tuning separately.
    *   A broad category might be too encompassing for content owners wishing to express specific preferences about the use of their content in fine-tuning applications.
    *   The overall scope: Is the combination of "Foundation Model Production" and "AI Output" intended to cover all possible uses of AI systems?
*   **Suggestions:**
    *   Utilize widely-agreed-upon external definitions for "foundation model" where possible, noting minor variations.
    *   Develop a concrete set of "use cases" to test the proposed definitions against, to ensure they address real-world scenarios.
    *   Consider the user's *intent* for expressing preferences rather than focusing solely on the technical *how*.
    *   Explore dimensional approaches (e.g., data aggregation, preservation of context) instead of strict taxonomies for defining uses.
    *   Crawlers need to be able to self-categorize their activities within these definitions.
    *   The discussion on declarant clarity (e.g., social media platforms declaring preferences on behalf of users) was noted for future discussion under "attachment."

### Search (Tentatively named "Exact Text Match" / "Laterhosen")

*   **Historical Context:** `search` was introduced early on to specifically allow search engines to operate, as disallowing AI training could inadvertently disable search. Modern search applications increasingly leverage foundation models.
*   **Proposed Structure:** The current draft tentatively nests `search` as a subcategory of `AI Output`, defined by two conditions: presenting a reference to the asset's location and using verbatim excerpts.
*   **Key Issues & Consensus:**
    *   There was a strong, widespread consensus that **nesting `search` under `AI Output` is problematic and should be removed.** It complicates explanation for declarants and conceptually separates a specific, long-standing use case from a broader, newer category.
    *   The term "search" itself is ambiguous due to its constantly evolving nature and differing user expectations of what "search" entails (e.g., 10 blue links vs. AI overviews).
    *   The "verbatim excerpts" requirement was criticized for potentially still leading to "substitutive use" outcomes if the excerpt is too long or crucial.
    *   Concerns were raised about how to define "search" in a way that allows for essential functionality (like sending traffic back to original sites) while preventing unwanted substitutive uses, especially for small content creators.
*   **Suggestions:**
    *   Use more precise terms like "citation search," "indexing search," or "referencing search" to clarify intent.
    *   Consider a broader "derivative works" category that would encompass `search` but not be limited to it.
    *   Explore concepts from Krishna's draft, which includes more granular categories like indexing, retrieval, display length, image, video, and exact match.
    *   Definitions should facilitate a "fair exchange" where content usage leads to appropriate returns (e.g., user traffic).
    *   Ensure definitions do not inadvertently prevent socially beneficial uses such as accessibility features or translation.

### AI Output

*   **Intent:** This new category aims to focus on the *observable output* of a system, regardless of its internal AI operations, to address concerns about substitutive content creation.
*   **Major Challenges & Confusion:**
    *   **"Automated Clients":** The draft's inclusion of "outputs presented to all automated clients" was seen as reintroducing complexities of internal system operations, contradicting the intent to focus solely on external output.
    *   **"Presented to a Human":** The definition struggles with the concept of "human user" in the age of agentic browsing, where AI agents consume content and interact with systems. It's unclear how a system can determine if the recipient is a human or an AI agent.
    *   **System Boundaries:** It's unclear how to delineate the "output" stage from internal processing, especially in complex, multi-component systems that might span administrative domains. The obligation to respect preferences across cascaded systems is a significant challenge.
    *   **Conceptual Problem:** Modern AI is moving towards autonomous agents with minimal human feedback, creating a disconnect between the technical realities and the desire for human-centric preference expression and liability.
    *   **Overly Broad Language:** The wording in the draft was found to be confusing and overly broad, encompassing various outputs like summaries, grounding, and search.
*   **Philosophical Debates:**
    *   The role of the IETF as a technical body in defining "tests" for compliance was questioned; it was suggested that interpretation of preferences would vary between implementers.
    *   A core question: Are preferences primarily about the *AI tools used* or about the *nature of the output itself* (e.g., whether it is substitutive, discriminatory, or used for model training)? Many participants leaned towards the latter.
    *   Concerns were reiterated about definitions sweeping up socially important uses (accessibility, translation) and the IETF's role in balancing these societal costs and benefits.
    *   The importance of Section 3.2 of the draft, which provides flexibility regarding non-compliance in certain circumstances, was highlighted, though some noted risk-averse entities might still avoid beneficial uses.

## Decisions and Action Items

### Decisions

*   The Working Group Last Call (WGLC) for previous drafts failed.
*   Working Group milestones were updated to August 2026 to reflect the significant work remaining.
*   This meeting's primary purpose was to gather preliminary feedback on new draft proposals, not to make final, binding decisions.
*   There was a clear consensus that the `search` category should *not* be nested under `AI output` and should be a separate, freestanding preference.

### Action Items

*   **Editors/Chairs:** Revise the document to un-nest `search` from `AI output`.
*   **Editors/Chairs:** Consider incorporating relevant concepts and granularity from Krishna's draft, which is being incorporated into issues in the repository.
*   **Editors/Chairs:** Revisit the "substitutive use" draft (Bradley Silver's) in light of discussions about the *purpose* of AI processing and output.
*   **Editors/Chairs:** Review and potentially remove/rewrite the penultimate paragraph of the `AI Output` definition, especially after `search` is un-nested.
*   **Working Group:** Members are encouraged to develop and submit concrete use cases to test the proposed definitions for clarity and scope.
*   **Working Group:** Continue the discussion on declarant clarity and transparency (e.g., WordPress, social media platforms declaring preferences on behalf of others), likely during the discussion on `attachment`.
*   **All Participants:** Continue the discussion on the mailing list, particularly for brainstorming new ideas or providing specific language suggestions.

## Next Steps

*   The discussion will resume on Wednesday, starting with the `Automated Processing` term.
*   Further discussions will include `attachment` if time permits after the vocabulary terms.
*   Cross-cutting issues will be addressed in subsequent meetings.