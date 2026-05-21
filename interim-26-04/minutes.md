# [AIPREF](../wg/aipref.html) April 2026 Meeting Minutes

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Tuesday, 14 April 2026](#tuesday-14-april-2026)
  - [1. Introduction and Use Case Review](#1-introduction-and-use-case-review)
  - [2. Purpose-Based vs. Technology-Based Model](#2-purpose-based-vs-technology-based-model)
  - [3. Training Preference Category (`draft-ietf-aipref-vocab`)](#3-training-preference-category-draft-ietf-aipref-vocab)
  - [4. Search and Non-Generative Search Preference](#4-search-and-non-generative-search-preference)
  - [Preliminary Decisions (Subject to Mailing List Confirmation)](#preliminary-decisions-subject-to-mailing-list-confirmation)
  - [Action Items](#action-items)
- [Wednesday 15 April 2026](#wednesday-15-april-2026)
  - [1. Relation to Existing Laws and Terms of Use (Issue 1902 / Issue 160)](#1-relation-to-existing-laws-and-terms-of-use-issue-1902--issue-160)
  - [2. Applicability and Effect: Illustrative Lists vs. Exclusions (Issue 160 / Section 3.2)](#2-applicability-and-effect-illustrative-lists-vs-exclusions-issue-160--section-32)
  - [3. Conformance and Technical Limitations (Issue 164 / Section 3.1)](#3-conformance-and-technical-limitations-issue-164--section-31)
  - [4. Distinguishing Access and Use (Issue 167 / Issue 150)](#4-distinguishing-access-and-use-issue-167--issue-150)
  - [5. AI "Use" / RAG Category (Issue 172 / Issue 150)](#5-ai-use--rag-category-issue-172--issue-150)
  - [6. Defining "AI Training" (Issue 1908)](#6-defining-ai-training-issue-1908)
  - [7. Defining "Search" (PR 201 / PR 1909)](#7-defining-search-pr-201--pr-1909)
  - [Preliminary Decisions (Subject to Mailing List Confirmation)](#preliminary-decisions-subject-to-mailing-list-confirmation-1)
  - [Action Items](#action-items-1)
- [Thursday, 16 April 2026](#thursday-16-april-2026)
  - [1. Search Category (PR 201 & PR 202)](#1-search-category-pr-201--pr-202)
  - [2. AI Training Category (PR 205)](#2-ai-training-category-pr-205)
  - [3. Section 3.2: Status of Preferences and Context (PR 206)](#3-section-32-status-of-preferences-and-context-pr-206)
  - [4. AI Input & RAG (Issue 172)](#4-ai-input--rag-issue-172)
  - [Preliminary Decisions and Action Items](#preliminary-decisions-and-action-items)
- [Next Steps](#next-steps)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Tuesday, 14 April 2026

### 1. Introduction and Use Case Review
* **Meeting Kickoff**: Mark Nottingham opened the meeting, reviewing the IETF Note Well policies, agenda, and the group's timeline. Mark Nottingham noted the need for concrete progress outside of meetings to ship specifications successfully.
* **Granularity of Preferences**: The working group reviewed the use cases documented on the wiki (training, use, and presentation). Bradley Silver and Chaerin Lim noted that preference signals should allow for granularity, particularly regarding how private agreements override general preference signals.
* **Scope of Use Cases**: Kaustubh Phatak and Bradley Silver discussed whether use cases should capture the specific reasons an entity might train on content or if the focus should remain strictly on the preferences expressed by content owners.

### 2. Purpose-Based vs. Technology-Based Model
* **Core Philosophy**: Mark Nottingham and Suresh Krishnan noted that the working group has transitioned away from defining preferences based on specific technical ingestion methods, focusing instead on purpose-based categories.
* **Handling Evolving Use Cases**: Eric Rescorla, Andrew Sullivan, and Bradley Silver debated how to handle secondary use cases and future technology evolutions. Andrew Sullivan cautioned against trying to specify every possible exception, emphasizing that the protocol should focus on the most common, clear preference expressions.

### 3. Training Preference Category (`draft-ietf-aipref-vocab`)
* **Removal of "Large"**: The group discussed Issue #183 regarding the subjective nature of the word "large" when describing models. Chaerin Lim, Suresh Krishnan, and Bradley Silver agreed that quantifying model size thresholds is impractical. The group agreed to remove "large" from the text.
* **Generative vs. Classification Models**:
  * A major technical discussion occurred regarding whether the training category should encompass simple machine learning models (e.g., spam classifiers, security analysis, or CSAM detection). 
  * Eric Rescorla, Andrew Sullivan, and Bradley Silver debated whether a model trained for classification purposes inherently possesses generative capabilities. 
  * Bradley Silver and Andrew Sullivan expressed concerns that overly broad definitions could unintentionally sweep in benign, non-generative utilities.
  * A self-organized subgroup (including Bradley Silver, Eric Rescorla, Chaerin Lim, Andrew Sullivan, and Kaustubh Phatak) met over lunch to draft a refined training model definition (Issue #1908). They proposed separating definitions into "general-purpose generative models" and "specialized generative models" while explicitly excluding simple classifiers.

### 4. Search and Non-Generative Search Preference
* **Defining the Search Exception**: The group debated how to formulate a search exception (often referred to as "traditional search" or "laterhosen search") to allow indexation and snippet generation while opting out of broader training.
* **Proposals and PRs**: The group examined two primary text proposals:
  1. **PR 1909 (Amended by Chaerin Lim)**: Focuses on allowing the backend processing of assets to perform indexing and ranking, utilizing models exclusively for the search application, while explicitly excluding generative search summaries.
  2. **PR 201 (Proposed by Jo Levy)**: A single-sentence definition outlining search output capabilities (links, snippets) with detailed sub-bullets specifying exclusions for generative outputs.
* **Points of Contention**:
  * **Verbatim Snippets vs. Adapted Content**: Kaustubh Phatak, Bradley Silver, and Chaerin Lim discussed whether translation, transcription, or non-substitutive modifications should be permitted under the search preference. Chaerin Lim argued that search preferences should not regulate translations, while Bradley Silver highlighted how minor text rewrites can assist user navigation.
  * **Model Training for Search**: Bradley Silver and Andrew Sullivan debated whether it is technically necessary to allow model training to evaluate and rank content for a non-generative search index.

### Preliminary Decisions (Subject to Mailing List Confirmation)
* **AI Training Definition**: Agreed to remove the subjective quantifier "large" from the definition of target AI models in [draft-ietf-aipref-vocab](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/).
* **Simplifying Terms**: Agreed to remove the high-level definitions for "Artificial Intelligence (AI)" and "Machine Learning" from the draft, as they are not technically required to define the specific vocabulary terms.

### Action Items
* **Editors of [draft-ietf-aipref-vocab](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/)**: Synthesize the feedback from the interim meeting to generate an amalgamated proposal combining the concepts from PR 1909 and PR 201 regarding the "search" preference category.
* **All Participants**: Review the proposed text for the training model definitions in Issue #1908 and the search exception proposals, and file GitHub issues highlighting specific objections or required refinements (specifically regarding translation/transcription and snippet boundaries) ahead of the next session.


## Wednesday 15 April 2026

### 1. Relation to Existing Laws and Terms of Use (Issue 1902 / Issue 160)
* **Max** presented a proposal stating that preference expressions are not intended to override website Terms of Use (ToU), and that in the event of a conflict, ToU should prevail as a matter of law.
* **Paul** and **Nate** raised concerns that unilaterally declared ToU are distinct from negotiated bilateral agreements. They argued that explicitly stating that ToU "shall prevail as a matter of law" is problematic across varying jurisdictions and runs counter to the group's purpose of establishing machine-readable signals.
* **Mike** emphasized that ToU generally govern human and logged-in user behavior, whereas machine-readable preferences are aimed at automated crawlers accessing public, non-authenticated content.
* **Meredith** suggested a compromise: state that preferences do not override ToU, but stop short of declaring legal precedence, thereby treating human-use terms and technical-interaction preferences as separate domains.
* **Glenn** noted that the IETF lacks the mandate to order legal instruments and contract formations.
* **Suresh** and **Paul** observed that the draft's original language ("without prejudice to applicable laws") is a neutral, light-touch approach that avoids altering the legal status quo.

### 2. Applicability and Effect: Illustrative Lists vs. Exclusions (Issue 160 / Section 3.2)
* The group debated a proposal by **Alyssa** to pair back Section 3.2, replacing detailed forward-looking permitted reasons to ignore preferences with a high-level, historical summary of safety, accessibility, and public interest practices.
* **Lila** supported retaining an illustrative list of rationales (e.g., academic research, accessibility) to give risk-averse institutions (like libraries and universities) confidence that standard public-interest exceptions remain viable.
* **Tim** (Timid Robot) proposed formalizing these examples into explicit "exclusions" in a new Section 3.2 to avoid having to protect these public-interest use cases individually inside every vocabulary category.
* **Glenn** strongly opposed this direction, stating that carving out licensing-like exceptions or setting policy on internet access exceeds the working group's charter.
* **Suresh** noted that Section 3.2 was originally introduced to clarify that preferences are not technical access controls. He indicated that a more minimal approach, akin to Alyssa's proposal, seemed to have broader support.

### 3. Conformance and Technical Limitations (Issue 164 / Section 3.1)
* **Suresh** introduced Pull Request 1905, which replaces Section 3.1 ("Conformance") with a more precise description of the specification's technical boundaries. 
* The proposed text clarifies that the document's primary purpose is ensuring that expressed preferences are *understood* by recipients, rather than mandating compliance. It explicitly outlines technical limitations, including the lack of built-in origin authentication for certain attachment mechanisms (like `robots.txt`).

### 4. Distinguishing Access and Use (Issue 167 / Issue 150)
* The group confirmed the conceptual separation between content acquisition (governed by `robots.txt` and access controls) and downstream use of the asset.
* **Ronnie** supported this distinction, noting that the draft should focus solely on downstream usage preferences without dictating what governs the initial access. This conceptual alignment successfully resolves both Issue 167 and Issue 150.

### 5. AI "Use" / RAG Category (Issue 172 / Issue 150)
* **Brad** and **Nick** highlighted the critical necessity of a preference targeting Retrieval-Augmented Generation (RAG) and downstream AI usage. They cited data indicating that RAG-driven crawling is replacing traditional search traffic, significantly impacting referral rates for small publishers and risking brand damage through hallucinated or misattributed outputs (e.g., "Frankenstein recipes" or incorrect itineraries).
* **Paul** noted that external initiatives like Rights Statement Language (RSL) and Content Signals contain "AI input" categories that are designed to be compatible with AIPREF.
* **Meredith** raised a structural concern, suggesting that attempting to control downstream information use post-publication conflicts with the core open-web publishing bargain.
* **Kevin** suggested exploring more granular display-based preferences, allowing publishers to opt into generative features only if proper attribution and links are guaranteed.

### 6. Defining "AI Training" (Issue 1908)
* The group evaluated two competing definitions for the training preference: Option 1 (narrowly tailored to models with generative capabilities or design purposes) and Option 2 (a broader definition covering general machine learning/AI models).
* **Tim** and others expressed concern that Option 1's focus on "design purpose" allows a "bait-and-switch" scenario where a model trained for non-generative purposes is later used generatively.
* A poll of the room was taken, indicating a strong preference for Option 2 (broader definition).

### 7. Defining "Search" (PR 201 / PR 1909)
* The group compared PR 201 (paragraph style) and PR 1909 (bulleted list).
* **Warren** expressed concern that explicitly banning "generative" capabilities in search might inadvertently prohibit non-substantive AI utilities, such as intelligent image cropping/resizing or semantic search term matching.
* A poll of the room indicated a preference to use PR 201 as the baseline. 
* A subsequent poll was taken on whether to keep or remove the word "verbatim" in relation to snippets. A strong majority favored removing "verbatim" (75% to 25%) to allow placeholders for non-substantive accessibility transformations (e.g., translation and text-to-speech).
* **Nate** and **Tom** cautioned that "non-substantive transformation" requires precise definition to avoid conflicting with other search exclusions.


### Preliminary Decisions (Subject to Mailing List Confirmation)
* **Issue 167 (Distinguishing Access and Use)**: Closed, with the understanding that access and downstream use are strictly separated.
* **AI Training Preference**: Option 2 (broader AI model definition) was selected as the starting baseline. The vocabulary term will be updated to "AI training".
* **Search Preference**: PR 201 was selected as the starting baseline. The word "verbatim" will be removed, and a placeholder for accessibility/translation transformations will be incorporated.

### Action Items
* **Editors**: Create and update Pull Requests for the "AI training" (Option 2) and "search" (PR 201 with accessibility edits) definitions to reflect the room's preferences.
* **Suresh**: Submit PR 1905 (Section 3.1 Conformance) to the mailing list for a formal consensus call.
* **Nick, Brad, Kevin, and Suresh**: Collaborate on drafting a concrete proposal for a "use/input" (RAG) category prior to the next interim.
* **Krishna**: Open a GitHub issue to analyze how the new search preference interacts with legacy crawler directives (e.g., `no-snippet`).

  
## Thursday, 16 April 2026

### 1. Search Category (PR 201 & PR 202)
The working group reviewed the proposed changes to the "Search" category in [draft-ietf-aipref-vocab](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/).
* **Non-Substantive Changes & Summaries:** The participants discussed the inclusion of "non-substantive" modifications. Christopher Flammang raised concerns regarding how to clearly differentiate non-substantive changes from summaries, noting that the relationship between excerpts, translations, and generative summaries needs clearer guidelines. Michael Jones requested further clarification on whether the category covers single-result summaries or set-of-results summaries.
* **Trained Model Scope:** Henk Birkholz highlighted the risk of search providers using publishers' content to train broad AI models under the guise of providing search. He emphasized that any model training permitted under the search category must be strictly constrained to the provision of that specific search service. 
* **Excerpts Wording:** To address concerns that the phrase "only excerpts... are displayed" was overly restrictive for UI elements (like links or styling), Christopher Flammang and John Mueller proposed refining the language. The group favored a formulation where displayed excerpts "serve to assist users in evaluating the relevance of the results" rather than strictly limiting the display to excerpts.
* **Defining Search Applications:** Christopher Flammang and Michael Jones debated whether "search applications" must strictly be defined by user queries, pointing out that implicit queries or feed-based discovery (e.g., news feeds) should be accommodated. Henk Birkholz cautioned against making the definition too broad (e.g., inadvertently covering electronic program guides or recommendation systems).

### 2. AI Training Category (PR 205)
The group discussed renaming the "Foundation Model" category to "AI Training" to better reflect its technical scope.
* **Definition Refinement:** The draft definition was simplified to "the act of using an asset in the production or refinement of an AI model." 
* **Parameters & Weights:** The group agreed to remove specific references to "weights" or "parameters" to keep the vocabulary future-proof and avoid technical loopholes. 
* **Explanatory Note:** John Mueller suggested adding a non-normative explanatory note clarifying that, in practice, any use of an asset that has the effect of changing or refining a model (including fine-tuning, Low-Rank Adaptation (LoRA), or third-party refinements) is encompassed by this category.

### 3. Section 3.2: Status of Preferences and Context (PR 206)
The working group debated PR 206, which introduces non-normative text on how preference expressions interact with legal and historical contexts.
* **Historical Context Paragraph:** Christopher Flammang and Henk Birkholz strongly objected to the "historically" paragraph, arguing it was confusing, incomplete, and too closely aligned with US-centric legal concepts (e.g., fair use). They suggested either removing it entirely or significantly simplifying it.
* **Public Interest Considerations:** Michael Jones and Suresh Krishnan noted that highly risk-averse organizations (such as those conducting academic research, web archiving, or accessibility work) need clear guidance that the vocabulary does not override legitimate public interest or statutory legal exceptions.
* **Neutrality:** The sense of those present was that the document must remain strictly neutral, avoiding both the appearance of granting a license and the implication that existing legal exceptions are clawed back. 

### 4. AI Input & RAG (Issue 172)
A preliminary discussion was held on creating a category to cover Retrieval-Augmented Generation (RAG) and model grounding, proposed as "AI Input."
* **Scope of Input:** The proposed category aims to distinguish between automated background retrieval (scraping/RAG) and direct user-initiated uploads of specific assets.
* **Bypassing Site Controls:** Henk Birkholz raised concerns about users bypassing site-level crawlers or `robots.txt` controls by pasting URLs directly into models, complicating how publishers express usage preferences.
* **Refinement vs. Inference:** John Mueller and Michael Jones pointed out that some RAG implementations feed user interactions back into training loops (backpropagation). The group agreed that if a RAG process results in model training, the "AI Training" preference must also be respected.

---

### Preliminary Decisions and Action Items

* **Decision:** Agree to merge the "Search" category changes (PR 201/202) and "AI Training" category changes (PR 205) into the editor's draft. These sections will be flagged as lacking final working group consensus to allow for further public tracking and iteration.
* **Decision:** Merge PR 206 (Section 3.2) into the editor's copy to serve as a baseline, with the understanding that the "historical" paragraph will undergo further revision.
* **Action Item:** Christopher Flammang and Henk Birkholz to collaborate on a simplified, neutral proposal for Section 3.2 that addresses public interest overrides (such as archiving and accessibility) without US-centric historical framing.
* **Action Item:** John Mueller and Henk Birkholz to draft concrete use cases and initial text for the "AI Input" / RAG category under Issue 172.

  
## Next Steps
* The working group will conduct asynchronous consensus calls on the newly established baselines for the training and search terms.
* **Interim Schedule Plan**:
  * **June 2026**: Virtual interim meeting focusing on "use" category proposals and restarting discussions on the attachment specification.
  * **July 2026 (IETF 126 - Vienna)**: Request two 2-hour slots to socialize proposals with the wider IETF community.
  * **Late August / Early September 2026**: Proposed hybrid interim meeting in Europe (target: London).
  * **Hosting:** Suresh Krishnan requested that any organizations willing to host the August interim submit facilities proposals within the next two weeks. Default fallbacks are available if no external host is secured.
  