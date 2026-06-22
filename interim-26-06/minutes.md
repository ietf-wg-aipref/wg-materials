# [AIPREF](../wg/aipref.html) June 2026 Meeting Minutes

* Scribe: Chris Needham
* See also:
  * [MeetEcho recording](https://meetecho-player.ietf.org/playout/?session=IETF-AIPREF-20260617-2100)
  * [YouTube recording](https://youtu.be/8rWjyJ4nKbY)
  * [AI-Generated Summary](https://ietfminutes.org/minutes/2026-06-17/aipref.html)

Paul gave an overview of updates in the draft 06 spec. There's a statement at the top saying that it doesn't reflect consensus.

The changes are updates the two categories discussed in the Toronto meeting. Those definitions have not received many comments since that meeting.

Section 3.2 is considered placeholder text as there's disagreement on the overall approach that this section should take.

Lila explained that the subgroup that took an action to work on Section 3.2 are in agreement with each other but other voices have not participated. Lila invited people to contact her to follow up. Chris, Nate, and Leonard offered.

The group discussed the approach to take, whether or not to include examples. Suresh suggested that people work offline and bring something back to the group. It's currently unclear what would gain consensus. Some have advocated for removing the section entirely, others want a more extensive list

Suresh suggested reviewing the list in the previous draft. Farzaneh cautioned against coming up with a comprehensive list, as it wouldn't be complete, and focusing on the category definitions while considering the end user perspective.

Lila also suggested a focus on the category definitions which could then lead to consideration of public interest safeguards. She expressed concern that people involved policy discussions are looking to IETF to have the public interest discussion. She called for IETF to make a determination of whether that discussion should be in scope for the Working Group. Suresh indicated that any decision either way would result in the document not passing a call for consensus.

The group discussed the complexity of the category definitions, their specificity, and whether they should be supported by explanatory examples. As editor Paul said that this could lead to changes to the structural logic of the document.

Suresh asked the group for comments on the search category definition, noting that there had not been discussion on the mailing list. Paul suggested that this definition has held up well.

Paul pointed to the current changes being suggested: the need for an inference time category, and the controversial section 3.2.

Regarding the inference time category, Erin said that she's still thinking about this given recent developments (i.e., the recent UK CMA decision), and may come back with a proposal.

Paul said that he has reviewed the CMA decision against the existing category definitions, but there is currently nothing in our draft regarding grounding. He shared a proposed definition.

Chris said that he's looking for a standardised definition that works across a wide range of AI systems and it's not just about Google. He suggested should look for a definition that is both compatible with the CMA decision, but is also more broadly applicable to other providers of AI systems.

Lila said that she'd organise a discussion on section 3.2, with Chris, Nate, Leonard (and others, possibly) ahead the IETF meeting in Vienna.

The group discussed issue 196. Erin said she's reviewing in light of the CMA decision, but not ready to comment.

Chris summarised the various inference-time / grounding categories that have been shared on the mailing list, from Nate, Paul, and Laurent. He said that the "provided by the user" part of Paul's suggestion is problematic. Chris said that the use cases in Laurent's contribution are valuable and should be added to our wiki so we can test definitions against them.

Kevin said that he agreed there's a bright line between training usage vs post training, but doesn't have well formed opinions on categories other than search.

Leonard said that grounding is a subset of inference time usage. He agrees with Laurent's first and second category definitions.

Nate said that inference is broader than grounding, his proposal starts where the existing training category ends, so those definitions intentionally work together to cover the entire range of usage. He suggested that these two categories could, in future, be enumerated as exceptions. 

Paul discussed AI system vs the user selection of assets as input. He explained that the previous AI Input category failed in our previous London meeting. Martin suggested that the hierarchical nature doesn't change things meaningfully.

Titus supports adding a category, and supports making the distinction between whether the input comes from the AI system or from the user. Content given as input might be used invisibly, and then there's a spectrum of how substitutive it is. He prefers inference as a term over grounding, as grounding is a specific kind of inference.

Nate wants to avoid us having a vocabulary where some use cases aren't covered, as this creates incentive for bad actors. There should be a way to say no to all AI. Suresh suggested identifying some of those use cases to add to the wiki for consideration. Nate said he'd coordinate with Chris to do that.

Martin explained that the categories deliberately overlap, so the search category includes training of AI models. AI systems can be trained live, which should be in the training category. He said grounding in the context of search should fall within the search category.

He asked about the distinction between users and clients of AI systems. In distributed multi-model systems, their clients are other models, also sub-agents. He suggests we need better clarity on this aspect.

Paul asked if we see a path to consensus without an inference time category. If we can establish whether we agree a category should be included, we can move onto the scope of those definitions and whether they leave gaps for particular use cases.

Caleb said (in chat) that there are existing mechanisms to say you don't want any AI usage. Paul indicated that there are cases that our vocabulary may not cover.

Timid Robot expressed hope in a use category, with clear definitions of what happens when they overlap, acknowledging the difficulty of defining the boundary. He suggested issue 172 should be distilled into two categories. He said he may help with that definition, but prefers to focus on section 3.2.

Martin said that based on today's discussion, we're in good shape going into the August meeting.

Coming back to section 4.1, the AI training definition, Paul indicated that he didn't want to revisit this. Farzaneh has raised comments against this, which Paul wants to take into account. Suresh asked her to consider use cases that a definition may not cover. Suresh suggested a deadline of a month from now for comments on the AI training category for Jordan and Farzaneh. Martin said a deadline wasn't needed, and the docu



