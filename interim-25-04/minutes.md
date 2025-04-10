# IETF AI Preferences Interim Meeting Minutes

Brussels, Belgium - 8-10 April 2025

Chairs: Mark Nottingham and Suresh Krishnan


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Morning session, 8 April 2025](#morning-session-8-april-2025)
- [Afternoon session, 8 April 2025](#afternoon-session-8-april-2025)
  - [Summary of morning (Mark)](#summary-of-morning-mark)
  - [draft-keller-aipref-vocab-01 (Paul Keller)](#draft-keller-aipref-vocab-01-paul-keller)
  - [Vocabulary Issues (lead by Mark)](#vocabulary-issues-lead-by-mark)
    - [Interface to attachment - abstract model or strings?](#interface-to-attachment---abstract-model-or-strings)
    - [Search / discovery carve-out](#search--discovery-carve-out)
- [Morning session, 9 April 2025](#morning-session-9-april-2025)
- [Afternoon session, 9 April 2025](#afternoon-session-9-april-2025)
  - [HTTP Header field attachment (unit based)](#http-header-field-attachment-unit-based)
  - [robots.txt attachment (location based)](#robotstxt-attachment-location-based)
  - [The document that we will adopt](#the-document-that-we-will-adopt)
- [Morning session, 10 April 2025](#morning-session-10-april-2025)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->
  
## Morning session, 8 April 2025

Note takers: Ted Hardie, Martin Thomson

Slight delay in opening the meeting due to a train strike here in Brussels.

The chairs begin with a brief overview of the IETF and its processes. They show the Note Well and explain its meeting, and then go through norms for participation. They describe the BCP implications for IPR on contributions. Note that this session is not under Chatham House rule, but is being recorded and minuted. The chairs then describe the consensus process within the IETF and reference RFC 7282. Noting that they hope it will not come up, the chairs explain the IETF appeals process.

The chairs note that they do expect the interim meetings for the working group to be face-to-face, but that open access will be provided by remote participation using the IETF’s toolset. The chairs will experiment with different ways to manage the queue, using both in-room and MeetEcho queueing. The chairs then reviewed how drafts are adopted and changed. The role of the editor was then reviewed, highlighting that they serve the working group, rather than exercising control over the content themselves.

The group will use GitHub, but the consensus is determined on the list, even though there may be some discussion on PRs (there is a preference to use those for editorial changes). The issues list will be used as a tracker, but the mailing list is the focus of discussion for substantive changes. https://ietf-wg-aipref.github.io/ is the working group github page. That, and much else, is linked from the datatracker’s page for the working group: https://datatracker.ietf.org/wg/aipref/about/ . The group then reviewed how working group last call and other steps lead to finishing work items. The chairs highlighted that positive expressions of support are important in this process. The charter of the group may be updated after producing the initial set of deliverables. Because of the aggressive timeline for the group’s work, expanding the scope would be done after delivering the initial document(s).

In response to a question, the chairs clarified the role of the Internet Engineering Steering Group (IESG). There were additional clarifications on the contribution process and the IESG ballot process.

The group then went through a round of introductions: please review the recording for the introductions.

The morning’s agenda is loose, to foster discussion. The first topic will be the vocabulary, which is one of the core outputs. The follow-on discussion will be on attachment. The final deliverable is an overview, but the chairs would be happy if the first two result in recommendations to the list of starting points for the ongoing working group discussion.

Martin suggests a structure to the first day’s discussion. The first would be the opt-in/opt-out/silence states for preference expressions. The second would be the application of the vocabulary to different activities–acquisition, training, use of trained model. He would also like to know whether search indexing is in scope for the work, since it may be interlocked with the location-based aspects of the discussion. Mark Nottingham notes that we have to be very aware of the context of the work–we are describing a technical mechanism, but it occurs within a legal context.

Glenn Deen wonders if, when we write this down, we can carefully describe the scope and applicability, so that those who might want to use it in other contexts are aware of what was intended. Mark suggests that we might need a guide to policy makers as an additional documents. Glenn is concerned that this technical solution might get pulled into new contexts where it might not be a good fit. Suresh notes that we are trying to provide signals and that the lack of signal may be interpreted differently in different contexts or jurisdictions.

Martin notes that legislation may simply over-ride a preference (e.g. the carve-out for research). In other contexts, the legislation may establish a default. We also have to note that these preferences will not be sufficiently detailed to handle the use cases currently handled by bilateral.

Leonard notes that he believes that there is a “fourth state”, and that the way TDMRep (W3C) works today includes a “go look over there” that may have more complex agreements. Timid Robot Zetha expressed in creating models of reciprocity and that these might be very valuable for avoiding a data winter.

Mark says that we should probably start here, given the aggressive timeline. We might ship a minimal core, and then have extended work done after. Timid Robot agrees with that view, but wants to ensure that we don’t prevent the future.

Martin notes that many in the publisher industry want to say “on my terms only”, which basically means the start of the negotiation is a default no. If we do that within the tri-state framework, that lets us do that and keep going. (Bradley) that may gets us squarely into the search space, since there may be a bifurcation between search vs. AI model training. “No, but” is a critical starting point.

Leonard notes that there is active work going on in the EC on machine readability, and that we may need to be sure that we meet that requirement. If we don’t do enough core work up front, the folks waiting on us may not get enough progress. Suresh notes that there can be side-efforts in which smaller groups can make progress. Mirja notes that there may be very different things in the future, and things like AI search are emerging rapidly. Bradley agrees that this is one of the more complex pieces. Matt says that where the content is being presented is very different in AI search vs. historical search. Mirja says it is changing fast, and that we may want to focus on the properties. Bradley says we know what it looks like now, and that it will evolve as publishers and others find things that they are comfortable with. “No” category is the most important piece to get right, and that is always up for bilateral discussions. Mirja notes that a default “no” is a different dynamic in the focus and that can be slower than default yes approaches.

Alissa asks whether the machine readability was for contact or was something else? Leonard, no it is to declare detailed rights, including things like charging model. It is intended to be an extensible, machine readable system, he will look for a link.

Ted points out that we are in a rathole. The key is what someone/thing does when it has a preference. robots.txt says some things about conditions. We could associate conditions with a nonce, crawlers could present that nonce when accessing content and servers could adapt based on their understanding of the value that was agreed. There are things we could do here that is minimal; not tri-state (silence is always problematic), but opt-in could be associated with a set of conditions. That could be much more expressive, relatively cheaply. Maybe we should talk about what we expect from the vocabulary than the context in which it might appear.

Paul suggests that we might go to discussions of what are in the drafts and focus from there.

Glenn suggests that we include sections in the vocabulary draft that document the tri-state model or whatever model we are actually working from. Suresh notes that we may want an indication that someone has seen the preferences; Paul replies that this probably doesn’t belong in the vocabulary draft, since its ontology might be useful across different systems (not all of which would be crawler-related). We are concerned with how crawlers interact with these here, but there will be others.

Mark agrees that we are having a wide-ranging discussion now, but we will try to focus in soon.

Joe notes that robots.txt is not enough, but that the problem is not so much new tech, but that existing tech is being used in news. There’s also an asymmetry in that once something has gone out onto the Internet the data never goes back. He re-iterates that there is really a need to start with limitation. Speaker from microsoft agrees with Joe that we want to start from default no plus opt-ins, because that is the most realistic way to handle new technologies. Sebastian then notes that he believe a default “no” results in some additional issues, including potentially public access to contact information, which may be problematic. He sees opt-out as a potential default, but believes we need opt-in as a defined signal.

Martin says that it seems we’re not all clear on how the different proposals work. We may want to spend some time this morning orienting folks on that. Timid Robot says that the issue Joe raised, on “my data is on the Internet and I can’t get it back”, that should be an expectation that later uses of crawled data should check current usage permission (using Common Crawl as an example). Mirja notes that we’re not really focused on the crawling, but on the uses. Even the baseline crawling is a parallel use to human.

There was a short discussion reviewing the previous discussion of expressions from a crawler that they have reviewed the preferences. Mark is concerned that some of the proposals there may need to be after the delivery of the initial documents because they start to create negotiation mechanisms.

Glenn wants to discuss the value of opt-out vs. opt-in. We are seeing some rapid deployment of new business models, and the opt-out default gives us time to resolve whether or not a new use is within the rights held in the content. A current example is the actors’ ability to withdraw consent from use of training using their likeness, but there may be others coming as well. “Opt-out” would have made that very difficult, because it is not possible to opt-out to things before they have been created. Default opt-out with carved out opt-ins is the easier one to deal with.

Mark says that there are legal regimes that are opt-in or opt-out and that we can’t change that.

Gary reminds us that we are writing these for crawlers that are wanting to be well-behaved, and that crawlers that want to misbehave can do so trivially. Bradley thinks we are getting tripped up around opt-in or opt-out, and that we cannot change the differences between US fair use and other UK or EU. But we can express what we should do when there is no signal. I don’t think we can think about it in terms of opting-in or opting-out. We should say “no signal means jurisdictional rules apply”, as that is the clearest thing we can do. There was a short discussion of the EU copyright/AI copyright act implications of the absence of signal.

Paul builds on Gary’s comment. People are conflating two issues–crawler misbehavior and crawler preference review. We cannot deal with misbehaving actors directly, we are dealing with problems that are lack of clarity of how to send signals to good actors. Gary agrees and believes that this will be increasingly important. Paul notes that this is a fairly critical thing for future work.

Ted agrees with the point about well-behaved bots. We need to be careful talking about the importance of having a clear set of signals. We are saying that these signals existing allows us to have people who ignore those signals being treated differently. That might include turning them over to the AI slop generator… All of those things are outside of our first task, which is defining those clear signals. Think about avoiding foreclosure on potential future development. It is maybe not a good idea to get into a content negotiation structure, but we should be able to version things. That would allow for the expansion to a richer set of signals in the future.

Mark as chair says that we want to allow some of the side discussions without blocking or distracting from main deliverables. Need to discuss how we enable that.

Suresh follows up to note that versioning may create a need to handle a more complex state machine than simply stale nonces.

Matt from FT we can’t legislate for China, we can only set things up so that folks can detect whether or not the signals have been obeyed. Mark Nottingham notes that audit was explicitly ruled out of Timid Robot asked that we have a second use case than crawling. Mark said that when we get to attachment we will get that.

Bryan Newbold drilled into the need for a vocabulary for meta categories like timestamps before which something becomes public or state. Suresh notes that there was conversation about this earlier, and asks him to raise specific issues that were not already covered.

Mirja reinforces that the legal framework can override the preferences, and that we need to have vocabulary that doesn’t elide that.

Hirochika-san notes that we need to think of the agent-type AI, this is a different problem from copyright, but it still needs to consider access control and server performance.

Alissa wants to put a fine point on something that Paul said: the point of defining these terms is to support good faith actors on the crawler and content creator side. We’re doing this work to enable good faith actors to land in a better place. That set of signals will then be used in other ways in many different jurisdictions. We may be able to foretell how the jurisdictions will rule, but that should not bound or drive what we decide to do.

Fabrice note that there is a clear need to communicate globally about what organizations like Google or Microsoft are doing, and that this vocabulary can help. How other uses develop will over time.

Glenn Dean agrees with Alissa and that we should focus on good actors. As a studio person, though, one of things we have to deal with is that we have good actor crawlers and creators today, and we have bad actor content publishers. We don’t want to get into a situation where the bad actor publisher can release content that neither of the other actors wanted to permit. He doesn’t want that outcome. Alissa responds that there are site actors who are currently blocking everything now who would do differently if they had more granular. Mark says it is not what we want to do, but what we can do with technical means. Martin notes that one of the worst features of robots.txt is that it varies with the identity asserted by the user-agent. He references the case of Brave using Googlebot’s rules, even though their uses may not be the same. He is concerned with asserted identity being a primary feature of the vocabulary, because it is discriminatory and might prevent the entrance of new market participants.

Gary also notes that Google published crawling ranges and that they had a situation after one of the ranges was released to GCP, and a company was crawling as Googlebot. Martin that bot authentication is separate from what we are doing here, but that it is an important part of the work and that the robots.txt user agent is adversely affecting folks who are using.

Farzaneh is glad that we (Alissa) brought up the good actor discussion, because we have a lot of other discussions about structures of control and focus on bad actors only. But she does have an issue with it being a binary description. There is a need to be a bit more contextual, like non-commercial uses and some of the less commonly discussed actors. The binary good/bad actor is reductive. Mark interprets Alissa’s “good” to be conforming to the protocol and “bad” as not conforming, not as a broader statement.

Timid Robot plus ones the idea that we should avoid hanging too much on user-agents. They also believe it is impossible to avoid mis-use of the vocabulary; if a website owner is claiming that anyone can scrape material that is pirated, that issue is out of scope for this. They are also concerned that we are conflating content holder and copyright holder. Access to the content gives you the ability to add the signal, but it may or may not be recognized in a specific jurisdiction as copyright holder.

Glenn Deen notes that it is not necessarily about negatives, but can be used in some context to attach a right to something no matter where the content is available (RFC example).

Fabrice jumps to a day two topic, he is concerned that if we focus too much on identification that we will find misuse. See the Deepseek question, where no one was blocking it, because they didn’t know it existed. We need to a way to express signal that is usable by any actor.

Leonard note that he agrees that the identification issue important but out of scope.

Cullen thinks this moving into a more useful direction, and that in our next session we can move toward discussing the syntax. Starting from where robots.txt is lacking seems to him a good starting point. What is lacking from that to express your preferences? Starting from that and thinking about syntax, I think that would help us make progress.

Paul notes that we cannot necessarily divorce considerations of copyright from the work; we need to be able to deal with multiple arrangements. In some, focus on copyrights will be unworkable; in others, there may be a chain of licenses from a copyright grant. We need to be able to handle both.

Glenn Dean wants to highlight use cases that are weird. One is where you are publishing content, but it is not covered by copyright. We need vocabulary to express that. We also need an ability to grant of permission like that. Mark notes that we are not chartered to handle copyright preferences. Glenn says he is not trying to create a general mechanism, but something like a reference. Mark notes that still might be out of scope.

Alissa notes that the reason copyright is in the background of the discussion is in part because of the EU regulations that created a broad carve out for research. That’s not true in other frameworks, but it is having a big impact on the structure of discussions. Leonard notes that when we talk about attachment, we may get to how to bind these signals to objects and that we may get to the intersection these signals and preferences within that context.

Leonard gives an example–if the video has a preference signal, it doesn’t matter whether the video came from Amazon or Netflix or whether, it is present for the review of the conformant user agent.

Gary notes that they would be very happy to see IMAP or email protocols. Google’s email SRE was intrigued by the process.

Martin disagrees with Leonard’s assertion that it doesn’t matter how the expression is distributed. It matters for the distributor, who may have certain terms with those who are uploading the videos. We may well be required to handle the union or intersection of preferences. Leonard agrees that this is required, Suresh notes that this is in the charter.

Timid Robot, their experience is that there are systems that are “first to find wins”, “last to find wins”,(missing method) and least permissive wins.

Glenn asks whether we need to have an expression of territory? How to make the choice on who to trust without that? Timid Robot believes that we have to assume that the consumer has to decide who they trust.

Martin notes that the distribution can become key to how the content provider understands what happens when it is given to the distributor. There is a signal and there is a context, and to get the right result, you might need the signal to vary by context.

Ted expressed concern that attempting to resolve the contextual issue runs a real risk of attempt to resolve things very much out of scope.

Mark asks for a concrete example. Glenn says we have two good faith where different signals are applied based on different actors.

Jari notes that there is a difference between the broader jurisdictional problem and the fundamental possibility of having multiple policies. The former may not be solvable, but the latter can be, using something like strictest policy wins approach. Glenn took an action to write his concern up but that it may as well.

Timid Robot believes that there is a scope issue on whether conflicting signals get resolved; Martin notes that we had a discussion of that during the workshop and that we agreed that it must be resolved. Mark notes that it may very well be an incomplete solution.

## Afternoon session, 8 April 2025

Note takers: Éric Vyncke & Jari Arkko & others

### Summary of morning (Mark) 

Wide ranging discussion and some convergence. We need to make progress though. Let's focus on the items we have on the table. Which content in the vocabulary draft ?

Two drafts about vocabulary as a start:
1) draft-vaughan-aipref-vocab-00 (Thom)
2) draft-keller-aipref-vocab-01 (Paul)

Mirja proposes to quickly present the drafts.

Leonard (contributor to Thom's draft that leverages also Paul's draft.

### draft-keller-aipref-vocab-01 (Paul Keller)

[draft](https://datatracker.ietf.org/doc/draft-keller-aipref-vocab/)

[slides](https://datatracker.ietf.org/doc/slides-interim-2025-aipref-02-sessa-proposal-for-an-opt-out-vocabulary-draft-keller-aipref-vocab/)

During the presentation

Farzaneh (chat): " despite the context of how this vocab came about (the EU laws) it's jurisdiction agnostic?"

Alissa (chat): "who were the various constituencies represented", Paul: Chatham house rules so no attribution but various parties

Paul: Retrieval-Augmented Generation (RAG) could be added under Text & Data Mining (TDM)

Glenn: what about LLM learning from another LLM ? Martin: should carry over the original policy. 

Farzaneh: is it similar to derivative work ? Glenn: not really. Paul: the I-D is mainly about use classes. Leonard: difference between training the LLM and using the LLM.

Discussions went in copyright and generative AI... No minutes taken as it is outside of this WG.

Mark suggests to have a limited vocabulary to have simpler policies by reducing choices.

Brad: should leave all doors open, e.g., for RAG, but start with low hanging fruit like training.

Ted: this I-D is good enough to start working. WG should wait for vocabulary to stabilize before moving to actions.

Joseph: should we include use case vocabulary (specific use case) that won't have any actions associated to it ?

Leonard gives the Studio Ghibli example that may allow for training but not for "styling".

Farzaneh (chat): "1) clarify it is not EU centric, 2) expand the focus from rightsholder preferences to site operators (or call it something else)."

Jari: I want to make an argument that inference is actually vey important for end users. They want to use Ai tools and automated tools to explore the content in the Internet, we shouldn't cut them off by setting them the same bar for using information as the large AI companies. Inference is also a fluid concept, not easy to define. I see three options: 1/ just include training and say inference is not included, 2/ define inference and have it in the vocabulary, 3/ adopt Alissa's model of what the impact is to the partipants (e.g., linking back vs. not) rather than talk about the specific technologies like training. 

Alissa: do you have a definition of "AI model", Paul: using GPAI definition. Gary: "AI training" is way to broad (e.g., Gmail spam filter is somehow also AI training).

Alissa: how often do we expect content owner/distributor to change the preferences ? 

Martin: the active training is not so interesting for owners, but it mainly about the use of trained LLM (e.g., used by the competition).

Piers: Pointed out that AI models result from training on large scale data and usually include fine-tuning with other data potentially by a range of actors (e.g. Open models). Mentioned that inference involves processing of model context which can contain data from various sources (e.g. RAG). Suggested that much of search may include some AI aspect. Support adoption with some modifications to include inference/RAG in the vocabulary.

Matt: does text summarisation count ? support adoption with adding some use case

Paul: about inference and other use case, he agrees that the I-D needs to be extended to cover other terms. While the I-D started based on EU, it is actually global. Also need to strike a balance between extensibility nad being broad.

Timid Robot: important to define when preferences are stalled. This is a good *basis* for adoption.

Mark: wondering about other use cases that may be important for EU but not for this WG. Paul: vocabulary does not mean that implementers need to implement everything. Mark also see the context quite abstract and high-level.

Leonard (chat): "A LOT of countries have (or are) adopting similar terms/concepts - EU, UK, Japan, South Korea, Singapore, & Australia for some..."

Brad: TDM should be a seperate use case, should define in details specific options for specific use cases (beyond the EU). OTOH should we care of problems that nobody cares ? Also support adoption

Joseph: also supporting adoption, a lot of other use cases (not in the draft), he likes TDM as a category

Martin: need to be flexible for evolution of the draft. Paul: sure, the pre I-D document was not intended to become an I-D, so, can be flexible.

Fabrice: very good start, publishers should also have their say, be more explicit in the text

Farzaneh: need a text that is linked to some jurisdictions. Bypassing the AIpref could make you liable in courts (even if not enforced by IETF protocols).

Timid Robot: about inclusion of TDM, how preference interpretation is important, i.e., TDM is important as a global container.

Suresh: +1 to use as starting point, likes having a top-level category, people care more on the impact on them.

Cullen: +1 to Suresh, hierarchy is important, support adoption

Mark: we can very little think about enforceability

Paul: finds a that "AI training is not useful" statement is from publishers.

Alissa: is there really a subset hierarchy ? Q: do we need to talk about "agent", Martin: I do not think so, Leonard: we should talk about even if we do nothing about it

Matt: unsure whether other use cases are all in TDM use case

Mirja and Paul discuss about the inclusion of "AI training" class in the I-D. Mirja is unsure of her support for adoption

Mark has kept a list of topics to be discussed based on the previous points: inclusion of TDM, time span of preferences, ...

Discussions on whether the EU source of languages is OK as long as it is not exclusive.

### Vocabulary Issues (lead by Mark)

The previous round of discussion generated this list of issues:
* Search / discovery carve-out
* RAG / inference-time / agents
* TDM
* Eurocentricity
* Nesting / hierarchy 
* What is AI / definitional questions
* Mapping to preferences
* interface to attachment - abstract model or strings?
* time dimension (attachment)
* spam filtering / offensive language / other "good" uses
* weapons / biometrics / other "bad" uses
* How to split between vocabulary and attachment (added by Martin)


#### Interface to attachment - abstract model or strings?

Leonard: serialization/parsing is different than an abstract model.
Mark: default serialization in appendix when specifying attachments
Ted: should there be a "registry" of serialization for the abstract model ?
Suresh: there should be one recommended serialization

Martin: [structured fields](https://datatracker.ietf.org/doc/rfc9651/) (in his draft) are consistent in interpretation and add a lot of expressiveness

Mark: abstract model with one RECOMMENDED serialization (consensus in the room it seems)

#### Search / discovery carve-out

Mark: our WG is about AI pref and not search pref
Martin: robots.txt were done originally for indexing only. He is concerned that we cannot re-use robots.txt without including "search" in the new model.
Mark: Paul excluded search because of robots.txt 
Brad?: search is indeed no more only about search
Alissa (volume to low for the note taker)
Ted / Martin (chat): "a search application directs people to the original location of relevant content as part of its operation one might even say "as the primary part of its operation"
Timid Robot: if we have TDM at the top level than we need to include "search"
Leonard: agrees with Alissa about "AI usage" and not "any usage", robots.txt is just a way to signal
Gary: robots.txt is more than plain search/crawler, e.g., even "curl" supports it. robots.txt is a good attachment place. Fabrice: even a single crawler can serve for multiple purpose.
Fabrice: we added co-pilot search, i.e., augmented search by AI. Agrees with Gary about the usefulness of robots.txt

Martin: the challenge is whether we include it and with which granularity. Support [Ted's comment on search definition](https://datatracker.ietf.org/doc/slides-aicontrolws-crawlers-adversaries-and-exclusions-thoughts-on-content-ingest-and-creators-rights/)

Fabrice: search is not only search, it is also for AI
Cullen: is search just "AI training" ?
Mark: unsure whether training is more generic than training
Martin: perhaps no need for strict hierarchy but overlapping concepts
Ted: data acquisition has not changed for years, data processing has changed a lot though (with ordering), but always giving you a set of URL, and now also gives answers in addition to locations. So, the preference should rather be on actions "allowed" on acquired data.

Matt: concerned about more than attention, but also being misrepresented or associated with fake content that has no relation to truth
Timid Robot: ?
Paul: inspired by Ted's point of usage, if it is not about search, but about finding something or being pointed to something ("findability"). For search, you can search for many things other than (content) locations.

It should be possible for us to have an "on" button for allowing traditional search in the context of TDM. 

An example: a social media company is creating a search index, but internally what actually happens is that it creates a RAG index.

Speaker notes that they believe the line is when the returned data is a summarization of the data.

Martin: Not clear what the line is. Can you clarify.

Speaker: the line is whether you use it for search or for some other purpose. The summarization is different depending on whether you try to report finding content vs. actual content.

Mark: There's a summary even in a search result, provided before the link.

The were was a period when Google wanted to change the headline that waas listed in the search result. Different headlines may mean different things for the publisher, if the publisher's material is summarized.

A new structure was shown in the screen, with tdm being the top level structure, and then divided between three partially overlapping three structures, AI training, inference, and search. And then genai training be a subcategory of AI training.

Alissa: One thing that emerges is that it is really important that the categories are discrete and meaningful for the people who want to express the preferences. Does it allow publisher and content creators to express what they want to express? We need to consult publishers to ensure that this matches what they can use.

Alissa: Another issue is not really about actions, but faithfullness. Will my content be used in a way that it is guaranteed to be represented in a faithful way.

Paul: If we go to the new diagram, there's still two conceptions of search, one being the old style pure search and the new generative-AI driven search results. These need to be distinguished from each other, unless the old style search goes away soon.

Martin: I was talking in the new diagram mostly about the old style search.

Paul: The other, newer search could be seen as something that the publishers don't even want to be part of as it creates a possibility of brand-damaging hallucinations.

Hirochika: how to express preferences around multimedia?

Ted: You should be able to express preferences for any media type. Martin: Right, if you can express preferences about text search the same should be applicable to image search.

Timid Robot: We are dealing with the intersection of two misleading terms. We talked a lot about how to clarify the term search into its components. If it is a summary or links or a portion of a page. But I think the other part of the problem is AI training. I guess I would want some clarity on what the latter means. Everything is AI based, we use AI to mean any kind of analysis as well as a way to generate new. What qualifies as AI training? Is there value in talking about AI training at all, since it is so amorphous. Maybe go back to analysis and action terminology after all?

Leila: If we don't worry about the terminology but just want to know where the line is. Then the line is whether you generate summaries. And I note that we initially had the purpose of this effort be about AI training, and now we are talking about not even having that term. And who is in control, could a publisher control downstream usage, e.g., whether their material can be used in for heart disease but not lung disease research.

Timid Robot: If we don't control downstream use, publishers will just opt out entirely.

Speaker: what fraction of web users care about the opt-out aspects, given that most users are on social media where this doesn't matter. How many users will actually be affected?

Gary: The largest fraction of the Internet is on a publishing platform (e.g., WordPress). Usually they add these opt-in/out settings for everyone. For instance in WordPress there's a setting for opting out of search. Quickly after AIPREF work completion, we could easily have 40% web adoption, given these large players.

Paul: We are handicapped by the people in the room, not too many publishers for instance. There's a lot of people out there, e.g., visual artists. Large classes or rights holders are not represented here.

Glenn: When training become more common, they are going to want to opt out of training. They would like to participate in a bigger market place, but are too small participate for instance in court cases involving material usage. One of the outcomes for high value content is likely opt out. For use of their content they will create point-to-point agreements outside the open internet, and for the Internet the policy is "not allowed". If this becomes the default, is that the outcome we want? For the broader internet and all of us?

Ted: We can't see anything that goes inside search and other companies analysis process. We should de-prioritize our work that affects things that isn't observable. We don't know what processes are going on in internally. Or how it changes. We have to focus people on what they can see and observe.

Alissa: I want to respond to Paul and Ted. I don't hear anyone advocating for not including AI training. Only advocating for an additional category of search.

Speaker: A lot of people are on publishing platforms they can't really influence the preference settings, but given tools they might actually want to opt in.

Wrapup: how did remote attendees experience the meeting? Farthest people from the mic were a bit soft. Also, stating names would be really useful.

Tomorrow morning we will continue dealing with the issues, and then continue with the attachment question later.

We expect draft to be adopted in a week, and then we will continue addressing issues in the draft.

Tomorrow start at 9.15am.

## Morning session, 9 April 2025

Note taker: Joseph Bradley

Agreed to work on vocabulary 

Reviewed names + affiliations 

Abstract model + suggested serialization agreed from yesterday. Also covered carve out for search + discovery. Concluded that we probably need search in our vocab. Paul's proposal suggested for call for adoption.

Started on RAG/inference time use cases. Noted that Paul's proposal doesn't contain language for these cases (yet). 

Paul points out that the omission is partly because the suggestion came too late. But the impactful reason is that inference/RAG is poorly defined and covers all possible uses of material after training. E.g. can an end user of content translate that content with an ML model? This issue has the potential to slow us down - if we want to ship by August we may be better leaving it out. 

Glenn asked why this slows us down? Leonard pointed out that deeper vocabulary affects how users will interact with the protocol and how the protocol evolves over time. Glenn asked what we need to make hard decisions about between now and shipping. Mark also thinks it's possible for us to add vocab later, subject to engagement with the policy community. Standards not useful if they're not finished! Risk that we ship something unfinished and people move on. 

Sonia expressed concerns that categories are too broad. We might want to focus on generative AI training as that has brought up most of the concern - same for RAG.

Bradley replies that skipping RAG would miss concerns from e.g. publishing concern where RAG is the number one issue. Queries whether RAG is actually that fuzzy. Work of the group risks becoming irrelevant if we miss RAG/leave it to 2026. 

Ted - we are too robots.txt focused. Vocab on acquisition can be taken from robots.txt. We should expect that non-HTML content will have similar acquisition models. What do we expect content *users* to do in terms of carrying these requirements forward? We need vocabulary that commits people to carrying these requirements onwards. This matters in terms of RAG/inference vocab for when we consider e.g. fine tuning. Content users need to re-check requirements every time they do acquisition, analysis, etc. 

Paul - not all of these issues are about vocabulary but about expectations, enforcement. Recognises Bradley's comments about importance of RAG to publishers. Notes that OpenAI users different bots for training and 'agentic' purposes. Not standardizing the agentic space would fail the WG. Challenge to Leonard - are RAG and inference the same to some extent? 

Jari - initially thought that we should focus on model training because users want to use RAG to inspect documents. ATM RAG/inference covers everything from trivial 'copying' through to translation, summary. Large context windows may make RAG less relevant but also puts more pressure on using content in prompts. 

Piers - RAG is filling the model context after a user prompt. Need to consider the value proposition around that kind of material - typically the useful information is recently published (e.g. news media). This means that rights holders may feel differently about permissions at different points in time that can be expressed by differentiating RAG/inference from training. 

Leonard - C2PA introduced inference as an option based on user request. Adobe creatives are very concerned about e.g. style referencing - usage is the important thing. But uses like 'summarise' are not treated in the same way even if the C2PA manifest has the 'no inference' flag. Suresh asks if end users can override owner prefs - answer is no. 

Fabrice - MSFT only looks at robots.txt for disallow, meta tags much more important. 'no-archive' takes products out of almost everything. May be sufficient to move forward with this. 

Hirochika - RAG is very important in Japan because copyright law is very different. All training is basically allowed but there are more restrictions on inference. 

Glenn - uncomfortable with us limited conversation out of RAG. We should attempt it even if we have to refine it later.

Timid Robot - do we need to distinguish training that happens at different times? Can we instead focus more the the specific interactions between data and a model? For example: the way search products summarize content during training and the way prompts summarize content because of prompt interactions can be treated the same way.


Joseph - it is important that we address RAG.  should differentiate also from user prompting - no need to contact the "originator".  Especially important when dealing with agentic systems. How do things like "pay for view" apply here as well?

Suresh - coming up with definitions is the key point!

Mark - no different than previous arguments in copyright 

Bradley - learning the extent to which different uses (e.g. news summaries, style mimicry) are sensitive to content holders. Move to actions (uses) is happening in the group. This is perhaps a more achievable approach. 

Leonard - brings up Mark's point that we can add/remove things in revisions. Leonard points out that deprecation better idea bc we need the labels that we have to last forever, or we have a 'stranded permissions' problem. Mark recognises this. 

Sonia - RAG isn't as broad as inference, but it definitely is broad. Impact on safety, accessibility, spam filters, general adoption. European Accessibility Act comes into force - if a user has a tool that describes a website, is that RAG? Suggests that we can control style mimicry at the output level rather than w/ training data. Focusing on use cases safer than trying to define massive terms like RAG, training, etc. On Japan - gov confirmed that RAG is permissible as long as it does not copy expressive content to the end user directly. 

Suresh - this was covered a little yesterday - owners may express preferences but there is no guarantee that these can be enforced in Japan.

Sonia - this is an important point, need to factor these things in bc our definitions will affect legal adoption. 

Sarah - if we don't have options for RAG/inference, we risk closing down content bc people will go to the fallback. To this end, imperfect definition may be better that we refine over time. Sonia says that TDM fallbacks could be worked around via temp. copies exception.

Mark - people are clearly interested in this. Ted has identified a use-case framework a promising but a moving target. Timid Robot's point about the time of use has not been explored as much but is promising. Wants to know people's reactions to this choice. 

Timid Robot - clarifies that they wanted to ignore time and focus on the interaction. 

Jari - wants to highlight the balance between end users and content/rights holders. Not sure that agentic framework does help users, who want to use these tools! Harm for publishers comes in the style copying 

Discussion on Jari's point about the definition of publicly available, whether we want to give agents legal status, the goals of this group wrt copyright law. Mark points out that people can ignore preferences! 

Glenn - we aren't setting national policies. These are *preferences* - not enforceable rules (by IETF). But these preferences will be discussed in policy and legal forums and will evolve. In music this evolution happened but not because of perfect preferences were expressed on day one! We should try to be liberal and expect the discussion to evolve around us. Let's talk about uses - this what the person specifying the preferences can understand. 

Ted - we are making an acquisition time signal. Notes that the group hasn't made much ground this morning. We might be able to do a lot with accessibility carve outs. 

Suresh - even if preferences are expressed ppl can ignore them. 

Ted - we need to understand at what level we need to express preferences so that they are not overly restrictive. Echoes Sonia's point - if everyone starts to opt-out of TDM that would be a disaster. Transformations for comprehensibility are reasonable use case! If we have too high level categories they will be too coarse and ppl will opt-out of everything. Recommends a tour-de-table to summarise this. 

Mark - not keen on such a tour right now. Too fine grained options will be un-usable. See P3P

Ted - P3P was itself a response to something stupid. But we need to address these issue or we will not get anything done. 

Mark - 'every use of AI' is an unbounded set and therefore needs to be avoided. 

Paul - largely agrees with Mark's comments that we risk going too granular too fast. No universal agreement on what is a useful use case, and which of these use cases should be permitted under copyright law. This will be a source of huge disagreements. Avoiding RAG will leave a gaping hole in the vocabulary. We get flexibility via 'preferences' - good faith actors not bound by the law can interpret preferences flexibly (e.g. for accessibility). Adobe is an example of an implementer that takes things strictly; this is OK! But this flexibility is useful for us as standards setters.

Suresh - Alissa's point that the other draft is useful is a good one! Ted's 'yes if; no unless' framework is powerful. 

Cullen - the need to enumerate all the use cases conflicts with our goals to meet the timelines. As a group of engineers, we must remember that most consumers do not have this level of literacy. Most robots.txts are not consistent with their ToS! Categorisation at a higher level makes sense. The timing model is a promising one - decouples the data-aggregation from the application stage, which often determines how data is used. Distinction between pre-and post-training applications useful. 

Piers - originally mentioned the time framework. But related to time of the data's publication; not model deployment time. What type of use can go down a rat hole.

Mirja - need to ask whether it is actionable (by user) and understandable (by content holder). For AI devs, easy to distinguish between training and inference time usage. Also easy for content holder to distinguish the value of the 'most recent' data. Third case where you say don't use my entire corpus in the training data but you can RAG me for citations. Timing questions risk becoming arbitrary.

Mark - time less concrete at the training stage ('homeopathic'). But at inference time is concrete and the transformative case is the source of discomfort. 

Glenn - need to walk away from the rights idea; we are expressing preferences. We need to consider what users are going to want to use!

BREAK 1045

RESUME 1100

Mark - in the spirit of Ted's suggestion, let's go around the room for the one thing you would like to see in the shipped product. 

Eric - risk of being too fine grained and too complex for end user and us loosing time. Need to get to a grammar ready for serialization. 

Leonard - need an abstract data model, including set of course-grained options available. Avoid user agent specific instructions. 

Timid Robot - would like to see vocabulary where we have 'thing = action', e.g. 'genAI = no': vocab needs to be robust enough for consumers to provide their own answers to both sides of that formula. 

Hirochika - AI still emerging, but we need to work on the current problem to be solved. Balance between coarse and fine grained to be determined. 

Jari - we can achieve a coarse grained vocabulary, need extensibility also. For inference, we can maybe agree on something with a qualification, e.g., 'inference for content re-generation'. 

Ted - pass for now, see earlier comments. 

Farzaneh - group needs to come up with limited but inclusive vocab by August that addresses issues from stakeholders. Stakeholders in the room have varying interests; doesn't think that that will stop us from coming up with useful vocabulary *if we keep it limited* - don't try to address the entire future. 

Cullen - coarse grained approach is a good approach with extensibility later. 

Mirja - content owners want fine grained vocab based on their understanding/assumption how an AI system works, but we must appreciate that data consumers may have different perspectives on what they are doing. Categories must be actionable by content consumers to match expectations which maybe more coarse grained.

Joe - need to decide what we want!

Sarah - coarse grained framework including inference/RAG with defaults to TDM exceptions. 

Matt - wants to see RAG. FT publishes a lot outside of the paywall and this is good for the open web. Publishers are less likely to continue publishing without paywalls if there isn't the ability to signal to third parties that scraping journalism outside of the paywall is not permitted. The absence of a RAG signal likely to see less content made available on the open web. 

Brad - need inference options. We are trying to target value extractive, substitutive uses - vocab should reflect that. There will always been 'unless' clauses; need to accomodate those. Purpose based restrictions difficult because purposes evolve post acquisition. 

Glenn - need to avoid trying to set policy. Uses is where language needs to go. That's certainly what rights holders are thinking about. We are not writing the grammar for us - must bear that in mind. Coarse grained is probably the option with extensibility. 

Paul - as coarse as possible. Rights holders will often say no by default. But need RAG/inference otherwise there will be a massive gap in the standard. 

Sonia - MSFT supportive of rights holders withdrawing their content in general. But inferencing will be very important for AI adoption and this hasn't been fully considered. A full audit of inferencing and what the implications of restricting inference would be. Opt out should be for genAI. 

Gary - coarse, simple solution that works for majority of publishers. Also must work with AI operators. 

Fabrice - short, crisp vocab. Could list N options for publishers that cover most use case. 

Gary - the opt-out must be understandable for publishers. 

Mark - for the inference issue? 

Fabrice - clear friction on LLM, but is in the past. RAG is more complicated - e.g. visibility but no text changed. So we can tackle the inference question with these use cases. 

Alissa - what is achievable and effective is a small set of categories. Paul's suggestions plus search (including stipulations about faithful reproductions), inference (which probably includes RAG). Distinguishing training and inference starts all the other conversations, and legal jurisdictions can set exceptions. Saying no in preferences does not kill accessibility. 

Bryan - answer on the order of a handful of delineated categories. Need to be able to iterate on the whole thing. 

Piers - echo Alissa. Minimal coarse set of tokens/vocab. Inference important. RAG is a mechanism that brings material into the inference time - could we stipulate rules about referencing/reciprocity? 

Sebastian - agrees with what has been said - need a minimal approach for August. Pressing issue, time is of the essence, and must align with legal needs. These broad categories have support from rights holders. Can add extensions/exceptions as we want. Same principles regarding training and RAG. Can extend minimal version later. 

Martin - no sensible way for us to do fine grained. Split on inference. Many of the applications we are thinking about will not have the ability to respond to these preferences. 

Mark - sounds like there is interest in addressing inference. But we have a preference for keeping things coarse grained with extensibility open. At this point we need concrete proposals. What would the vocab definitions be? How do we describe them? How do they fit into Paul's draft? People need to go away and write those proposals and discuss them in the mailing list and future meetings. More substantial contributions should come in internet drafts. 

Paul - it would be good for us to look at existing systems. Whatever we say will have a standardising effect but interacting with what already exists. 

Glenn - be aware of IP issues when you suggest things!

Leonard, Jari, Ted, Martin, all interested in making proposals for inference or search. 

Glenn asks if we can work on Github. Mark points out that Github is not a canonical form of information for this WG but we can work around that. 

Martin says that people should focus on getting drafts out to the list. 

Suresh - refer back to previous proposals/drafts for ideas and copy. 

Mark - this is a path forward for search and inference. Looking at the vocab issues, we seem to be OK with TDM as a high level category. Have spoken about 'good uses' but seems that we don't want to address those now. This is a potential unrealistic rathole. But our framework should be extensible to these issue in the future should we wish to address them. Room agrees. 

Mark - for eurocentricity, this seems to be an editorial issue to come back to later/will be ironed out. Paul seems to agree. 

Mirja - TDM term is the big import. 

Paul - SG and Japan use it too (Martin: 'escaped into the world').

Mirja - TDM comes from an era before AI, so we may wish to define something better. 

Paul - a number of jurisdictions use this term though. It also has some overlap with AI. Convinced that you cannot do vocab for this without mentioning it (in vocab). 

Mirja - can be mentioned but not implemented. Does not to be 1:1 with copyright law. 

Paul - these jurisdictions trying to build copyright frameworks. Cannot be ignored. 

Farzeneh - copyright should not be the centre of our considerations. Need to consider practises around the round. Need to avoid Brussels affect. 

Paul - these are prefs that may not have legal backing and can be ignored when legally permissible. There is no legal context that forces me to respect all rightsholder requests. But I might be amenable to complying with targeted concerns about e.g. genAI. For this to function in legal concepts we need to reference TDM. 

Mirja - it can be roughly similar to TDM but doesn't have to map directly to TDM. We can explain to policymakers why this different definition is needed. 

Suresh - examples would be great. 

Mark - diminishing returns. This is an open issue to which we (and editorial) will return. 

Brad - we can't avoid using TDM. The 'nesting' idea may be too strong for the legal context/intention where reproduction and displacement are important. 

Mark - let's discuss nesting. 

Glenn - before nesting: concern I have around euroconcentricity (and other regional focuses) is that we will pull in policy decisions that don't apply here. New terms free us up for past decisions. 

Martin - important to realise that some uses are string subsets of other uses. This helps us because we can inherit preferences. But that's not true for search which is a composition of technologies. So nesting is a useful concept (allows granular expressions in the future) but we can't rely on it for everything. 

Mark - rough agreement on nesting hierarchy or not? 

Mirja - not convinced that there is really nesting here. 

Disagreement in the room about the external consistency of Martin's nesting model of AI uses. 

Martin - definitions may not correspond to what people are thinking of! 

Paul - not sure we can say that; depends on how we define inference. But there will be some nesting from the broadest level, and will be necessary. 

Mirja - these are still preferences, open to interpretation.

Suresh -some of these combinations will not make sense. Becomes harder to maintain the model if we have no sense of what is most specific, which will matter for combinations later on!

Martin acknowledges this. 

Alissa - this diagram doesn't have RAG in it, but by including that we can to six 'things'. Nesting may be making this these harder to use. We can achieve the same thing by having very clear definitions. Makes combinations potentially easier. Whilst it might be fun to consider the structure of these six uses, it may not make the MVP easier to ship/use. 

Paul - there must be *some* nesting - otherwise how could you opt out of TDM but not inference? 

Alissa - this depends on you having a clear definition of TDM already. 

Paul - this depends on the definition from the EU, which is designed to be a superset of other uses. This is where the nesting idea comes from. 

Brad - not sure that's true. 

Alissa - if that's true, maybe that's fine. The other five could be a subspace of TDM? But there still seems to be disagreement (e.g. inference). Important that users can distinguish from each other and user can make decisions about (dis)allow). 

Timid Robot - going to be hard to avoid subsets. If we try to avoid this the vocab will be very verbose and hard to use. Hierarchy adds value in terms of describing generics. Enables content holders to avoid having to describe specifics. 

Paul - seconds Timid Robot's comments. 

Ted - extensibility has been mentioned in the chat; strongly agree that if there is no structure amongst the terms then expression becomes harder as the number of terms increases. Examples is en-XX, which is very helpful. Will also be helpful when data is found, with preferences attached, in the wild. 

Mark -want to avoid defining AI before lunch! Mapping to preferences TBD; this will come with attachment. Happy to hear about time but thinks that this is about attachment. 

Glenn - we need a timestamp in preferences. 

Mark - this is attachment mechanism specific presumably.

Joe - disagrees. Leonard discusses this

Mirja - doesn't matter since when policy was deployed, just the it exists. 

Glenn - disagree. 

Mark - not sure we can discuss this before lunch. Why does this matter for the vocabulary question? Can people write use cases? 

Martin - think timing would be a mistake. there is no need beyond content based preference expressions. We stand the risk of making this far more complicated than it needs to be. 

Suresh - distinction between time of policy creation and policy duration. 

Glenn - I don't know what I want!

Paul - not sure what is wanted to time. No time dimension to preferences? This is an attachment thing. 

Glenn - doesn't mean I disagree.

Joe - would like to see use cases.

## Afternoon session, 9 April 2025

Note Takers: Farzaneh and Martin 

### HTTP Header field attachment (unit based)

Mark N: We just need to choose a field name, right?

Joe: Varying degrees of technicality in the room. An issue is that there are these registries, how do I ensure that I hit my preferences?

Mark gives a brief overview about how HTTP operates for those not familiar.  Point out difference between content and content metadata.

Joe: Maybe there needs to be a way for people to choose between robots.txt and headers?  Or point from one to the other?

Mark: It might depend on servers as to which is most able to produce one or other form.  Crawlers generally keep headers.  There are some exceptions where you don't get headers, like MASQUE.  Those protocols might not need to have that connection between headers and content.

Leonard: There are two aspects to headers.  The header is "embedded" in the HTTP part of the exchange, but there is also Link headers, which we use for C2PA.  This enables physical detachment/indirection for the metadata.  We should also consider link headers for this.

Mark: [[RFC 8288](https://datatracker.ietf.org/doc/html/rfc8288)].  The relations can be in link headers and formats, so we need to consider these as a separate form of attachment.

Leonard: We should clearly consider things that are out there today.  An well-defined mechanism for finding preference data is an option we should consider.

Martin: my proposal ([draft-thomson-aipref-sup-00](https://datatracker.ietf.org/doc/draft-thomson-aipref-sup/)) is content related header never really formalized but it was very loose and not about the transaction right now, but the properties of the content. It's a good way to ensure things get attached to the content. If you take stuff off of websites and not saving headers you have lost the info that has used that content. we should talk about situations that loosen the attachment, possibly can use indirection in various ways. This group should not focus on indirection. Header through HTML we can say equivalent of HTTP header is incorporating in the content. We should make it as simple as the expression is. 

Gary: Robots.txt ([RFC 9309](https://www.rfc-editor.org/rfc/rfc9309.html)) is robust and you can set up rules that match specific patterns. If you don't want PDF to be crawled, you can mention that (`*.pdf$`). PDF files in this directory but not the other one. So you can have specific rules. Robots exclusion protocol is robots.txt and x-robot text header. with the URI level controls you can specify a few things some stuff. If you are launching a new header, we will have to figure out how the different headers can work together. For example the header has to comply with GDPR but also has another message. How can two different headers interact with each other. Will be difficult to get everyone on the same page. we are already supporting one set of rules so it can be difficult to follow other rules if they conflict. C
Martin: maybe the robots.txt map cleanly with our definitions. 

Leonard: we should discuss whether robots.txt is the right place to talk about this. If your other preferences are indicated in another file then we have to discuss how it can work together 

Jari (needs a review): At a higher level, whoever is serving content can do the mechanisms and expressing preferences. The receiver needs to understand all of them but even if there can be negotiations ...if you add too many capabilities and preferences in different places, how can the crawler make sure it knows everything

Mark: Registry of attachment? some attachments in our deliverable but not all. 

Glenn: need a list of extensible 

Jari: Another approach: These three things are mandatory and everything else is optional. 

Mark: we need to adjust protocols in the future we don't know all implementation and predict so we need to be flexible 

Fabrice: HTTP Header: used a lot, there is value using no index in xrobots txt, allows the http to be published. 

Mark: When you have a separate source of information authority, operationally the closer metadata is to the data the more likely it's accurate 

Fabrice: we attach the preference to data at the same time (in HTTP header) 

Suresh: wants to do what we can and not going down a path that is not feasible to do 

Jari: reasonable effort to do the three things that we have identified in this group 

Paul: AI developers arguing it should be robots.txt only. the AI industry is trying to make the tools more limited. Will other capabilities be predicted in law or is it the job of standards. The EU AI Act Code of Practice mandates any subsequent IETF standards, is that language acceptable IETF language? Yes it is 

Martin: Paul hit the head on the nail on what is practical: declaring party is a neutral term that makes it good for our purpose. (---) has standing properties we don't have to go (Martin to add)

Leonard: If we have abstract data model and serialization we can connect the dots 

Glenn: Multiple embedded things like audio, video, capturing ... is our intention  to create a single policy set attached to the container?For example, are we applying this to the policy set in the QUIC attachment? 

Martin: proposal here is to attach it to a HTTP provides to a client, it does not touch any streaming, it's a chunk of bytes sent to the client

Martin: some protocols might need to carry attachment (like SMTP) having an attachment for that might make sense. 

Ted: media over QUIC, attach to a specific content, you could also deliver it for an entire session. define media over QUIC, the syntax and the content type but we are moving down in the weeds here

Mark: The analogy is if we want to regulate TV content we are not regulating electricity sockets 

Glenn: Do we need to apply it in QUIC per stream?

Mark: Composite media types are controversial, link relations can talk about a piece of content and making part of something to another 

Glenn: media rich world with different types of media, advertising does it too. Trying to sort through all of this as we are discussing where there will be dragons or opps.

Mark: we will get deep into it later

Suresh: at some point it's a good idea to discuss it later. seems like there is no discussion on HTTP header. 

Joe: Can good faith actor ask who is the rightsholder for this container

Leonard: thats why embedding is better than HTTP Header. Fingerprinting mechanism suggested by Sebastian. There are mechanisms for this that exists out there but then it all comes down to how much you want to retrieve 

Suresh: we don't determine the validity of who can signal the preferences. (implied by the charter not explicit)

Mark: we can speak to the issues but we cannot provide technical mechanisms to solve the problem 

Timid Robot: In the kind of situation Joe said: people who have needs to verify the signals and preferences can use other tools. HTTP header is going to be "container level"?

Mark: Yes it can be either Json, HTML, Txt file. 

Martin: Headers on a Msk tunnel (Martin needs to finish this)

Sonia: if the container is considered part of the content and it's a part of TDM how do you read the message.

Suresh: location based preference that robots.txt state the preference 

Gary: robots.txt allows the client to read it even if it's disallowed. 

Paul: reading a file of instructions is not within the definition of TDM. 

Mark: we are outside of the authority of this WG

Sonia: just to point out that TDM is problematic 

Paul: difference between location and asset based any solution to the problem should include all kinds of the mechanisms but might fill in holes that might arise out of behavior Joe described. we don't need to solve the entire problem space here. 

Glenn: Video services that combine ads and movie (matter of concern)

Mark: when you have many images on the web you still have headers for each image 

Glenn: The policy that I attach to HTTP level to the whole container should apply to all the things I add to it. So the answer would be in that scenario you can do certain things with the content but not with the ad 

Gary: Google has a larger container playlist of different things that browser is going to read. If we see in HTTP header signals we will look at that signal and we won't go down to each individual content in the playlist. For example In a playlist file the first three are videos you want indexed you leave it blank and there is ad following.

Glenn: delivery of content of different types that needs to have different attachment to them is a challenge 

Mark: lets see if we can define mechanisms that can address that later but can't at this time. 

Glenn: fair answer

Piers: If robots.txt signals yes he questions whether that the client has to go to each piece of content to look at the HTTP header. Is the client obliged to check the HTTP headers from then on? how do you combine the two (robots.txt and HTTP), can you have a larger sort of indicator at a high level.

Fabrice: if the signals conflict then we have to talk about how to sort it out 

### robots.txt attachment (location based)

Mark: discuss two things attachment by location (robots.txt) and if we are going to do something newer

[[RFC 9309: Robots Exclusion Protocol](https://www.rfc-editor.org/rfc/rfc9309.html)]

Fabrice: there is no opt out or opt in globally, so we need to address it. All parts have to be listed no ability to opt out globally. Different AI agents have come up with different solutions, Google has Google extended, you have new players (deepseek) looking at stuff and getting blocked. It is important to express allow disallow by content and also by user agent. The key problem is that websites want no AI training. But it should be more granular and have a category for search for example. 

Mark: location and user agent is covered but purpose is not. so if we have a vocabulary it can tackle it. 

Martin: robots.txt has to be looked at by clients. robots.txt is good for signaling a large proportion of websites not to be allowed. This is about setting out purposes rather than knowing user agents and blocking them or not. If we have this usage preference expression and can attach it we have done our job. There are no usage preference on content to date. 

Mark: using robots.txt as long as we can accomodate purpose based preferences 

Martin and Fabrice agree 

Ted: Ted thinks we should leverage robots.txt. But they should consider two things: 1) include preference in robots.txt and to point to another preference/this other file, this other syntax. if you want to rule out a certain part you have to be able to in a blanket fashion and robots.txt does that. 

Gary: robots.txt should remain because of what Martin said. There will be user agents that people want and you need to create exception for them so we need to have user agents 

Martin is not saying that we should unwind user agents 

Gary: so many agents on the Internet that you might need to be able to adjust control for these clients 

Paul: Vocab and ability to express in robots.txt 

Timid Robot: robots.txt should remain, reduce the number of URLs that crawlers have to hit. Is another work group (WG) owning robots.txt?

Mark: no

Cullen: "maybe" to robots.txt. Depends on the schema of the expressions. Need to know when preferences were expressed. Given misconfiguration, expanding the schema, we see a lot that are misconfigured. Does this further entrench that sort of problem? We have to think about people getting this wrong. A separate file, with a pointer, might avoid or at least separate out some of these misconfiguration issues.  seems like syntax constraints might not make it a good fit, depending on vocabulary.

Joe: misconfiguration can happen and we might just need newer tools later. No need for a pointer, if it is a separate file, just load that separate file. 

Piers: robots.txt seems like a good option; referencing might lead to the problem of having to make two sequential queries.  Tying it to user agent... It is being deprecated on some platforms.  He acknowledged that client/browser side useragent issues are less relevant here. How might that interact?

Martin: actions that browsers take don't matter here

Mirja: robots.txt is not modern but reinventing it is problematic. robots.txt is about access control rather than usage  but our issue is about accessing and what can be done after accessing the file. We shouldn't break the access control. it's not about just being accessed or not so we have to consider that. 

Mark: when we started this work, I had reservations about robots.txt and assumed that we'd make a new file.  robots.txt is old and horrible.  Gary convinced me that it was extensible enough for our purpose, but most importantly that the implementations were aligned.  There might be issues, but think it is worth doing.  Need to keep discontinuity of purpose in mind, so that we understand how the history of the format might affect our work.

Gary: I like robots.txt because it’s simple (dumb)

Brad: can robots.txt go beyond its primary purpose and include other actors crawlers and others. 

Gary: defining the actors would be very useful. Would a browser be considered an AI agent? 

Mark: the ability to define different attachment mechanism appropriate for application: doing agentic AIs, look at these attachment doing something else look at others 

Timid Robot: I'm Timid Robot and I'm looking forward to us determining who/what is and isn't a robot within the context of robots.txt

Fabrice: we will break the Internet if all the browsers start looking at robots.txt file. 

Sebastian: We should be aware of the sentiments of who are affected by the protocols 
Rightsholder and creators don't like robots.txt, it doesn't have meaning or relevance. Proposal: the vocabulary communicate the preferences and keep in mind that the tools we use should have the support of creative community. 

Mark: Creating a new format is very hard and lengthy, we can potentially update it (robots.txt specified in RFC 9309).

### The document that we will adopt

Mark:  not going to hold a popularity contest among the drafts we have.  Instead, pick editors.  Have them construct a draft and then issue a call for adoption on that draft.

Martin: we need to take a shortcut, we have to do both together. we need to have an attachment document 

Mark: if we want to do them together later on we can do that too. 

Paul: vocab and one attachment mechanism would be good 

Martin: If we are gonna do two documents at the same time it's fine but will take more resources 

Leo: vocab/default serialization and then attachment 

That's what we are talking about 

Timid Robot: there is value in doing both together; having the second attachment (unit) will inform how we do each in a constructive way. 

Gary: I want to work on SMTP, would it make sense to submit a draft on attachment for SMTP?

Mark: sure, you can work on a draft but the group won't focus on it now 

Bradley: the ID that I was referencing should be coming through today, I just want to make sure that after August it would be read and considered.

Mark: right now we are just identifying starting point and of course later we will consider the other IDs. 

Suresh: we are expecting IDs. 

Martin: Mentioned combination

Mark: we have a discussion about combination and maybe people write IDs and then we come back and discuss

Martin: that actually might be the way, Jari also has a proposal put a link in chat to it 

Mark: as we talked, identified the issues about attachment. Time: which version of the robots.txt should I use at different times, what attachment mechanisms do you look at to determine applicable preferences (where is it mentioned), containers - encapsulated media, 
robots.txt, we don't alter it unless we have to

Leo: are we taking position on embedded preferences

Mark: for specific formats, the venue that have it should look at it, we yet have to come up with a proposal to show the relevant venue 

Paul: IANA registry of attachments

Mark: one is to have a list of IANA attachments 

Mark: a registry to make the attachment mechanisms discoverable. Alternative is we don't do it and legal contacts decide 

Paul:self assigned responsibility. the original idea of vocabulary was different. Any entity that comes up with an attachment mechanism can point to our RFC

Suresh: using this attachment mechanism in the same way that you need it. 

Paul: I understand the value of this but don't know exactly what it means 

Mark: a registry can be added to either through RFC or other requests. If this is not anywhere a lot of doubt in content creators what will be listened to and what will not be. we establish a registry, then in the guidelines for policy makers you can mention the preferences mentioned in our registry. 

Paul: policymakers prefer to dodge, so this would be useful 

Mark: we can allow various things in the registry but have recommended ones

Glenn: If I don't have a list of registries and mechanisms how do I know where am I supposed to look at. It will create chaos for adoption globally. 

Suresh: I understand the problem, can have IANA list managed by experts. Policy and guidelines can tackle some of the issues Glenn mentioned

Timid Robot: premature (tied to reputation, enforcement, etc.), tremendous amount of information that is adjacent to this, expectation that people use and implement are going to educate themselves. We shouldn't try to handhold.

Alissa: minor issue and can be crossed later. Feels like generic educational task. Something we can talk about later. 

Mark: if you have issues about attachment time to talk now.

Sonia: attachment is an essential part of the standard. Because it brings certainty to implementation of vocabulary. why are we setting it aside?

Mark: we will have an RFC on attachment.

Sonia: you can't agree to a vocabulary without implementation. 

Mark: some of the mechanisms are not iterated by the IETF, some attachment mechanisms are in other orgs.

Paul: concern by rightsholders that you use an attachment mechanism and vocabulary that is not listened to. A web crawler for example should not be obliged to go to an attachment registry but other players might have to. AI companies say robots.txt is good enough but rightsholders say no it has shortcomings and they insist they need other ways to communicate and make sure they are listened to. It can't be voluntary whether you are listened to. Revolves around some concept of widely used. 

Suresh: IETF is not the protocol police .

Martin: Paul's point is a good one on: we can decide on mechanism but not how they are used. we can't advocate for the value of mechanisms that we have as opposed to others. we should talk about robots.txt. 

Timid Robot: push back against idea that we are providing a complete solution ("make right's holders happy"). we only need to provide a good beginning.

Sebastian: authentication and identification?

Mark: out of our charter

Martin: doesn't mean we will not look at it in the future. If I have obtained some content, what expectations do I have with respect to time with that content I have reached. What if robots.txt doesn't say anything about preferences and how do I know if robots.txt has been updated. Most of the crawler operators regard robots.txt valid for 24 hours so they have fresh version of it. If they hold on to content and use it they still check the robots.txt 

Fabrice: fetch something last August, want to do something. The applicable version of robots.txt is the time of access. 

Martin: what would be the expectation around the time of usage and acquisition 

Paul: search engine operators might have a different behavior than others 

Timid Robot: 

Joe: crawling and scraping are different. crawling is good, but people who are about to train they should check preferences. Do we want to have different tools for different purposes. Crawling is for mapping the Internet. scraping is making copies. scraping and crawling is important. 

Leonard: we dont have consistent definitions on these terms and should be careful and discuss further

Suresh: what are the things that we know about and what have been done to document. for example Fabrice said they follow robots.txt at fetch time etc 

Mark: a lot of training was done and scraping was done before anyone knew it was being done. If something was scraped four years ago and I am training model we could say it should be applicable now again.Transitional problems. when you obtain data for a specific purpose you have to limit it to that very specific purpose 

Martin: 

Farz: We usually don't apply rules retroactively because of certainty and fairness issues.  i'm not so sure that whether something is applicable a long time later. Circumstances might have changed.  Crawlers could be liable for that from a legal perspective.

Timid Robot: 

Cullen: when the data is retrieved post AI world, there should be a mechanism to see what the preference was. 

Paul: pay attention to timing relevance but it's not now. 

Gary: RFC that you have to refresh every 24 hours, and it has to say when you are training you have to re-check the preferences. Gary says they do check the RFC. 

Martin: what is the applicable preference if the data has changed? 

Cullen: in an AI context 

Timid Robot: there is a mention of robots.txt and its time requirements, Martin mentioned headers and times associated. Future looking stuff, this could be an attachment problem and it's upto the attachment implementation 

Leonard: 9309 is ambiguous, it's not about HTTP, any protocol that goes over FTP or anything it's not http specific 

Gary: It is not specific to http, applies to any protocol (see [RFC 9309, 2.3](https://datatracker.ietf.org/doc/html/rfc9309#section-2.3)).  We use it for FTP, for example

Fabrice: rules should specify where the default is and mention what you are preferring regarding time. Maybe the publisher can override for this user agent

Farz: Gary mentioned that teams check for updates before using content. Other actors might not have the same means and technical expertise to do similar things.  We need to facilitate it for them so that they can look at the update to make it less complicated for them, if they intend to act in good faith.  If they have to check every time they want to use data, then we have to also help them to be able to know that detail and to technically do that.

Martin: you can't have it applied to your end, the scheme needs to opt in. Establish expectations, define preferences from and relay it

Gary: why can't we rely on 9111. There is a bunch of complexity in the caching tool

Mark: HTTP caching is greedy and HTTP internal semantic applications usually define their own concept as a result

Martin: training an AI model, the content doesn't expire similar to caching content

Gary: technically the content expired 

Joe: Thinking about opt out should be available to big and small actors. 

Sonia: freshness has technical constrains and authorization and should be discussed in the industry. Not just freshness other aspects also do  

Mark: adoption of Paul's ID, we should discuss how do we reconcile multiple preferences 

Jari: laying out the problem: getting multiple preferences in a single file. There are somethings that are not communicated, not informing you about the laws, also there might be some agreements between the parties. Using these preferences that are standardized. Law can say certain things should be allowed and somebody opinion might be different from the law. Set of information that we need to take into account. Recommendation is to recognize its existence but not our problem to solve. But combination of preferences, what is that algorithm: HTTP says something, robots says something else. Martin's draft was saying if anybody says no then it's a no. we as the IETF have no way of knowing, the only safe thing to do is to follow "no"

Mark: imagine if someone says no for something broad but specifics are more nuanced

Jari: One general class and specific class that needs to be combined. If somebody says website says no then it's a no. 

Joe: are you talking about a single file? 

Jari: yes it's about a single file. 

Ted: Agree that the approach is to lean on most restrictive. it is reasonable to think about but we should after August think about how to address these jurisdictional issues. We have to think about this at some point because there are legal consequences we might have to deal with. Between now and August we treat the copies as two different corpuses but after August we can change it and have to make sure the syntax allows us to address the issue.

Timid Robot: asked the question that Ted answers

Ted: the robots.txt might say something different the algorithm can have a syntax to update later  

Mirja: in the end if you want to use the data, you have to decide based on various issues, 

Timid Robot: Require to resolve the hierarchy I might wanna say TDM no, search yes

Sonia: for example no generative AI training and AI training but we are talking about different designation that are conflicting. There could be conflicting preferences intentionally. The rightsholder might have provided the content to two users. 

Mark: this is not about reconciling two different sources 

Sonia: in that case, having two designations still might be intentional 

Mark: constrain ourselves to this: one actor, fetches something from a website that robots.txt allows but the PNG has a not allowed 

Martin: In the absence of external information about what the preference is we should lean on more restrictive signal 

Alissa: I want to make my UGC on this site, and the platform has a disallow in robots.txt. would the platform's preference trump my preference?

Timid robot thinks no 

Glenn thinks yes 

Martin: Jari's draft is sensible. if we dont say something about it it means it's the most sensible. I want to serve people not robots, all the creators involved are happy, if someone gets that content from another channel that says yes then that's ok. we don't have to specify it.

Joe: risk that it would become useless for copyright regimes. For jurisdictions where robots.txt become binding, why should I state my preferences. 

Martin: if you assume  actors are going to ignore that then we can't really start this work 

Timid Robot: advocating least permissive or least permissive 

Martin: most restrictive, least permissive 

Timid Robot: having a resolution past is important and we need to decide on interaction between location based and asset based. We might hit robots.txt and stops and never sees content that's permissive assuming that all the content that is permissive. 

Glenn: what we should do is to consider the signal at the time of transaction. on a per access basis the most restrictive for that transaction. we don't deal with combinations of multiple transactions 

Mark: there are sites with many users. we don't have technical means to address the problem. Policy can tell them how to behave. we need to describe carefully issues that we dont address. 

Paul: asset based preference signal should have preference over location based. The more specific attachment and clearer in hierarchical.

Sonia: censorship: what if a bad actor just say no TDM

Fabrice: some content might not be tagged and default rule has to be clear. 

Mark: happy with the progress, need to follow through proposals. 

## Morning session, 10 April 2025

Note taker: Ted Hardie, Jari Arkko

Chairs begin by reviewing progress to date during the meeting.  Next steps are to make those more concrete, by create a repo and starting an issues list for the draft.  Reminder that the discussions should take place on the list.

To meet the milestones in the charter, the chairs believe that they we will need at least one more interim meeting.  At the beginning, the face to face meetings are particularly important to get folks moving in the same direction.  We can also hold virtual meetings, which have fewer constraints on scheduling.  Chairs are thinking a virtual meeting in the May time frame, after folks have written proposal.  That virtual meeting might be two or three days of shorter sessions, but the shape is TBD.  

Given the compressed timescale, arranging another hybrid in the July may be useful.  London is the current probable target, with the issue being timing. The week of July 14th is convenient for some, but it should be noted that it is the week before the IETF meeting.  This will be discussed with the IESG, since it would contravene an existing scheduling policy.

Glenn notes that the SVTA is meeting in Madrid the week before the IETF, and he's wondering if there is any chance we can meet there instead.  Discussion of the meeting space issue ensued, with Microsoft, Ericsson, and Cloudflare meeting space being discussed (in Madrid and Lisbon).  This is still pending the IESG decision, though, so final dates not yet available. Paul is concerned that going after the IETF will hit the vacation season. Hiro asked about how the draft deadline would impact, and Mark noted that this could be handled. 

The chairs are looking for input on the timing between the two meetings. After receiving an update from the IESG, the chairs will send a poll to the list. Eric (IESG member) notes that as not too many AIpref participants commonly attend the IETF, this should not be an issue for the IESG and Lisbon and Madrid are the same visa, and that London would require a different visa for some people. Mike believes the situation warrants bringing it to the IESG. 

There were additional discussions of conflicts, including IGF, the ITU "AI for good" meeting, WSIS +20. There was also discussion of how many meetings would be required during the IETF meeting, which would be for input from the wider IETF community.  Probably would request a single meeting, on Monday, so that day pass would be possible for those not attending the full IETF meeting. A straw poll showed interest in Thursday/Friday before the IETF. 

Paul notes that the main point for others outside this process is "when does this become a stable reference". Mark explains the IETF last call period and then the subsequent processing.  Mark and Paul talk about what shape "stable reference" exactly means.  So six weeks to two months from the working group shipping to achieve stability in the core concepts, syntax etc.  Final editing can lag a good bit. Pessimistically, from Martin, end of October to stability. There are methods to request expedited review.  Sonia and Deen asked why that charter date was chosen; Mark responds that it was an effort for the work not to be OBE.  Paul notes that the relevant provisions of the EU AI take effect in early August. 

Ted asked if there was any thinking about running a hackathon project; Mark responded that he thought a validator might be a reasonable project.  Farz asked if folks had considered Hiro's comment from yesterday on the creating of an RG as an adjunct.  Suresh responded that the IAB could schedule an IAB open technical session, to test if there is a community interested in that discussion, the IRTF chair would naturally be part of that discussions.  Mirja noted that measurement work related to this is already taking place in MAPRG.  Farz responded that some of the research in the workshop extended beyond that.  Mark, wearing an IAB hat, noted that there are other RGs working on related work, so it might be that this gets dispatched to various RGs.  There would be discussion of how it and the WG interacts.

Gary returns to the previous topic and notes that there are three crawlers using an open source parser, and that working on that could be a demonstration of the concepts in the doc. In the chat, Sebastian notes that Liccium is facilitating declarations for thousands of publishers and other rightsholders with millions of titles. We are implementing the vocabulary and would be happy to verify and test it.

There was a bit of additional discussion on the mechanics of the hackathon, including remote participation. Sebastian notes that there is an engagement hear between the declarant and receiving party, and that verifying that would be important at some stage. So crawlers would be one party, model developers using the preferences by the declarant would also be significant receiving parties. Suresh noted that groups like Timid Robot's might also help test the pass through. 

Chairs are open to discussion on how to make progress in the remaining two hours.  No objection to returning to the issues list for the vocabulary.  Sebastian asks for a clarification of the meaning of opt-in, signalling for training or grant.  He's asking that we touch on how to use this vocabulary in an opt-in fashion.

Mark notes that the intent is to create an abstract vocabulary and serialization that can express either opt-in or opt-out.  Martin notes that this system does not have authorization, so that some of the usual parts of those systems are not presenting (no binding to identity, or to link that identity to the content).  Martin discusses how the one-bit privacy control system works as a generic expression of preference. He thinks that what we get will reflect that sort of an approach.

Glenn Deen notes that he has advocated on the list for an opt-in use case, and that there are some legal frameworks in which a positive signal may be required. Ted pointed to a previous discussion about the difference commercial=no and non-commercial=yes.  Because those are not a perfect inverse, we have to acknowledge that we will have some signals that have some overlap, and that's a natural complexity of supporting both.  Martin then walked through the example he and Alissa discussed in chat yesterday.  Sonia wants to clarify whether we are producing preferences that are useful in specific jurisdictions or a signal that is generally useful independent of the jurisdictions.  She notes that there are no jurisdictions that require opt-in, and she expressed concern that the added complexity that would arise in any system that used both.  

Mark noted that the primitives are meant to be usable in either, since we cannot influence the jurisdiction's legal regime.  He noted that there would be utility in a hackathon project that showed the actual resulting preference taking into account all of the signals, especially if you could then integrate that with a signal of the defaults in a jurisdiction.

Paul disagreed with Sonia that there are no opt-in regimes, as he believes the current UK regime would require opt-in to give a clear signal of preference to allow use in ai training.  There is certainly a lot of resistence to opt-out from the creative community and advocacy for opt-in requirements.  He also reinforced that there are issues in both related to the defaults understood by the system.

Martin notes that even in a strictly legal opt-out regime, that it might be useful in a hierarchical system to have the syntax for opt-in, because the scoping of those statements gives you greater granularity in your statements.  Martin also notes that in an opt-in regime, you might see higher requirements for authorization or evidence for opt-in, because of age verification or similar concerns. 

Timid Robot wondered if a discussion about opt-in or opt-out discussion is a bit irrelevant, because there will never be a world in which there is a single jurisdiction or a guarantee of commonality of policy over time. The hierarchy can set a top-level context for all other declarations; if it is a default "no", then the later opt-in statements are within that context. The Vocabulary should state users SHOULD always set top level context (for example: tdm=yes, tdm=no) for clarity and consistency across jurisdictions.

Paul notes that he is queasy about the vocabulary making recommendations.  Timid Robot notes there are IETF mechanisms for making recommendations--Martin notes that those are for achieving interoperability, not guide other behaviors.

Joe believes that it is more important to note that some of these distinctions are contentious, e.g. commercial vs. non-commercial, because actors disagree about whether or not they fall within the carve-outs.

Piers asks for clarity in how we express opt-in and opt-out, so that we can contextualize those in different jurisdictions.  He wants to know whether that is up to the content providers, sending different representations to different jurisdictions (either of the robots.txt or the content)

Glenn had a question very similar to Piers', and that he could see a rights holder setting different preferences in the EU and US. As an app developer in EU I would follow the EU rules, in the US I would follow the US rules. A lot of websites employ rules like not supporting EU GDPR rules and don't allow users to view the websites from EU. In our case, I might say in EU context that I want to opt out of training whereas allow that in the US.

Paul: The thing we said we'd move forward, was one that isn't specific to a particular legal framework or region. I can say "no" but it needs to be globally applicable statement, whereas of course there can be local interpretation what the "no" means. For August deadline we can't have this complexity.

Glenn: I want to express territorial level differences in the policies I express. And we have this in place in other context today.

Suresh: If you want to make a proposal, please go ahead and make one. But otherwise the WG position isn't that this isn't included.

Sebastian: Just going back to the opt-in. I think there is a case for opt in. I just wanted to warn that it can't be considered as a free-for-all to do anything with the content, as there are still laws that apply. But a strong signal from creators is the ability to say that they are open for negotiation of the terms. Also, there should be some way to revoke or update an opt-out/in.

Sonja: Are we building controls for legal compliance or for preferences? We are making the assumption that preferences are legal requirements, but they are not. Controls should be around preferences, and they should be jurisdiction agnostic. In any case we need to comply by law. E.g., TDM is well defined in EU but operates within a set of exceptions. In short, let's focus on preferences not copyright law.

Mark: Absolutely, we need to keep that in mind. But at least one legal regime has put a hook on the preferences in the legislation.

Mark: We are at the beginning, AI is evolving, let's be careful about the assumptions we are making. For instance, copyright is an opt-out mechanism, and Creative Commons is a way to affect that. We don't control any of those things, we control only the preferences we express.

Suresh reinforced that the best we can do is to ensure that whatever we come up with can support an opt-in regime.  We need to be conscious of it, so we don't kneecap any later effort to do an opt-in regime.

Fabrice notes that there is already an effective default for robots.txt; if you don't have it, the assumption is that it is permitted to crawl a site. There is also ongoing conflict between the use of different tools, e.g. the no-index directive and robots.txt where site maintainers set them in ways that create silly states.

Paul thinks all of the proposals target a vocabulary that allow for preferences in either opt-in or opt-out systems.  It may be that there are attachment mechanisms that only permit one or the other, but on the vocabulary level we are targeting is a use case level, and he thinks that is necessary for allowing different types of use in different legal.  He also notes that our choice of using the term "preference" is appropriately humble about our power in this set of systems.  We can give folks an interoperable way to express their preferences, but any force will come from systems outside our process, like legislative action or legal decisions, which may not be globally consistent.

Mark notes that he expects the WG document will have a section to show how to use the vocabulary to express preferences -- does Paul agree that is the expectation?  He agrees that this expected, but that those are not recommending choices, but showing how things are expressed.

Sarah believes that in our document on guidelines for policymakers, we will require a section that shows how these attachment mechanisms/vocabulary is or is not sufficient for opt-in or opt-out regimes.

Joe, reminds us that this not about enforcement, it is about expressing preference.  At that level we can be more ambitious about encouraging declarants to use these in ways that are common across recipients.  Having a different preference per geofenced area is odd, like having a different favorite milkshake in the US versus the EU would be odd.  

Paul notes that so far what we have produced documents about global artefacts, and that replicating copyright's territorial system may not be appropriate.  Glenn does not agree, but did not debate in the interest of time.  He suggests that it might be as simple as adding a country code to the syntax.  Mark reminds him that we need to get something that can ship; Glenn ripostes that we still want something that can get the different communities around.  Timid Robot noted that it took Creative Commons approximately 15 years to get to declarations that were not jurisdiction specific.

Mark: I have lists of topics, first about things that regulators and the rest of the world know are out of scope for us. But also about things that are conditional on what we actually produce. The whole list is as follows:

- opt-in vs opt-out
- robots time dimension
- disparate assertions from multiple sources
- hosted content
- rightsholder identification
- accessibility, academic / research, impact upon other "good" uses
- data protection / privacy
- enforcement / audit

Martin: We need to have a basic description of the model, would like to do this in the vocabulary document. We may not need to talk about all the implications, e.g., not about rightsholder authentication but our assumption about hearing from those who declare their preferences.

Sarah and Martin: We need to be aware that legal regimes may contribute, e.g., in the areas of non-commercial use. And this may happen in two directions, in saying what can be claimed by rightsholders and what can be done by users or crawlers.

Paul: There's likely rules about accessibility and spam filtering.

Suresh: I'm not keen on adding this to the vocabulary document but rather make an applicability document. Not all material may be done at the same time.

Mark: Maybe we can start a separate document and decide later if they can be published in one go/in one document.

Timid Robot: We need to describe the impact of statements, e.g., tdm=no,search=yes, some of these impacts are not immediately obvious.

Mark: Generally, the IETF shies away from user guides in specifications. Not a hard and fast rule though. 

Joe: I think it is definitely worthwhile to have some kind of notes, but how formal that is and if an RFC is needed is less clear.

Ted: Want to go back to Fabrice's earlier note about people getting to odd states with the statements they make. Thinking of the combinations document. We need to be relatively explicit what combinations mean, both when coming from one or multiple sources. We need to describe this, for the implementation community that really needs to know how the combination stuff works. Maybe that's not by August.

Jari: Fully agree. But need to know the semantics by August.

Ted: Yes, the pretty pictures can come later.

Paul: All this makes sense, but I just want to warn that we are defaulting to a very engineering style view. An example is that a no means "we are open to negotiation", and the associated expectations about potential commercial arrangements. 

Mark: The spirit here is more that we are creating something which has a lot of nuance. We should write it down.

Fabrice: My engineers come up with complex structures, but when I listen to publisher side, the needs are much more simple, want three options, want to get out of the LLM thing entirely.

Sonia: We need to be able to action an opt out.

Paul: My point is that it also needs to work for people who want a very simple yes/no.

Timid Robot: Want to make a point that for Microsoft the three options may be sufficient, but when there's multiple players there may be a need for more complexity.

Fabrice: When we went for a simpler model, and a word of a new standard, a lot of concerns went away.

Paul: I just want to observe that it is probably not an accident that Microsoft comes up with three options. The draft that I put in had three options. It points to a level of complexity that we shouldn't go far beyond. People are forced into a situation where the regulatory environment requires them to pick a choice, so less choices is better.

Mark: Listening to the last couple of days, we expressed interest in search and inference, and already in those cases there is a lot of optionality and variety. I'm thinking we should be pretty coarse grained in defining those.

Mark: Seems like this discussion has concluded, we can use the remaining 25 minutes to bring up any issues people have.

Gary: I put a crawler conduct draft out there, if anyone wants to take it over, it would be good, I can not pursue it. I think though that it would be good to have a document like this.

Farzenah: How can we run with this document?

Mark: Not a WG document, but something that can be published on your own.

Mark: There's also a non-WG mailing list and team to discuss bot authentication in the web.

Joe: Interesting, is there a timeline? 

Mark: No, but there's indeed industry interest.

Joe: Is this an inference bot case?

Martin: No.

Suresh and Mark: This is just a way to authenticate, what you do with that, e.g., authorization or policies on who you accept is another topic.

Fabrice: There is a lot of wasted energy on various bots running. We have a real problem for the industry today.

Mark: There's already IETF programs on addressing sustainability, they might be willing to take this problem on.

The chairs thanked everyone contributing to the meeting.

The group agreed that we made progress.

Thank you for Microsoft for hosting us.

AD thanked everyone for good progress.

