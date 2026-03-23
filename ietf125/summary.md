<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Session Summary: 20260316-0330](#session-summary-20260316-0330)
- [AIPREF](#aipref)
  - [Summary](#summary)
  - [Key Discussion Points](#key-discussion-points)
    - [Charter and Scope](#charter-and-scope)
    - [Document Status and Editorial Updates](#document-status-and-editorial-updates)
    - [Contentious Issues: Search and AI Output](#contentious-issues-search-and-ai-output)
    - [Use Cases and Future Proposals](#use-cases-and-future-proposals)
  - [Decisions and Action Items](#decisions-and-action-items)
  - [Next Steps](#next-steps)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



**NOTE**: _This is a non-normative, AI-generated summary supplied only for convenience; it does not necessarily represent an accurate record of the meeting. See the minutes for the authoriative record. See [the source](https://ietfminutes.org/) for more information._



# Session Summary: 20260316-0330

# [AIPREF](../wg/aipref.html)

## Summary
The AIPREF working group met at IETF 119 to provide a status update on the development of protocols and vocabularies for expressing AI usage preferences. The group is currently focusing on refining the core semantics of its primary drafts after a previous Working Group Last Call (WGLC) was unable to reach consensus. The chairs emphasized a shift toward a "Minimum Viable Product" (MVP) approach, paring back contentious terms to establish a solid technical foundation.

## Key Discussion Points

### Charter and Scope
*   **Mark Nottingham** reviewed the working group charter, highlighting that the goal is to standardize building blocks for the **expression of preferences** regarding AI model development and use.
*   It was reiterated that the group is not creating technical enforcement mechanisms; the work is analogous to `robots.txt`.

### Document Status and Editorial Updates
*   The group is working on two main documents: [draft-ietf-aipref-vocab](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/) and [draft-ietf-aipref-attach](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/).
*   **Martin Thompson** (Editor) noted that while small improvements regarding conformance text are being made, the drafts are largely stable as the group awaits substantive proposals on broader categories such as "inference" and "AI output."
*   Contentious terms related to AI output and search carve-outs have been removed from the current versions of the drafts to focus on the core vocabulary. The history and reasoning for these removals are documented on the working group wiki to prevent redundant discussions.

### Contentious Issues: Search and AI Output
*   **Search:** Discussion continues regarding the "search" term. There is concern about the power imbalance if search engines require AI training consent as a prerequisite for indexing. However, defining universal semantics is difficult because AI is increasingly integrated into standard search functionality.
*   **AI Output:** Previous proposals (e.g., the "Zurich proposal") regarding preferences for how data is treated in AI model output fell apart under scrutiny. The chairs suggested a broader discussion is needed to find an appropriate approach for this area.

### Use Cases and Future Proposals
*   A new wiki page has been created to collect use cases in three categories: Training, Use, and Presentation.
*   The chairs encouraged participants to think in terms of **purpose-based** or **display-based** preferences (how data is used) rather than just whether AI is involved, as this may be a more promising path for consensus.
*   **Benjamin Curtis** mentioned work on an IEEE standard for user preferences (including cookie banners and AI) and asked about its relevance. **Mark Nottingham** and **Martin Thompson** noted that while user-level controls are relevant, they are "fraught" with concerns regarding user agency and the open web.

## Decisions and Action Items
*   **Action Item:** Participants are requested to submit use cases to the new [WG wiki page](https://wiki.ietf.org/en/group/aipref) focusing on the expression of preferences.
*   **Action Item:** Any new technical proposals for the upcoming interim meeting should be submitted to the mailing list or as Internet-Drafts well in advance of the meeting date.

## Next Steps
*   **Interim Meeting:** A three-day interim meeting is scheduled for April in Toronto. The goal is to hone the existing drafts and evaluate any new proposals that might gain consensus.
*   **Focus:** The working group will continue to focus on achieving a "Minimal Viable Product" for the core vocabulary and attachment mechanisms.