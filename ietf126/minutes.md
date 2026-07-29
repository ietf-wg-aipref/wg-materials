# IETF 126 AIPREF Working Group Minutes

Note taker: bnewbold

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [WG Status and Meetings](#wg-status-and-meetings)
- [PR 213 Discussion](#pr-213-discussion)
- [Second PR ("Refine section 4.1...")](#second-pr-refine-section-41)
- [Use / Inference](#use--inference)
- [Wrap Up](#wrap-up)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


## WG Status and Meetings

MN (Chair): Status: had an interim meeting which went well, encouraging progress and momentum.

SK (Chair): Pattern of stronger process at interim meetings to date.

MN (Chair): Will push for more interactions on mailing list, pushing towards decision making, but still plan to schedule more interim meetings. Next interim in London (late August), with additional to follow. Call for hosts.

## PR 213 Discussion

https://github.com/ietf-wg-aipref/drafts/pull/213

MN: Proposal to cut down scope of section in Vocab document. There has been both support and objections to this PR.

Timid robot (author of PR): This WG is in a difficult place b/c there is already legislation in place which puts pressure on the outputs of the group. With that in mind want to reduce scope. Request to keep feedback in the form of proposed changes to the text. Please restrict criticisms to what is actually in the text. Goal to ensure that this work is not an extension of legislation.

Glenn (Universal): The IETF does not write legislation. Legislation can evolve to change based on what the (IETF) community does. Disagrees with last line of current PR, supports a change proposed by Sebastian on the mailing list. Wants to avoid getting this work in to copyright and other concerns, and Sebastian's proposed change.

The text in question from the PR:

> Because of this, stakeholders need to decide when and how to follow or not-follow preferences in the context of legal, institutional, ethical, or other interests and commitments.

Glenn: This opens a can of worms. Folks might cherry pick out specific terms from this statement.

MN: Thinks that this is a clarifying statement about how the work will be interpreted in the real world.

Glenn: "legal" and "ethical" are the specific terms of concern.

Sebastian's text:

> An entity that receives usage preferences has a choice whether to follow those preferences. This specification does not determine how that choice is made. Whether and under which circumstances a preference is followed is outside the scope of this specification.

MN: This seems like the only contested part of the PR, so will focus on this aspect.

Timid robot: Largely agree with Glenn. But think that we can be more helpful in the environment this document will be published in. Thinks that the current PR is preferable, but happy that the proposed change only applies to that one paragraph.

MT: Has another proposed text:

> An entity that receives usage preferences has a choice whether to follow those preferences. External factors could influence that decision, but the decision itself is outside the scope of this document.

MN: More nuance in this discussion today than there has been on the mailing list.

Nate: I am part of a small group that came up with this text. Wants to ensure there is input from that entire small group. The first parts of the PR have no objections, it is just this last part. Recently went back and read the robots.txt RFC and it does have some similar language.

Mirja: The previous text clarified that not following preferences was not necessarily bad behavior, and this current text does not have that. There is some text elsewhere in the document (a bullet point; that the document does not provide for enforcement), but that could imply that the specification is intended to be the *basis* for enforcement.

MN: We should not get in the business of defining "good" or "bad" behavior in this group.

Glenn: Say that an implementor takes this spec and does add an enforcement mechanism.

Mirja: Just want to clarify that the purpose of this document is to be a basis or component of enforcement. But folks can do enforcement if they like.

EKR: Thinks that MT's proposed text is fine.

MN: Seems to be convergence on MT's text. Let's take it to the list, maybe a formal consensus call.

Sebastian: Comparing the versions: in one the specification itself is the first mentioned thing, and in the other external factors are mentioned first.

MN: This seems more editorial, not fundamental disagreement, which is progress (though not everybody is in the room).

## Second PR ("Refine section 4.1...")

Kevin: Work from Toronto was to incorporate feedback from discussion there. One concern was to ensure that preferences "stayed attached" through model training. But this seems to be an attachment concern, so that language was removed from this draft. Elsewhere word "synthetic" was proposed to be removed, but I think it is stronger to keep it.

Nate: Can you clarify why these changes were proposed? (the "used or made available to use, for generation")

Kevin: Refer back to the second paragraph of the PR description.

EKR: Think that this text is good. Can you give an example where a model might be used to generate content where that is not synthetic content?

Kevin: Good question. No, can't give such an example, though in theory such a model could be trained. Just made this change to be clearer.

EKR: Ok, not going to debate, just wanted to understand.

Farz: Previously raised concerns in Toronto that the proposal made the category broader. Kevin has mostly addressed those since then. Cautiously optimistic that we can support this language.

Martin Duke: Not an expert here, but regarding "synthetic" term (gave an example about retrieving colosseum photos)

Nate: Concern about replacement of "production" and "refinement" terms. Don't think that models really "learn".

Kevin: Good points. When you are producing or refining, you are modifying the "learned parameters". I've chosen precise language here.

Nate: When does this terminology end? Are "weights" a type of "learned parameters"?

Kevin: Often just say "weights" all along. But when you are doing inference, you are sampling from the weights (learned parameters), no longer modifying them.

Nate: Makes sense, important thing is to maintain a clear line between this and inference.

Lin: Sugests adding some context about the terms and why they are used.

EKR: Hypothetical: every day takes the first 100k of the nytimes and uses it at the start of the context window. Would this language cover that?

Kevin: A bit hard to say, but probably not.

EKR: Trying to test the boundaries of definitions here.

Kevin: This is sort of a degenerate case of RAG, which we have discussed previously, and will probably get to soon.

MN: Productive conversation, let's continue on the list.

## Use / Inference

MN: Have preserved definitions of "use" and "inference" terms in the Github wiki. We could use those as starting points for discussion. We can start those discussions when we get proposals.

Nate: Wrote a proposal in PR 172 which has not gotten many comments (on RAG and Grounding). My proposal is basically "everything after training". Don't need to define every category of use, but if we can define the process of "training a model", we should be able to express preference around use of use models.

MN: See some nodding heads in the room.

Timid robot: Want to repeat something said in Toronto, which is that fuzziness can be resolved by defining what should happen if categories do overlap.

Paul: What Nate proposed is sort of a rewording of the very first attempt at this in London. There is fundamental disagreement around "who is using the content"? Is it the AI model (or the party operating the model), versus a user providing the thing to the model. And whether this preferences should apply to individual user's behavior. We know some people want to include this, some want to exclude this, so probably need to separate them.

Nate: yes, maybe need two separate categories, one for users and one for automated. Alternatively, could have a separate "user invoked" category similar to search. The "put a bikini on here" phenomenon is an example of user behavior that might want to be ruled out by preference.

Faraz: Agree with what has been said. We are not here to do content moderation. Have discussed the impact on end user if preferences are too broad or impact things like translation and accessibility. We need to address those concerns when discussing inference. Users taking direction action should be out of discussion.

EKR: As a practical matter, trying to enforce against user-supplied artefacts will not be effective, so we shouldn't worry about them.

SK: To address Mirja's earlier question (...)

MN: It seems like the user-supplied artefacts is the controversy.

Mirja: A category which covers both cases would be quite broad.

Timid robot: Responding to EKR's statement about user-supplied artefacts, previously Leonard had provided several examples of flows where software might refuse to take actions based on metadata and preferences. Share the Faraz's concern that this ends up very broad.

Paul: We know that people have different expectations about the expression of preferences, and honouring them. Autonomously fetching versus user-provided does seem to be the split.

Sebastian: Do we have terminology for the modes that we want to separate? (autonomous and user-provided). Eg, RAG. This will have an impact on attachment document, eg if preferences need to be attached to assets. Nate's proposal to not distinguish might make this simpler, but if we do separate them, we need clear terminology.

MN: Might help even the discussions to have clear terms.

Nate: Agree with Paul. Having two categories which together cover the whole field seems good.

Faraz: We have discussed a lot, and have heard from public-interest groups that this could have an impact on the consumer side. Concerning to me that we are discussing having preferences apply in situations where user takes a direct action.

Timid robot: Agree with Faraz, but think that this WG is not focused on social or political concepts like the open web or public interest. And that a good approach is to focus on clear definitions of when preferences apply (eg section 3.2).

(no further talks)

## Wrap Up

MN: Want to do whatever we can between now and the next interim meeting to ensure that meeting is productive. Will discuss the PRs on the list, and the use/inference definitions. Will start developing an agenda in coming weeks.

SK: Reminder that we don't have an AI-use category in the document today. Requests input from Faraz on section 3.2.

Faraz: No problems with section 3.2. The disagreement is feeling that this section is not sufficient to ensure the public interest and ensure access to the internet and AI services.

Thom: Have a draft trying to define what "machine readability" means, as it is being used in a lot of other documents. It is 00 right now, we are working on 01. There is a link to this on the mailing list.

MN: Collaboration is helpful and results in better outputs, want to encourage it.

SK: Want to thank Lila for her work on docs.
