# AIPREF Working Group Interim Meeting - 23 June 2025

Notetaker: Felix Rada

* Purpose of interim meeting is to solicit feedback on latest drafts and identify outstanding issues.
* Editors plan to make one more update to current drafts before design team meeting in mid-July.
* Presentation of vocabulary draft, attachment draft and corresponding open issues by Martin Thomson.

# Vocabulary draft - issue discussion, draft review

## Relationship between categories
* What does it mean that one category encompasses another?

Farzaneh: Is it possible to declare "tdm=no, AI=yes"? 

Paul: Yes, being lower in the hierarchy does not mean that a specific instruction cannot overrule the more general category instruction.

** Figure visualizing the hierarchy between categories is unclear

Stéphane: Hierarchy should only exist if it serves a purpose.

Suresh: From declaring party perspective, having a catch-all category is helpful, because it allows you to opt-out of everything and only allow uses that you fully understand and endorse.

* Should TDM category be renamed to something like "computational analysis"?
  * Support for renaming to emphasize that it is an all-encompassing umbrella category
  * Assumption is that AI inference and search categories are included in TDM category
  * akin to "non-human usage"

Paul: If there is no overarching category broadly equivalent to TDM as defined in EU law, EU copyright holders will not be able to use the vocabulary and may resort to another one, meaning that rights holders

Martin: There is demand for the ability to declare a broad preference against all uses and then opting in to selected, specific uses. The EU definition of TDM is helpful, though we don't want to tie the vocabulary to any given law.

Suresh: Having a hierarchy enables the same signal to be interpreted in the same way in different legal regimes, Is there/should there be overlap between the search and inference categories?

* different positions on whether "inference" and "search" categories should be included

Farzaneh, Paul: importance of clarifying that preference signals do not confer rights, vocabulary does not assume that rights holders are making preference declarations

Farzaneh: preference signals should consider the end user, this raises problems particularly with inference/RAG category

Paul: To reduce potential impact on end users, editors consider narrowing the inference and search categories

M Thomson: AI inference and search categories have a risk of overlapping, search includes AI at various steps

* What should be the scope of the inference category?

Felix: Instead of AI inference category, describe how that use-case differs from search and how the information is presented to the user.

Leonard: This category is different from training, because the asset is not used at the training stage, but at the inference stage, so it should be separate from AI training.

Paul: Demand for "search" and "inference" categories comes up consistently, we just need to get the names and definitions right.

Timid Robot: Focus on "what" of the categories, not the "how", to avoid overlap between them

Felix: Vocabulary for behavior of an AI system, may want to
distinguish from direct user input and inference distinguish between human and AI system behavior

Paul: Inference category needs to be narrowed down based on the discussion. To remain understandable, we may need to renam the category based on the narrowed-down definition, for example using a term like RAG. What many rights holders care about are cases like AI summaries, translations, style imitations etc. The objective is not to interfere with individual users' rights.

Leonhard: Terms like "prompt-time" or "RAG" could be workable, but the category predates RAG in the context of asset-based identifiers. If a declaring party says "you cannot use this as a style reference", they should be able to express that preference and incorporate it into the asset.

Timid Robot: User prompt example is a UX problem, not an AI preference problem. Vocabulary is not an access control mechanism.

Felix: If a TDM category is included, some commercial entities will treat it as a legal directive and restrict downstream uses that end users may actually be allowed to perform based on other copyright exceptions.

Leonhard: The market will address demands for AI systems that down restrict users' rights

Mark: We should be explicit about these possible effects

Paul: It may be out of scope to tell third parties what consequences to draw from voluntary preferences, but we should improve the definitions to limit unintended consequences.

Suresh: Should preferences be carried forward?

* Objective of vocabulary is to align between different entities working on this issue, including IPTC

# Attachment draft - issue discussion, draft review

* Where in time does the preference apply (between crawling and use)?
* attachment includes embedded metadata
* a sub-group could discuss how the attachment for other attachment mechanisms could work

* issue #51: Should path come before or after expression?
  * affects extensibility: Should users be able to attach additional information to their preferences, such as a link to terms of service? Not necessary to include in first version, but the form should support adding it later.

backwards compatibility with existing robots.txt is an important design consideration

How does the attachment mechanism resolve hierarchy or conflicting information, e.g. robots.txt declares disallow, but content-usage for specific uses is set to y?
  * Attachment document will deal with the hierarchy between different attachment mechanisms, e.g. robots.txt vs. HTTP headers.
  * need for clarity on crawling rules vs. usage rules
  * today many site owners interpret the presence of a crawler as equating usage for AI training. There is potential for misunderstanding that crawling and use are not the same thing.

# Conclusion & next steps

* Participants are asked to stay up to date with mailing list and review next version of drafts before the London meeting.
* All issues should be exposed before the meeting (asap), so the meeting can be focused on addressing the issues.
* Opportunity to have a hackathon at Madrid meeting to test and validate some of these concepts.