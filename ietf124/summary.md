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
- [Session Summary: 20251105-2100](#session-summary-20251105-2100)
  - [Summary](#summary-1)
  - [Key Discussion Points](#key-discussion-points-1)
  - [Decisions and Action Items](#decisions-and-action-items-1)
  - [Next Steps](#next-steps-1)

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

# Session Summary: 20251105-2100

 Meeting Minutes

## Summary

The AIPREF session focused primarily on the "automated processing" top-level preference term, which had seen significant discussion since the previous meeting. Participants raised strong concerns about its broad scope, potential for unintended consequences, and impact on socially beneficial uses like accessibility tools. The discussion explored alternative approaches, including removing the hierarchical structure, narrowing the definition to AI-specific contexts, and the role of "unknown" or "uncategorized" uses. There was also a notable debate on the practical and legal implications of such preferences, particularly regarding EU law and the behavior of implementers. Ultimately, no consensus was reached on the "automated processing" term, and the chairs indicated it would likely be removed from the draft for now to allow for further conceptual development. Progress was noted on the "Foundation Model" and "Search" terms, while the "AI Output" term also required substantial revision or removal.

## Key Discussion Points

*   **Note Well and Agenda**: The session began with the customary IETF Note Well reminder. The agenda focused on discussing "automated processing," the last of the "four horsemen" of AI preferences, with an anticipation of spending most of the time on this topic before discussing next steps.
*   **Concerns about "Automated Processing" Term**:
    *   **Lila Bailey** expressed concerns that the "automated processing" term, as currently defined, is too broad, sweeping in a wide range of socially beneficial, commercial, private, and personal uses that are not even AI-related. She specifically highlighted accessibility tools (screen readers, text-to-speech, captioning, alt-text generators), questioning if such tools would be affected and if the current "ignore preferences" clause (Section 3.2) offers sufficient protection. She referenced the Marrakesh Treaty as an example of societal rejection of copyright holders preventing accessible formats.
    *   **Meredith** emphasized the importance of considering the interests of users and the public, particularly concerning research, free expression, and equitable access to information. She worried that prioritizing the interests of AI tool developers and content creators might overlook what is truly useful for the public, especially disability rights. She argued against enshrining preferences that are not socially beneficial, such as opting out of accessibility or certain types of research.
    *   **Victoria** echoed concerns that a "catch-all" category for automated processing is bad in principle because it inherently sweeps up unanticipated good uses, including accessibility and expression. She stressed the need to prioritize user interests above those of publishers or companies.
*   **Defining "Unknown" and Scope Refinement**:
    *   **Ted Hardie** suggested moving away from a hierarchical structure for preferences. Instead, he proposed treating categories as parallel, allowing for a separate declaration for "unknown uses" that is not at the top of a hierarchy. If no preference is expressed for "unknown," the default would be a null response, leaving it to the reader's best judgment (potentially guided by jurisdictional defaults). He was open to adding "assistive technology" as a specific preference if that helps address concerns.
    *   **Timid Robot** questioned if removing the hierarchy would truly resolve unintended consequences, suggesting it might necessitate anticipating all unintended uses to categorize them. He asked if narrowing the scope of the top-level term to strictly AI-related activities would alleviate concerns.
    *   **Martin Thomson** acknowledged the difficulty in defining "automated processing." He proposed a distinction based on "processing that happens for a human or a single human user" to separate automated from non-automated processing, which could protect accessibility tools. He also argued against Ted's "uncategorized" concept, stating that "unknown" to the preference setter is also "unknown" to the consumer, leading to ambiguity, and that categories will evolve. He encouraged constructive suggestions for improving the definition rather than debating its existence.
    *   **Bradley** noted that external pressure from policymakers (especially regarding TDM exceptions/opt-outs) means *some* group will define such a category if AIPREF does not. He argued that the broadness of the term doesn't mean the preference shouldn't exist, and that publishers also have an interest in accessibility. He highlighted the current lack of visibility into crawlers' identity and purpose as a key reason for the need of a broad category.
    *   **Alyssa** drew parallels to the GEO-PRIV working group, where attempts at defining very specific preferences did not lead to widespread deployment. She asserted that if the document doesn't define something, people will interpret it as they wish. She questioned the value of an "unknown/uncategorized" category without clear use cases that outweigh the cons.
    *   **Ecker** argued for a "catch-all" category to provide determinism for site operators, preventing them from having to specify every possible use case. He differentiated between opposing a catch-all *in principle* versus opposing specific things swept in by a particular text. He also pointed out that existing mechanisms (like robots.txt) already allow for expressions that some might consider "bad policy."
*   **Practical and Legal Implications**:
    *   **Glenn** cautioned against creating exhaustive lists due to the rapidly evolving nature of technology. He advocated for solutions that allow for evolution and for publishers to choose between opt-in or opt-out models, recognizing that publishing content implies a desire for it to be used.
    *   **Robert** highlighted that current privacy and rights frameworks often leave users without choice regarding their data. He questioned the effectiveness of past opt-in/opt-out solutions (e.g., robots.txt limitations) and stressed the importance of user agency regarding data use, particularly for AI training.
    *   The chairs (Martin and Ecker) encouraged participants raising concerns about negative effects to specify the *mechanisms* causing those effects, beyond simply stating "these are just preferences."
    *   **Victoria** suggested the legally binding effect under EU law as a mechanism, noting EU exceptions are less flexible than US fair use.
    *   **Paul Keller** disputed the claim that current EU law directly references or makes any of this work mandatory, encouraging reference to mailing list discussions.
    *   **Aaron Simon** argued against a "naive" view that preferences can be ignored, stating the European Commission would likely treat IETF standards (especially if an extension of robots.txt) as binding via the AI Act's code of practice. He emphasized IETF's responsibility to define an appropriate scope and avoid creating categories that are "actively harmful" or allow rights holders to govern every possible use of content.
    *   **Ecker** pointed to text in the draft stating enforcement varies by jurisdiction and acknowledged IETF cannot control EU law but can control the breadth of the categories.
    *   **Nate** expressed concern that, by not having more granular preferences, the net effect benefits incumbent companies who bundle services (e.g., search and AI summary) without allowing users to specify different uses.
*   **Accessibility and User Intent**:
    *   **Meredith** specifically highlighted that most users with disabilities rely on general-purpose commercial tools. She warned that if compliance with preferences doesn't incentivize enabling accessibility, those uses will be inadvertently excluded, not due to malicious intent, but out of necessity.

## Decisions and Action Items

*   **Decision**: Consensus was not reached on the "automated processing" top-level term.
*   **Decision**: The "Foundation Model" term is a promising candidate for continued discussion and work.
*   **Decision**: The "Search" term is also promising for continued work.
*   **Action Item**: The current text for the "AI Output" term is seen as a distraction and will likely be pulled out by editors for now, with further discussion needed to refine its conceptual slot.
*   **Action Item**: The "automated processing" term will likely be pulled out of the draft for now. Community members are encouraged to propose alternative functions or definitions that could achieve consensus for this conceptual slot.
*   **Action Item**: Chairs will initiate consensus checks on the mailing list for the proposed directions regarding "Foundation Model" and "Search" categories.

## Next Steps

*   An interim online meeting (one or two sessions) will be held in December to continue discussions.
*   Another hybrid face-to-face meeting is planned for late January or early February.
*   The chairs will follow up on offers for meeting hosts (in the United States and Canada) and solicit feedback on preferred locations from the community.
*   The chairs will start mailing list discussions and consensus checks to formalize the outcomes of this meeting and gather broader community input, especially from those unable to attend.