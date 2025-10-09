# AIPREF Working Group Interim Meeting - 30/9 to 2/10 2025


## Day 1 Morning

### Introduction by Mark Nottingham

* Working Group last call has failed
* AI training preference close to consensus
* AI use or inference category has no consensus, needs to be discussed in depth, same as top-level category
* Proposed discussion points: Possible changes to charter, whether to ship a minimum preference early

#### Poll: Is it possible to achieve consensus and meet our chartered goals (in some form)?

Total Participants: 48
* Yes (24)
* No (3)
* No opinion (11)

#### Poll: Our charter has the appropriate scope

Total Participants: 41
* Yes (15)
* No (15)
* No opinion (5)

* Jo Levy: one significant concern is that the charter is too broad, covering how content is collected. Rather than limited to use. Among other concerns
* Warren Kumari: Voting no can either mean that the scope is too narrow or too broad.
* Max Gendler: Intentions behind charter were laudable, but small adjustments could be made informed by the discussion, but this shouldn't derail the work.
* Mark Nottingham: We are trying to find out if the charter is wildly wrong. Small tweaks are not re-opening.
* Suresh Krishnan: Re-chartering takes a lot of time. We can always collect new work items for a potential recharter.
* Farzaneh Badiei: Originally supported charter, but recent discussion that vocabulary should be useful in any scenario online and offline changed that assessment. The vocaulary should not signal preferences for offline uses.
* Pedro Ortiz Suarez: The charter is focused too much on the AI term. The mailing list discussed a definition of AI that didn't reach a consensus. Experts don't want to define AI. The research community does not use the term AI.
* Mark: It may be better to focus at the purpose for which AI is used rather than the use of AI as such.
* Pedro: The term AI is not well defined, it is very difficult from a technical point of view to implement anything with the current scope, it is better to focus on how the technology is used than on how is implemented. "AI training" doesn't really make it anymore, as this is no longer the focus of model developers
* Warren: Narrow the charter now to have an achievable goal, but don't broaden it.
* Mark: We can narrow our deliverables without changing the charter.
* Warren: If we keep the charter as is, we should agree what subset we will focus on.
* Mark: First we want to see whether we can achieve anything during this meeting.
* Paul Keller: It's useful to clarify what the purpose of changing the charter is. We only need to change it if that helps us to move forward. The starting point of this work was to allow content owners to communicate their preferences to AI developers. These preferences may not be state of the art and may not make sense.
* Eric Rescorla: The charter provides boundaries of what the working group can do. Broadening it is only necessary if it precludes things this group wants to do. Removing AI is not helpful. An expression that includes snippets and AI overviews together would be out of scope, because snippets are not AI-specific. There are calls to make the outputs of this working group mandatory. So agreeing on a vocabulary that is ambiguous but mandatory to process would be worse than doing nothing.
* Felix Reda: Narrowing the charter can be useful if we want to preclude starting the same discussion over and over again once we have discussed a proposal thoroughly and decided not to implement it. That should happen at the end of the meeting rather than the beginning, though. Agree with Farzaneh that limiting the charter to online uses, or how AI outputs are displayed online, rather than all AI uses, would be helpful. This would protect users' rights in a lot of scenarios such as accessibility features, or models users run locally.
* Leonhard Rosenthol: Not having any standard and a proliferation of very different preference vocabularies is the worst case.

#### Poll: It is urgent that we deliver something soon (~EOY)

Total Participants: 43
* Yes (13)
* No (19)
* No opinion (5)

* Suresh: We should not delay results indefinitely.
* Mark: Even if we don't set a fixed deadline, we should set expectations, also to avoid too much group turnover.

#### Poll: I (personally) have the interest and availability to participate for the next six months, provided it is productive

Total Participants: 44
* Yes (30)
* No (0)
* No opinion (0)

#### Poll: I (personally) have the interest and availability to participate for the next six months, provided it is productive

Total Participants: 44
* Yes (26)
* No (3)
* No opinion (1)

#### Poll: We should focus on a minimal training preference and ship that, then shift to other preferences

Total Participants: 44
* Yes (26)
* No (12)
* No opinion (1)


#### Discussion of poll on minimal ship

* Mark: Invitation to those who voted no to discuss their concerns.
* Brad Silver: Concern that we will never move beyond minimal training preference. Other aspects may be more complicated, but are no less important. AI training is low-hanging fruit, but also less pressing today than preferences around AI use. Developing preferences around those uses would increase legal certainty for AI developers as well.
* Mark: Would it be preferable to delay all deliverables than to ship a) and delay b)?
* Brad: Not necessarily, but we should try to get consensus on a) and b) first before abandoning a holistic package.
* Max: The categories are interconnected. If you ship one, that limits the design options for the other categories. Another issue relates to defaults. As they are currently set out, anything that is not defined leads to a specific outcome. That makes adding new categories at a later point more difficult.
* Eric: AI training as such is less of an issue to content owners than some economic effects that are connected to AI. Limiting the category to "generative" doesn't solve the problem. There is a lot of concern among news publishers about RAG, which is not covered by the AI training category. Working groups usually try to radically reduce scope when they've been unable to overcome gridlock for a long time. That could happen eventually but we're not there yet.
* Paul: When the disagreement is about the scope, reducing the scope to the preference of one group is not a consensual outcome. The purpose of this working group is to express preferences including training, but is not limited to training.
* Chris Needham: The categories need to be developed together, including a category addressing inference-time uses. We haven't devoted enough energy and effort into trying to find consensus on a holistic set of categories yet, and it's not beyond our collective ability to define those.
* Leonard: If we postpone other preferences, we will lose a lot of participation in the working group. That may actually make it easier to agree on subsequent categories, but not with the same quality.
* Pedro: Inclusion of training is important, but the research community and rights holders are currently moving in another direction. Training remains extremely expensive, so this preference addresses a small group of actors. The vocabulary should not be extremely technical, it should be simple for rights holders to use. Robots.txt is already difficult to understand for many.
* Mark: Suggestion to move to discussing the issues. Paul will present the state of play.

### Presentation of state of play on vocabulary document (Paul Keller)

* Vocabulary is supposed to serve different attachment mechanisms. One of those attachment mechanisms is the one developed by this working gropu. Others include C2PA, TDMReP, IPTC+, TDMAI, RSL etc. All of them should be able to use the same vocabulary.
* While this working group has been deliberating, new vocabularies continue to pop up.
* RSL originally included the vocabulary from an early draft of this working group (RSL). Today it references Cloudflare's content signals.
* If this working group continues not to deliver, private standard-setting efforts may become the de-facto standard, or there will be no interoperability.
* Existing vocabularies are more extensive than just including a training category. If we only ship a training category, our vocabulary will not meet the needs of the sector and is unlikely to catch on.
* Addressing the concern that the EU AI Act GPAI Code of Practice will make the vocabulary de facto mandatory are unfounded. The Code of Practice only references the attachment mechanism (i.e. subsequent versions of the Robots Exclusion Protocol), not the vocabulary. It should be made clear that the vocabulary will not be part of the next iteration of the REP.
* Warren: The de-facto standardization is also a reason for shipping a minimal standard fast, to demonstrate the group can get something done.
* Felix: Is it possible for the REP to not include all of the the vocabulary?
* Paul: We should explore that possibility.
* Mark: So the attachment mechanism could be agnostic to what vocabulary is used?
* Paul: No, the attachment mechanism should use categories included in the vocabulary as they are defined in the vocabulary, but it can limit itself to referencing a subset of those categories, e.g. only the ones that make sense for crawlers.
* Eric: Don't create a false sense of urgency because actors in the industry are creating facts.
* Suresh: While we don't have a vocabulary, other attachment mechanisms that want to reference it can't continue their work.
* Stefano Gentile: From EU Commission copyright unit. The EU Commission wants to achieve an effective preference expression for rights holders. Arriving at a vocabulary is key, irrespective of whether they are enforceable worldwide. Didn't intervene earlier because the debate should aim for a universal approach rather than an EU-specific approach. However, the outcome could support EU regulation and increase legal certainty for rights holders and AI developers. The EU Copyright directive Art. 4 requires that TDM opt-out be expressed in an appropriate manner. That could be done through a vocabulary emerging from this group.

### Discussion of issues

#### issue #159: Overall Approach of the vocabulary
* Eric: Presenting the issue
* Mark: Are you saying there is no useful distinction between training time and use time?
* Eric: Somewhat. The real objections of rights holders boil down to the outputs of models rather than the model weights. If we provide a vocabulary that is so inexpressive that the only way to object to a very specific use is to say "don't train". That will not meet content holders' needs, but preclude a lot of useful uses.
* Mirja: We don't have a great overview of all the preferences that some stakeholders want to express. There are definitely some that want to opt out of every use (by a particular company).
* Eric: That can be addressed by robots "disallow all" (do not crawl).
* Irina Bejan: It's hard to pinpoint content owner expectations because how their content is used constantly changes. A possible alternative approach is live preferences: Whenever a new use case emerges, the AI provider should ask for permission for that new use case. That would allow more flexibility over time.
* Erin Simon: This group is not representative of all needs, so we will be unable to arrive at a complete picture. Instead we could do a study to answer the question empirically.
* Pedro: Search engines already use genAI model. You can use a model trained for one purpose for another purposes. You do not know all uses at the training stage. We can have an AI training category, but we have to educate rights holders that opting out of it can have unintended consequences, e.g. in the context of search.
* Eric: Would welcome a presentation of Krishna's display-based proposal as a next step.
* Martin Thompson: This afternoon, we should discuss what it means to express a preference - who is responsible for the consequences of that? But agree we should discuss Krishna's proposal first.
* Suresh: Finding agreement on questions such as "What is substitutive?" is difficult. We have been unable to agree on that in the past. Even if we agree that we want to avoid substitution, that doesn't allow us to develop a common understanding of what constitutes substitutive use.
* Eric: The vocabulary should allow people to express what they want to say without saying things they don't want to say.
* Erin: This group shouldn't unduly focus on one particular product. Propose to demo Cloudflare's work in the afternoon.
* Mark: It would be useful to accommodate as a side session at the end of the day.
* lunch break


## Day 1 Afternoon

### Doc: [draft-madhavan-aipref-displaybasedpref - "A Vocabulary for Controlling Usage of Content Collected by Search and AI Crawlers"](https://datatracker.ietf.org/doc/draft-madhavan-aipref-displaybasedpref/)

* Summary: Vocabulary draft provide more options to content owners, proposed a set of vocab terms for display preferences, esp. when the content is shown in different AI experiences. The core is display-text (allows/disallows the display of any identified text and associated reasoning with it - if set to no, it won't show the parts of the text and won't use it for reasoning aspects.). Setting display-text to yes, allows the content to be used. display-text-link contains the number of tokens/chars that can be used from the content for AI or generative scenarios. Exact Text Match - reproduce exactly the text (limited by the number of chars specified).
* Overview of the document -- see [draft-madhavan-aipref-displaybasedpref - "A Vocabulary for Controlling Usage of Content Collected by Search and AI Crawlers"](https://datatracker.ietf.org/doc/draft-madhavan-aipref-displaybasedpref/)
* Display Text Length
* Exact Text Match
* Leonard: good proposal if we wanted to limit the scope of the work only to web text-based content, doesn't take into account other media formats within the web. It is an interesting proposal, but small in scope to address the vocabulary requiremeents as we are currently seeing it. 
* Krishna : This is not only for web, we do not propose this as exclusive to web.
* Leonard: If I want to apply this to an image or a text that isn't on the web, I am not sure how it is relevant if the surface is not a web page. 
* Mark: We're taking this into the direction of CC - you can't use this data, but you cannot modify, you can use this data, but need to attribute it (or not use it at all). We dont want to obssess over the fine grained control?
* Bradley: you don't need to use initiated access of content - what is considered user initiated, is a RAG request?
* Krishna Madhavan: if your crawler is tied to a user request (pasting the URL of a page to an assistant), it is initiated by user.
* Bradley: this reflects when you have a choice between opting out by using the "no snippets" statement - can you walk me through how a publisher can do organic search with no summary?
* Krishna: these preferences can be layered - you can use exactly as I provide, or maximum X chars - you can apply different preferences for different parts of the document.
* Warren: worried this could end up with the wrong incentives - i.e. the wrong cookie ads - or the content "I want you to display, even if not high quality" - that could increase web spam
* Krishna: we thought about spam and spam prevention, if you use these preferences you can still block spam without blocking all AI use.
* Warren: not sure if it helps, if the options is nothing or just a specific bit of text - I might choose to show even if it's not optimal
* Alissa: mail list discussion about no-follow or other purposes for indexing the page. Could you describe what no-follow means?
* Krishna: we didn't say anything about no-follow in our document. 
* Alissa: if I am just parsing the file, but not for indexing purposes, can I do that? 
* Krishna: the preferences we have now dictate the preferences for content - the main reason you go for these documents, we are not curtailing any of those usages
* Elaine: proposal on separating indexing and retrieval (acked by Krishna)
* Pedro: question about the specific part of search and the decision between classical search vs AI overviews we see right now. the question is - my understanding of these tchnologies, at least in the backend, are very similar. In this specific framework, would it be ok for a search provider to train a model for actually serving classical search? Most of the information retrieval algorithms work with transformer models, the same underlying model as generative models (GPT, CLaude). The backend technology is exactly the same. Most of th search providers right now, in order to provide classical search with snippets, they stil need to do the same type of training. As long as the end application is search, is it ok?
* Krishna: If gen AI is blocked, you cannot use the content for training gen AI models. If display-text is set to no, it means they don't want to have a snippet generated either. 
* Pedro: by snippet, you mean the little piece of text that appears in classical search below the link?
* Krishna: yes. 
* Eric: It's an interesting integration form. How does it tie to the current vocabulary thing? Shall we make a list of the things we want to say, i.e. "use it for snippets, but not for page overview" - is this desirable property of the system to say? This seems to be a high priority thing "I want you to put something on your page that makes the users come to mine". 
* Mark: Is this specific to AI or just control search engines?
* Eric: there is a lot of overlap between search engines and AI, this intermediating piece existed before AI. Do people think they should be able to say "I want a info box vs an AI overview".
* : looks like we are looking at the attaching mechanisms, not the vocabulary
* Krishna: when we consider HTTP headers, attachements mechanisms - they are all valid approaches.
* : If something is behind a paywall (the way the attachement is implemented), can you still specify it?
* Krishna: We didn't get into attachement mechanisms yet.
* Sebastian: If I read it correctly, this is post-training. I thought it's useful to distinguish - have a structural approach  to distinguish pre-training/post-training and the AI use category which is more or less dealing with inference/RAG/Fine-tuning. These are post-training categories, so I am not sure where we are in the discussion, as AI use was removed from the discussion and now it seems the proposal is only about the post training AI use, so I am missing a more generic definition of where we are int he process and where it can be applied. 
* Krishna: we didn't get whether this is pre/post-training. As an expert, I have an issue distinguishing between the two. I can define them, but it is hard to present to a general audience. We kept it there for continuity, but not labeled if it is purely pre/post training which makes implementation difficult for non-AI experts.
* Martin: There's multiple pieces to this and I can see how they fit together. If a summary is generated by GenAI, I will opt out of the gen AI portion and I will only allow indexing. How does it work if it was produced by a general LLM if the context is feed as part of the generation?
* Krishna: Display-text does that
* Martin: you are making a statement about AI use we were talking about earlier. A question for the room: do you think that for someone who understands this and can apply these policies, it can resist the test of time?
* Krishna: I think it does, as far as I can see for forseeable future - but beyond 5-10 years, I don't know - something for poeple to think about.  
* Paul: I have a hard time fitting it into the context and the charter's scope. Initial conversation around the vocabulary, Leonard made a point that a number of things are not relevant in some other context / attachement mechanisms, so I am wondering how to reconcile that - a number of the categories you mentioned might be useful as additional args together with the search category. The question is where do we define those additional flags, if it good to address them in their own draft instead of the vocabulary discussion. 
* Krishna: I think that might be right and the cause of the heated debate. We didn't make our proposal search specific - it is applicable to other scenarios. If it should be expanded - it is an open question. 
* Pedro: 1. on gen AI - from a technical POV, I support that whatever we come up with, it is better to not differentiate between pretraining/finetuning/posttraining/reinforcement learning, as the capabilities are moving (for example, gen AI models for images can do things in inference --- without training -- that can adapt a certain style). My question is the specifics category in generative AI training, should that be modified a little bit so that it includes cases where the model is not trained? 
* Mirija: You said this genAI training category from a different draft. What is the problem with the previous draft?
* Krishna: genAI category makes sense in some way bc it is about the output we are producing, thus the rationale why we kept them. I have major issues with the prev. draft - there's a draft that articulates it. 
* Mirija: Some cases we discuss how we get smth from the web to the model and sometimes about from taking smth from the model to the web (display). I think putting all into 1 bucket is confusing, because sometimes you can achieve an outcome by restricting what comes in the model and outside - we might have different options for each.
* Felix: Go back to Martin's point about display-text category bc I didn't understand by reading it I didn't realise it was for displaying an AI gen outcome. It might be useful for publishers, I am not sure how it relates to gen AI use that we discarded. Search companies might access something at inference time, whether to show it as a search result or not. Google Search might use AI to decide if it's something or not so we need to access it as inference - but with display-text, you only block what can be done when the content is used for generation. 
* Mark: summarising, removing the top level category, switching to this purpose-based approach. Without detailing further, controlling re-use, controlling modification. Is this of interest for the group? Time for a poll!
* Mirija: Is the main difference that is purpose-based or that it is more fine-grained?
* Mark: This comes with territory, we can have different strategies, but we need to solve how we think about these things. 
* Mark: calling it display-text and not purpose-based might be distracting.
* Paul: need to articulate the key problem, why we need to replace the original approach to do something focusing on display.
* Mark: display makes sense if you are talking about search. 
* Paul: this is not a group chartered with new ways of doing search. display, search is not in there.
* Mark: As we said before, for inference time it is not meaningful to say you cannot use AI with this content, it's just a tool, programming language, etc, it's non sense to say "dont use my content with linked lists". There's a latent argument that this can be up-leveled to everything here except AI training.
* Krishna: AI inference / AI use category is overly broad which block a lot of AI operations - you couldn't run, retrieve something. By taking a more focused approach, you wanna summarise something - you can take these approaches. It does not restrict to search, but applies broadly to AI - search being a main scenario to AI. It is impossible to separate search from AI ad AI from search. 
* Chris: I agree with Paul, we should be aiming to find a vocabulary that publishers can use. It's unclear to me why display-text the description, why it is not a good basis on RAG, grounding, inference - and integrate some of that language in that definition.
..
* Pedro: why the existing vocab does not address the things that can be addressed with display text is that we are struggling with decoupling things, for instance, general purpose AI, generative AI, how search works with these concepts. I think a use-case/display-base would be more reliable on time because it does not rely on the underlying technology. The current vocabulary does not define what AI really is, it is really ubiquitous how it is being used in multiple apps, approaches - it's a very very long list. Saying "opt me out of AI training" is becoming more and more akin to saying to a programmer "opt me out of a for-loop". If you think how you display the data, translation, appropriation of style, that is more understandable. 
* Alissa: responding to what Paul was saying - when we try to standardise thing, you have an exact thing you need and when more people show up, the concerns are quite granular. I am in support of the fine-grained approach, but if we fail to address concerns people are bringing up - we are not doing the job and there will be collateral damages as Krishna as mentioned.
* Eric: The charter does not proclude this work - we shouldn't use the charter in this way, it shouldn't be a problem.
* Mirja: I like it's not AI vs non-AI, everything is AI. It is more fine-grained, but it has generally different approach because the previous attempt was hierarchical. Currently, it doesn't cover the full space - this is better because it leaves us room to say other stuff in the future that currently we cannot.
* Martin: the intent is not to fix search. It might be useful to talk about what we understand reasonably well: co-generation. How it would work for display-text, how do you practice preferences on how your content is used? There is the genAI component that's part of it. If there's a corpus of code that can be indexed and use it to produce code, how does it work?
* Krishna: as an engineer, I would just reuse the code as a library. If a model is trained on code and the code says dont use it for model training, I am not aware of models being able to reproduce code in a generative text. Not in a RAG scenario. The exact match does apply here - if you have it and you use that piece of code for generation, display-text would apply. 
* Martin: there's an implication that there is re-use in that model, but it does not apply well to display-text. If you wanna copy text, there might be more efficient way, so where is the display in that scenario? How does it work for an image application or other use case of this case? I am struggling to define display so that it applies. 
* Krishna: Happy to think through this with you. We are trying to cover ground for most scenarios. Part of what I think works for a proposal is the folks. The code generation is a good example and can take it offline and discuss. 
* Paul: I am wondering if we are having 2 different discussion that are coluding - how we discuss things changed and this is a more grnaular way to expressing our vocabulary compared the two sides with our discussion from the beginning. 90% of time was spent on discussing AI use and search - they were hard to define, one of them has disappeared from the draft, in this proposal - there's a good grasp on the functionality we want to reintegrate in the draft. It might be useful for the folks what we have aggrement on and to me it is he question you raised "Do we still have the rough starting agreement that we have a relatively clear conceptual separation between pre and post training? Do we still have that, what do we do with top-level category" We can have a more productive disucssion if we start there.
* Chris Flammang: the language for display-text "the text that you reuse in a generative AI experience". We need to include other modalities, express preferences for audio, images. Address usecases around impersonation, style transfer. 
* Mark: no training is about giving clarity that it won't turn off search. There is desire to have control over summary, but we want to allow people to use the other mechanisms. 
* Sebastian: I understood the proposal to provide better definition for categories, not replacing hierarchical model. Provide examples for higher level categories, for users to understand what it means "I dont want this, I find it within X, but I don't opt out of search bc it affects the access to my content". With replacing, we do the 2nd step before the 1st. The first response from creators - is there a way to opt out of everything? If you need such granularity, it is a danger. Hierarchy makes sense. 
* Mark: To synthesize the discussion, as a website operator, I don't want them to train on my content. AI however is such a prevalent technology that it's problematic.
* Felix: This is a meta-comment. We're struggling to discuss all of the elements of the proposal at the same time. Is displa category a replacement for AI use, how it would change, shall we bring other modalities? Shall we get rid of top level categories? Do we need distinction between pre/post training. Work on only 1, i.e. display-text category to address the summary issue which is a pressing concern for many people and then revisit the rest. 
* Mark: we're trying to steer the discussion. From my POV, it's about this search stuff. 
* Felix: Is this a replacement for the search category? There are already more fine grained control in use than the one proposed in the draft. We would be doing a diservice to those who are using those controls. More discussion is needed for the AI summary case where the display-text and exact match interesting. Can this be applied to other modalities, images, generic display-output.
* Gary: You said people just want to opt out. My experience with small publishers is that if you small poking them for granular stuff, they have a lot of preferences and some might be technical items that they don't like,i..e gen AI display. Eric's comment is very interesting, can we just run a study and see what people want?
* Mirija: We want something simple, to keep it simple - you just disallow, there's no simple switch.
* Sebastian: reacting to Gary about search categories. The search cat. is meant to be in place to avoid that creators have to choose between preferences on AI like pre/post training and being found on the web. I have not done this study but I assume search category would be swtiched on because the creators and right holders want to be find through any available means, i.e. AI supported search. If you are too granular in that case - can we simply say "we want to be find, but dont want AI to train on our content"?
* Suri: If it's not general use, it is flat and non hierarchical - maybe people know what exactly what to do , but unclear how to generalise it. Make sure that we don't block more than it's needed. 
* Warren: Gary's proposal on a study/survey it is very hard because we can reach some publishers, but you wont reach my auntie or myself. My meta comment we have quite a while, we're low on time and there's no clear consensus - it's going on circles. How do we make progress. 
* Erin: the discussion was about appropriate level of granularity where the attachement mechanism comes into play, because if you can attach the rules to a specific crawler, this drives the discussion wider - so I believe we need to narrow it. 
* Bradley: we don't need a survey, this is an open forum for folks to represent their perspectives, hope they all show up. Proposal as it related to search and AI use is in the right direction. It is a supplement to a doc we were working on, a potential path to start mining for definition and usecase. Worried about surface vs display, a very specific prision of search. I am hearing some folks struggling and I'm struggling too where there is a valuable case. The creation of a RAG index that does not relate to the preferances - is this included? SOmething we did not talk a lot about - the principle of combining preferences and making them dependent on each other to allow the free and effective expression of a preference (i.e no dependancy like can opt into one if you opt into another one).
* Paul: go back to where we got the first discussion about search. Mark you said it was unnecessary carve out of a too broad category. My point is that in some of this discussion which was based on the top level category - text and data mining. If we are moving away from linking a top level category, away from the EU discussion, we can move away search - the carve out is to remove uncertainty around saying no to this, will say no to not appearing in search results. Difference between training uses and search uses - "search engines could only find things they were trained on". The more important, if we have the carve out at the top level category, we address the uncertainty at a lower level. 
* Mark: I hear interest in getting into more fine grained into search control - Poll?
* Felix: check - you have an AI system, it generates an output shown to user - that's display? For the index creation, even if you include it, it would also be display. You can look at a piece of content for analysis (should or not show up in search), but when you want to use it as part of a generative AI pipeline, it requires display.
* Chris: I'm thinking about agentic use-cases. If we rely on display as seen by a human, might be or not a human, we could have a user which is not. 
* ?: Follow up - is there a human at the end of the agentic chain? If the content is passed on?
* Bradley: The RAG index thing - it is on my mind because not all deployers will create their own index, so wholesaling RAG indexes for providing predictions, it means that some could pass forward their RAG but along preferences and allow those to create products.
* Erin: On search category in the chat, having a category like that reduces the burdens to define each crawler (i.e. less known crawlers), but the line drawning is problematic. Search tries to draw a line between traditional search and the more contemporary generative summary, AI inflected search. This distinction draws a line that limits today product design - exact text preference is binary and easy to follow for future flexible developments. 
* Kevin: Why don't we think about the adopted draft, but instead of looking for something else - why not adopt Krishna, text-oriented ones? Training and gen AI training rom the adopted draft and from Krishna not the gen AI, but the aspects about presentation.
* Sonia: So basically the categories from Krishna's draft plus AI training from the adopted draft.
* Paul: So you would drop the top-level category?
* Kevin: Yes
* Eric: I look at both and feel they are not quite adequate. (see chat)
* Alissa: see chat. It's enough to try to address some fraction of the problem and put a band aid there's no collateral damage but we didn't address the core of the problem. This is not appropriate for an IETF working group - stick with the original and make sure we are not giving publishers a fallacy and bargain - I see more sense in trying to address the problem. I would not rush us along to a decision and allow folks to do a deep dive.
* Mark: Krishna, you intended it to be open for changes?
* Krishna: We wrote it as a standalone pressing all the ideas together. There's good discussion around how this could evolve till we get to a draft. As a standalone, it works in my head, but I'm open to discussion.
* Caleb: If you take a look through ekr 's list of what preferences people might want to suggest, there categories need to be independent of each other. They are also product design questions, whilst good to proliferate choices and categories, but if one is inseparable from other, it will result in more opt-out than necessary. Fine grained decision will influence product, and we need to weight how it might affect ability to build products in the future.
* Mark: Poll! We should limit search to being a carve-out to assure that preferences do not affect it(
* total participants: 43 - yes 11 - no 16 - no opinion 8
* We should define more fine-grained search (and other) controls (total participants : 42 - yes 18 - no 5 - no opinion  8
* Krishna: Submission process question: do we want to remove the top level category? TDM makes impossible post processing of the documents. Alternative - change the definition. 
* Martin: This is incredibly broad - there are many problems people identify - nothing is too broad/too narrow - preferences are at some level. "Any use" if a fair preference. Talk about unintended consequences - if you express opinion about X, and that covers some future use / application that someone saw that preference, abid by that preference and the outcome is surprising. THis is the potential outcome of the TDM category. There's some classes of use that might be accessible i.e. research, accessibility, research. A new application we haven't though about and future product managers can make a decision despite the content owners didn't expect something to occur.
* Krishna: This is ur perspective. The bread of the cake opens it to a lot of misinterpretations and harms. There is a lot of ambiguity and to solve it, we need lots of subcategories that we need to address that are ill framed or defined.
* Ekr: People can express very broad preferences. Particularly here, I don't understand how it is different than saying no to bots. 
* Martin: Distinction between acquisition and use "you can't have this content" - this is analogous to not allowing someone to fetch the content. 
* Erk: The diff is scope.
* Mark: Ask a question related to: what is the possibility of people not adopting, can a preference be ignored where a strict adherence to a preference can lead to suboptimal outcomes? Is this a consideration we need to take into account into drafting this. 
* Martin: The whole point is to establish that there are circumstances that the one using the content will have more information than the one expressing the preferences so that it might override the preferences. If it's something connected to the immediate needs of a human - please summarize this content for me - the system will ignore that the interest of the user overrides the preferences of th web service online. 
* Mark: my question is more broadly - as someone who talks to other consumers and not confident about overriding and might not understand when it is permissable to overwrite them - what role does the ability to ignore preference play into the architectural decisions we are making? There are def instances where it happens, but I wonder what effect it has on decisions
* Paul: these are preferences, the usage depends on context - it was initially AI control, it moved to preferences to address these design considerations.
* Mirija: most care that their content isn't used in a specific context than used in a specific way. From the users POV, they don't care so much - but they want a way to say my data is excluded. You can ignore that data - but if too many people ignore the preferences, the preferences are not useful. So if you have too many exceptions, it is not reaching its goal
* Eren: Prefrences aren't totally absolute is useful when there is an use case that was not captured. If there are well understood, it makes no sense that you can ignore them - there will be compliance and involuntary compliance will happen. Most online players voluntary honour no snippet request. Enforcement wont perfectly match, but we need to provide clarity - preference won't work if everyone ignores and if it's not clear what needs to be honoured, it wont be honored. 
* Paul: We cannot capture some things into preferences, because they are fairly limited to a small group of the world. Some are really hard to meaningfully encode in the preferences themselves.
* Eren: I think that's a helpful motivating example, but we shouldn't attempt to match the legal contour or match legal rights, but user requested fetched isn't limited to a particular part of the broad and there is consensus it should be captured. We needto eliminate ambiguity. 
* Paul: In some cases, we might not be able. Even if we edit that into the scope of preferences and not in 3.0 where we have it right now, we cannot do it in all cases.
* Warren: there are just preferences, this isn't a legal thing, but once this is created, it will become a legal requirement likelihood by a lot of actors - 
* Suresh: us not being limited to a specific regime, we can only present them as preferences and others can work to enforce them. there is some stuff missing, mapping it to legal thing is something we are not well equipped to do.
* Warren: but the issue is that we're assuming it won't turn into legal terms
* Mark: it's one thing to make sure the preferences allow people to express themselves accurately and reduce misinpretetations where possible with some margin, but it's smth else to appeal to the effects
* Paul: we don't define anything and we make more stupid rules. The effort of this group - as a group we have a higher chance arriving at a result that minimizes the amount of damage that can occur from legislative intervention.
* Farz: I've been making this point and I like Kirshna's draft because it addresses some of the concerns from the beginning with TDM. However, automated processing is not as well established - put on the record when we are talking what will happen to the users, we should think about non profit, research orgs, archives that will kind of getting these signals that they cannot do the job they were doing. That's why I like Kirshna's solution
* Mark: we heard fromr other folks that these are just preferances and you are saying this is not adequate
* Farz: if there was no incentive to follow standards, we would not come up with them in the first place. there are market incentives out there that makes following the standards better off. This is not just signaling preferences. there is a paragraph into Keller's draft thatmention that ~under what circumstances you dont need to folow the preferances. We should keep that language if we keep TDM with autoamted processing, but that language is -- in how many cases is it ok to not follow these preferances?
* Suresh: Farz, the problem can still exist because it is still a preferances, I wonder why it is related to TDM.
* Farz: TDM is better than automated processing, TDM is broad.
* Suresh: imagine we take away TDM, then there's still a need for someone - i.e Internet Archive has this cultural heritage reason to do it - the preferances can be overriden. Ekr's point is that if you want to express your preferances, you should be able to clearly express it. Whether it can be followed, it's not something we can express.
* ...
* Ekr: Some of these will need to be captured, some won't be optional and people in some cases will decide to override the decision - that's a bug
* Eliot: It occured to me that we're optimistic thinking that people will latch onto what we're publishing. We're worried on regulators jumping on the boat a little too quickly - 1 is coming up with a standard day 1 but considering coming up with experimental RFC and trying to get a bit more running code and understand where things are pitfalls instead of finding all the dark coners. An alternative is put smth out, try something out, revise revise, and then maybe not need the section 3.0. 
* Leonard: From the conversation in the chat is also relevant: one of the things we've done and we are undoing is that in the vocabulary document we have "Things you can state" - 3.2 and related - how do they relate to enforcement, when are they respected? Vocabulary document instead of statement of implementation and move it to the attachement document (robots.txt, C2PA, ). This might give us the vocabulary before we move to others
* Paul: I wanted to come back to the initial question about top-level category - there is a purpose for it, which is we know or that anyone parsing AI instructions will run into machine readable opt outs against TDM from the EU - the good thing is to treat it as an operational signl in the vocabulary. Otherwise, you need each other attachement mechanism will need to have a proprietary specific interface to specify TDM opt-outs. The point of it is that I can interpret that based on the rules in the vocabulary otherwise I need other rules that aren't specified, esp. if someone is going on a text acquisition.
* Paul: vocab doesn't exit
* Mirja: this problem already exists, why do we need to solve it now?
* Paul: we are trying to make a lot of signals legible, esp. in relationship with eachohter. Vocab doesn't allow to rely that isgnal to something we have in the vocab, i.e "not our problem, solve that yourself" - Is it useful, does it make the vocab more useful? We can make it.
* Sonia: Categories need to be clear and actionable. TDM is definitely not that. Usecases that might seem as permisable, people will have various different interpretations of how TDM means. TDM was an exception to state that you can do TDM among other exceptions. There's lack of clarity what that means. It's not specifically to AI, but it includes AI. 
* James: Two viewpoints - these are preferances and they can be ignored. Yet, we need this category because it is in EU law and it needs to be contained. If we are assuming this category exists without explaining what exceptions are - and I'm not as confident this group isn't better placed than regulators to have this conversation. We don't know if someone is ok opting out and being shut down from AI or maybe there are unintended consequences when they opt in into that. Define more closely than a wide broad category
* Mirja: It's not appropriate to pun in a machine readbale document something that only a lawyer can read to know if it's ok to use. 
* Mark: discussion is specifically on TDM
* Kevin: To Mirja point, we are not suggesting these are all part of standards. Where you create those standards is out scope
* Mirja: my assumption is that you express a signal to have an automatic processing of that signal. 
* Paul: machine readable signals provide no value if you need to check it
* Mirja: use cases are around AI and generative AI and not as broad as we are discussing here
* Erk: we're not changing back to TDM - we need to stay consistent with the draft
* Mark: do we need this high level category
* Mirja: I was responding to Paul on do we need this category
* Erk: Chat on implications of 3.0 and Eric made an assesment - on level setting, all IETF standards are followed and if you don't you're a jerk; implication is that no matter what we say in 3.0, if you don't do, you are a jerk - we will see regulatory requirements that will support this 3.0. 
* Suresh: 3.2 was added because without this people will be bamboozeled adding things they don't need. If you wanna take it out, we can have a discussion. We shouldn't loop over it. I agree it doesn't make a diff for me but some, i.e. civil society, were complaining. 
* Erk: I'm not advocating pro/against 3.2, what I hear no disclaimer we put in there will be effective
* Eren: this debate is not about 3.2 - it's useful as far as we go, if someone has an obligation to do, they'll do. This is just level setting. the real debate is the high level top category. The reason some objectify is that 3.2 is the safety mechanism that is too broad. We need to be careful about the mechanisms were we enforce preferences.
* Martin: there is a lot of criticism and not a lot of leaning forward, what we are looking forward to give us some alternative. we tried to do what you describe and the reason why we are doing preferenaces and not control is because we cannot capture those exceptions.
* Mark: fundamental issue is whether we need a top level category - what does it really mean to "not use my content for AI at all". AI is just a technology, not a purpose. 
* Michael: I dont get the point about ultimate system not making a decision, if a piece of content can be used by a model or not. 
* Max: Part of the issue is that it's not solvable in the vocabulary document, but to preview something for later int he week that some can be handled in the attachement document with pointers into other things that cannot be standardizable. Might be hard to shove everything into a vocab document but just point where they exist.
* Mark: if folks are interested in that - let's hear. 
* Suresh: My concern is that we are cycling between two things, which is ok if we make progress. I want to have some things I wanna give permissions for, but I don't want to give for things I don't know. So they would turn of high level categroy and just enable the low level. What happens about what we don't know about? (default allow or default deny)
* Eren: that's begging the question and I dont necessarily agree we need to do that. there's way to block crawlers from doing that. Having a high level automated category is too broad of a category that we are trying to carve out in a useful way.
* Mark: This is not just for the web, but for anyone who would use this vocabulary. 
* Bradley: having that cateogry would be useful, if not, we would end up saying the same somewhere else for a thing that it is important to know about. there is strong convience, efficiency argument, reduce legal risk to have all in 1 place. there is already a legal regime that recognize the ability specific activities. In London I was very verbal - it has to be there because all the other things. It seems to me it would be a mistake not to be there, because we'd put it somewhere else.
* Mirja: the main reason why we have this category is that is some or we need this high level category and the difference between hierarchy / no hierarchy is that you can cover the full space by default. Without, you'd go 1 by 1 through each use case. Given space is changing, I think that's a better approach. 
* Martin: The question for me goes back to question raised by Ekr earlier - as a group shall we allow the group to express this particular preference? I understand how you might adhere by regulation by implementing this. Breaking the space requires knowing what might emerge, thus why we went for hierarchy. 
* Mirja: if automated processing is not a category, what alternatives we have?
* Martin: there are types of AI training that are not generative that people might not want to exclude. There's more that they don't know about and might default to no or yes. T
* Mirja: we would have a set of AI training ?
* Martin: the current draft allows for any category to be a supercategory to others in the future. We can make a deliberate choice to ignore all unknowns.
* Mark: goes back to the previous discussion, if we do something bigger than AI, this changes and we need to define that somehow.
* Martin: the big question to me is if peope want to express this preferance and we are denying that

* Can you live with shipping a vocabulary that includes a top-level preference? total participants : 39 - yes 17 no 8 - no opinion 3
* Can you live with shipping a vocabulary that excludes a top-level preference? total participants : 39 - yes 17 - no 6 - no opinion 6

## Day 2 Morning

Mark kicked things off.
Polls were pretty inconclusive.
Mark summarized on the whiteboard arguments for and against (the scribe was remote)

Main argument for: cover unexpected use cases.
Main argument against: unintended consequences.
Restated a point from preferences should have reasonable fidelity to people's expectations

EKR:
If we allow people to say, nothing allowed, it inhibits innovation.  But my point was
that the language should be sufficientl semantically rich that people aren't put in the
position to simply say no no no.

\[?]:
If it's not in the vocabulary people will have to go elsewhere for a solution.
???

Sebastian: There should be ways to express reservations, as this is supported by regulations.

Paul:
There's a tension between identifying what creators really want and unintended consequences
of using that vocabulary.  Anything they can articulate should be in scope.

Suresh:
For: Having a top level category allows for easier support for both opt-in/opt-out regimes. People can declare their preferences in a simple manner (i.e. allow certain things for opt-in regimes and keep them the same while opting out at the top level for opt-out regimes)

Felix:
One argument against a preference for "I don't want any use" is that it isn't aligned with the regulation, because it excludes all TDM uses, which is different from all acts of reproduction (copying) that are needed for TDM and are stored longer than temporarily, which is what copyright law allows rights holders to opt out of.  We
might be lying to ourselves that we can deliver this based on copyright exceptions et al.

Chris Needham:
For: enables a market place between content creators and AI consumers

Irina:
Focus on technology rather than focus on use case.  It's hard for this group to "draw
lines"... it's against the top level, umbrellas are technology specific.

Paul:
Helpful to keep for and against and not what top level actually means.  Get the structure
first.

Erin: regardless of a scope of an opt out, a market can emerge between rights holders and users.  So that shouldn't be a for/against point.  Article 4 in GSM says that reservations of rights against TDMs have to be honored, but it doesn't say that there has to be one form.

???: what is it that we are trying to define?  is it that top level catch-all?  Is it something that complies with that regulation?

Caleb:
If we would expect all people to take a top-level opt out and then opt in for search, then maybe there's not demand for a top level opt out.  Simply separate the purposes.
(Caleb used the word "problematize" ;-)

Felix:
It depends on what the categories are.  With all the top level we've discussed thus far, it exceeds the charter, because they discuss things that aren't AI-related.

Martin:
Some of these are non-arguments, and we will need to work through them.  I found Erin's argument about the market convincing, no matter what set of categories we come up with, the market will address uses that are considered valuable.  We should examine demand a little more closely.

Kevin:
When would one want to prohibit all uses but wouldn't want to use "traffic control"... ??

Felix:
For example when you want to opt out of everything then selectively opt back into certain uses, such as search. If you say do not crawl, you can't do that.

Sonia:
Against: 
1. Technology feasibility
2. Lack of consistency of application- how would you implement it to the letter?

EKR:
1. This category might be outside of our charter, but may be the right thing to do even so.
2. Are there other mechanisms applying some of the things that could solve the top level use case?
\[hard to understand]

Christopher:
For: ease of implementation is important, e.g., different paths in robots.txt could have different values.  It's easier to just opt out at a high level, and then
relax that restriction later.

Paul:
The fact that we are building a vocabulary that can used more broadly than robots.txt, it needs to include their needs too.
Many other attachment mechanisms don't have an established "Note Well".  By excluding a top-level category, we are standardizing
"you have no business here".  Vocabulary is not only for robots.txt but for a bunch of other
attachment mechanisms.

Sonia:
Inferencing is not included in the EU directive, so perhaps we should question that top level category.  If you had a TDM exception under the directive, it wouldn't necessarily impact inferencing.

Are we trying to say, "against TDM" or "against top-level"?
TDM wasn't intended to scope out what you couldn't do, we would never scope things quite so broadly.  What would that top level category be?

Mark: "Definitional impossibility"

Warren: I'm concerned that we are designing something for people who are competent.  Research
shows that majority people use the default robots.txt.  So defaults matter.  The system needs to be clear enough for people to understand. Mark calls this "Leaving sharp tools lying around".

Sebastian:
There could be different ways to encapsulate different categories- pre-training/post-training, for instance.  Not fully clear what top-level means.

Mark:
Starting position is that it encompasses "everything", but not a human using a web browser.

Tami: encourage good behavior and best practice.  Although a top level might be problematic,
we would love to get to a place with the vocabulary where user agents can
state their purpose more clearly so that users don't have to use that high level block.

Sonia:
It's difficult to understand the intent of the top level category.  Is this just a switch
to say no to all categories?  Does it have to be something that says no to all category but also something else?

Mark: Two arguments made: one is a convenience switch so people can enable/disable then selectively enable more specific categories.  Also, AI came along and surprised people, and they don't want to be surprised again.

Sonia: so "no to anything I don't know about".  Maybe that doesn't have to be "top level".
Against: lack of rationale to include?

Mark: but what about \[this list\]?

Farzaneh: we don't have many small operators.  "I want to appear in search, and I want my stuff to be trained, but just recently I received a notification that robots.txt disallowed searching pages that I didn't know of".  Having a broad category for that small site operator who doesn't know what they're opting into our out of could be problematic.

Mark: this falls under the "Leaving Sharp Tools Lying Around" category

EKR: we've been saying "top level".  Is it the top level of a hierarchy?  Is it exhaustive?
Could it include some new thing that wasn't AI?  Is it the union of known or a catch all?

???: Unless we have a switch to turn something back on, how does someone turn that on?  Otherwise, how to we avoid unintended consequences?  We are assuming use cases that people will be fine without having.

Mirja: be careful about making extensibility harder.  We should be careful about just adding categories because it will impact tooling.

Martin: can we move to the next phase of the discussion as we are now repeating ourselves...
There are things that we know about that we are not labeling.  There are those that we have created labels for that we know about, those uses that we haven't labeled that we know about, and those uses that we haven't labeled that we don't know about.

Mark: we should identify that as a crucial argument we need to figure out to move on.

Martin: we need to trim "fud", and sort through that key point.

Daniel:
We haven't interrogated the expectations misalignment this could cause.  We are assuming a common understanding that may not be there for the average web master.  The more I hear this discussion the more I am convinced that there is \[definitional impossibility].

Suresh: hierarchy v non-hierarchy?  Opting out should not affect unknown future uses (?) \[more]

Paul: \[let's move on.]. If we go back to the first poll of shipping a limited set of categories, having a top level category probably increases our ability to reach consensus.

Kevin: We have not even gotten to the point of agreeing on the language.\[more]

EKR: we already have a way to say "allow everything", and we have a way to say "disallow specific things", and top level category permits us to say "disallow everything that are not specifically allowed".  You have to be able to opt into the things you want to opt into, it undercuts the model if default no does not permit people to allow the things they want to allow.

Mark: if we make progress on the rest of the vocabulary, we might have more comfort to move forward one way or another.

And we broke for 1/2 hour at 10:20

We began to reconvene at 10:50.

Mark: before the break we were talking about top level/default.  We should perhaps defer that discussion until we have a more granular understanding of the vocabulary.

Erin: we were talking about the line drawing difficulties of a substitutive category. Which uses would be more substitutive in practice, and where we thought content providers would be more likely to object or agree.  We haven't arrived at principles but are otpimistic.

EKR: what is substitutive and what is not \[might be a hard question\].  This might be a deep rabbit hole.

Mark: we could create a design team that incorporates multiple view points. Any output doesn't have special standing, but it can be a way to make progress.  Maybe that would be helpful here.

We can return to the proposals from Krishna and Bradley; Erin's proposal isn't ready.  So for now we'll go back to Krishna's proposal...

Michael: we submitted a proposal as well.

Suresh: all of the proposals we have seen are additive to the existing vocabulary draft and cannot be substitutes.  It is not clear how they can be combined in an appropriate manner.  Unless we have a combined proposal on the table, this discussion will be difficult.

Felix:
It would be useful to compare Krishna's, Erin's, and Bradley's categories since they all appear to be trying to solve the same use.  Can we do a comparison and come up with something that satisfies all of them?

Martin: Search is evolving in a direction toward having generative content.  It would be helpful to walk through that use as a test.  But we have to be careful about narrowing to that use case.

Erin:
Presenting an [experimental feature from Google labs](https://blog.google/products/search/web-guide-labs/).  Here we are using AI to organize and provide context to a search results page (SRP).  The query is broken down into multiple subsidiary categories (comprehensive bird watching, getting started, equipment guides, etc).  Then there is a lightly longer generated bit of text that explains why it is relevant.  Should those generated texts be in scope for search?  It is generated text, and it is sentence level, and it is expressing what is in those pages, but it is not a summary of all of those pages.  There is a continuoum from search to long form summary that would be more "substitutional".

Martin: maybe worth talking about the definition of "search" (for instance).  Summaries of content is not covered by that definition.

Paul: You would need to remove both the title and the summary \[to meet the search definition.]

Martin: we would like not to have this stuff resolved in court.

EKR: we talked about this as a spectrum.  What is the intent?  Should we provide a toolkit that sites can opt into and not others?

Leonard: when we talk about search, this also applies to other assets, like images/videos...

Suresh: let's always be specific.  In EKR's camp \[on having a rich vocab]

Felix: Could you run us through this specific use \[with your respective models]?

Warren: I don't understand how we're going to come up with specific things for new stuff.

Felix: let's just use this as a test.

Warren: agree

Irina: dynamic categories would help for cases where the categories would otherwise be too restrictive.  How should my rules and preference change based on those new categories?

Paul: \[this is controversial because of AI]  What matters is the end result: we don't want to direct people to first say no.  In the end this **is** about substitution. Probably should not be called "display-based".  The concern of substitution is that publishers see referral traffic declining.

Michael Jones: Because I read the copilot summary means I didn't hit the link is a view of substitution.

Martin: I don't know that we can use any of the proxies we have to get "there".  Can we get one step closer? \[Is length a proxy?]

Krishna: it does address this particular scenario without being overly generic.

Caleb: in the world of a top level catch-all category, this example would not have come about.

Mirja: substitution may be a bad term.  If the user avoids clicking on things they don't actually want, in the end we are reducing clicks but it improves usability...  If I only want to get the temperature, I don't **want** to click.  Maybe that reduces income, while increasing usable.

EKR: Users want answers.  They want to find specific things (the pages).  Now you can get one without getting the other.  Or "Make me a summary of a WG in the form of a Metallica song" is a completely different category.

Max Gendler: pushing back on opt out styming innovation.  I don't think it holds water.  Putting a preference out there doesn't remove the possibility from the world.  \[You can always pay for the content for those new uses.]

Leonard: one of the reasons Bradley discusses "substitutive" is that it's not just about reducing clicks, but the scenario where the user is performing local search.  So now they've lawfully acquired the asset- you don't need links.  But you want to perform a search or get a summary, etc.

Paul:

It would be benefit us if we looked more closely at the actual proposals.  People are more likely to allow searches, while inference / substitution are more likely to be disallowed.  Both are applications of the same technology in different ways.

Warren: \[???]

What is best for the people actually consuming information?

Felix: the text does not support Erin's use.  If we go back to Krishna's text, then if you say display text no, you would not be allowed to use it, but length might facilitate a use case, but the publisher would have to be aware of the impact.  Text displayed (Section 4) is a better starting point.

Christopher: push back on reducing clicks.  There is a difference as to what is best for the user and what the user wants.  I worry about the integrity of the response.  Also maybe it teaches people to accepting answers without critically thinking.

\[Daniel]: is analyzing, but choosing to not display less relevant results or information covered by substitutive use case?

Krishna: display text length is limited to a number of characters, and we need more clarity around the language.  Does ai substitutive use preclude using an input document for relevance and ranking?

Leonard: ranking is not substitution.

EKR: definitions are anchored against a very specific pre-trained model.  This may not be how things work in the future.  The principle seems to be that you would have previously downloaded the thing, but I am handing it to you directly.

Felix: I don't think this is such a huge problem. From the perspective of the publisher, there is the no training category that most of us have agreed upon, but with RAG-style scenarios, even if I said no, RAG might still bring stuff back in.  That would require a separate way to say no.

## Day 2 Afternoon

A few people got together over lunch to combine the display based preferences along with the current vocabulary. Erin and Felix presented a quick overview of a potential AI Output based classification.

Erin: we will address the common desires among content creators that require direct quotation and disallow summarization and the combination of the two. We also talked about maxed links Erin will write them down to focus on them. 
Do we want a list of links with titles and snippet as simple search. Do people want to be able to object to the entirety of the AI (blue link result should be included or not?)because most people would not want to control that or not. If we are going to create these categories poeople might want to disallow everything including traditional search

Ekr: if i do link+quote that is primarily ...?

Mike (Cloudflare): Input is interesting. As a content creator it is difficult to trace how the content has been transformed. This is concerning. Focusing on AI input is more approrpriate

Paul: It is about using as input. Deployed model: if you are concerned about something you expressed for input to have an effect on the output, this text is not for that. This is not a replacement for training or generative AI category. This is when assets are provided as input to train AI models

Mike: if I dont want my content be used in RAG, the AI model will never fetch my content. As input to any process that the model is going to do. 

Martin: the work in this group does not govern whether content can be obtained. It's about preferences after. 
It's not a governing control. It's about understanding of preferences. 
Leonard thinks this as an addition is good

Ekr: if you remove everything after certain queries will it have an impact? In the yes state it's ok but in the no state, it gets tricky. we want to focus on whether this is the right direction. Second, one thing that happens models are set up to design is not being raged but it's search engine. If instead of RAGing the search might direct to text and link. Do we need the text as "input for training model".

Erin: the reason it's there is to distinguish from the model being trained. 

Ekr: Is it ok to say it is fine to train to provide snippets or is it just train or no train

Erin: training is too upstream in the foundation and should be adapted to time etc we don't want to stop training upstream 

Ekr: worried about adaptation 

Felix: output v. the ingestion: if you don't want your content be analyzed at all it won't end up in search anyway. There is a lot of demand for content not to be summarized but appear in search result. Thats why AI has to ingest it (to appear in the search result,)

Eliot: Link is a form of attribution but there are other forms of attribution: let me add a snippet to refer to the website. This is more policy condition than action 

Suresh: Mike can you walk us through the ID you just submitted? if there is some purpose you want not met by this let us know 

Krishna: one of the strenghts of display based: the text here address most concerns with the display based. Spam marking or safety marking is a different output than what we are talking about. There are limitations to think about it in terms of output. 

Elaine: was it the intention to cover grounding? 

Erin: yes

Elaine: Ekr mentioned "user query" is not clear. but what does user query mean?

Erin: there is a definition of user query, it means it's an input by a human, it's content type neutral (not typed out) can include assets 

Elaine: are we including agentic AI applications?

Erin: Agentic applications are in scope in terms of what they use to go out and fetch and return but whatever the end user is supplying is not in scope, we want to carve out agentic AI so please give us suggestion

Sonia: I think what we are intending to cover here might be broad. All AI models generate outputs. Doesn't matter if displayed to users. WEb crawled assets not mentioned either. 

Erin: we can ask should this be limited to web crawl but don't understand the cotent be used but not in the output. You can limit it to the cases that use of asset is limited to responding from the asset. 

Sonia: the AI processes various images understands something is harmful. It falls under broad category of Inference

Erin: content type was set aside on purpose. If the image used in your example should not be displayed, then it will be prohibited by the ..parameter 

Sonia: first section is top level control and then the follow up is what the publisher can additionally comply 

Erin: you can condition your preference on some requirements: AI output (ye) condition= quotes means only use asset as a verbatim quote 

Sonia: publishes harmful images

Erin: by focusing on what is displayed to end user we have eliminated the cases that internally needed for safty. output is not AI process returns result, it's more about providing something. It's difficult to expresss. 

Mike: AI output lives in broader context. Robots.txt doesn't solve the issue. You can carve out search. 

Alissa: same question as sonia 

Felix: agent question: we discussed definition of outputs could be specified. Just because you are handing off input to an agent, doesnt' mean this doesn't apply. If end result is not outcome delivered to the user then this category will not be affected

Ekr: I hit some API. how do you know what the end point is. It should be very clear which one it is. 

Martin: the original intent was what was being presented. your point about API: the definitional part gets interesting---the text is trying to establish the susbtitutive aspect and only try to talk about that. When systems inteconnect the boundary between user and systems is unknown.The agentic question interesting. Agent producing multiple types of output, put it on a screen etc but if agent says please navigate to a web page, that would not be the intended use. 
The question we need to ask is is it useful for some to ask for thsi and can it be professionaized 

Leonard: introducting the agentic problem is complex: there is the output and input both. queries can be created by agents. It can be multi-agents. we should look at end user input and output. 

Ekr: what you want is that this is how you present system boundary. At the end of the day what is being spiited out follow ths signal. Maybe we can remove query. System boundary input and output. 

Daniel: I don't understand if we have AI output no then it won't appear in search? 

Felix: No

Daniel: deferential implementation by crawler. 
Martin: we are still questioning what would happen if someone says no to AI Output. At the moment you cannot have anything on search if the answer is no. 

Leah: I wrote out categories and subs: in London we discussed sub categories tell me about them. 
when we are talking about search, indexing etc. Search categories might benefit from sub categories overview, indexing, snippet. And then we can have AI training with its own definition etc

Ekr: I read that even if you say no to AI output here is the link. I don't care about a precise product but we need to be clear to do AI processing. If that is the intent then it should be sharpet. 

Alissa: what do people view as the benefit of this approach to that of Krishna

Paul: We see it as a merging of different approaches. Descirption of calling it output is better than display. Krishna's draft is a bit complicated we dont want to stress on different modalities and want to condense Krishna's draft. 

Krishna: there is a lot of discussion on output part being exponed to the users. The question is code generation aspect we didnt address as a part of display. I think the feedback is whether this is search centric or not. It is not. There still much work to be done to say what exactly an output is but it's a good start to bring all the drafts together. 
we have to consider that AI crawlers are collection mechanisms which we need to discuss. There needs to be reconciliation of proposals. 

Mark: can we take a couple of polls? In the form of one asking: if you think Krishna's (display preference) or Erin's (AI output) proposal is the way foward? 

Mark: they are not altearnatives you can go for bothy 

Paul: we started with Erin's draft both are there 

Felix: maybe we should say is this viable?

Paul: maybe this would address the need for having an explicit search preference 

Suresh: what are Mike and Leah (Cloudflare)thoughts?

Ekr: Concerned about how far humming is getting us. So we are trying to harmonize the drafts and it's great. But does this supersede Krishna's or are there cherry picked stuff? if the latter then it's concerning. 

Krishna: not sure it supersedes it at some point we have to talk reconciliation 

Ekr: give people a little more time to work on this to reconcile everything and look at it holistically

Erin: Krishna's control for indexing and retrieval is not in this new one

Ekr: these things work together. combination of directives allow this system to work so we can't cherry pick around.

Martin: top level remains an important issue. we can somehow keep it separate. The other component was indexing and retrieval, talked about it concluded want to rely on exisiting control and not to rely on a future mechanism. once thats done the other pieces in Krishna's is about finer control, how much video, how high resolution etc. The conclusion there was to defer to some future date. Look at it and see if this is a good replacement for search category, as a replacement for Bradley's proposal and Erin's proposal. If people are happy with the direction this is going then that's good.

Mark: extended break helps? 

Martin: no homework exercise, and people need to go and think if this works for them. We don't have much to refine it. we can try. 

Paul: to get some clarity on the environment might help and get the concerns that are not covered and how we can cover it

Mark: lets see if this can be an laternative to search 

Suresh: Max has something too, we have a draft from Mike and Leah, see what is missing from this proposal 

contentious. Other principle is simplicity so the audience at large understands it. Search, AI input, AI training. search is worth calling out. People understand traditional search better so they can easily allow it. AI input: might be slightly out of the charter, it's a good definition because we don't want the creator content be used for training down the line. AI trainig: content not to be ingested for training. 

Paul: last sentence of each category refers to a top level category but this supposed to be a mistake and can be removed (cloudflare doesnt have a top level category)

Leonard: biggest concern is that definition of AI input locks it into search answers. AI input is better cause not limited to search. Everything is on the Internet from CF's perspective we need a set of vocabulary that work off the Internet and off the web. 

Ekr: point of terminoglogy: this was not a design team that came up with a new proposal. there are 8 values here: search no input yes training yes so this means you can use this for anything but search? 

Mike: yes

Martin: preferences might be illogical thats not a problem. The problem is why do we have different words in the CF draft and having rational for these things more useful than definitions 

Leah: on search we have an addendum (Martin has seen it)

Felix: it doesnt achieve what it purports to do. if it's clear what a search result is it can work but then we don't know what that is. Same goes with AI generated search summary. So if you take things as defined here you will be excluded from search because traditional search includes summaries 

Chris: don't understand the various implications. need to think through and understand combinations and option. but CF's proposal is good and understandable. Also it has the advantage of having "input stage ". Chris thinks the Erin et al proposal is not as direct as what CF has

Caleb: active consulting of a web index to create search results falls in 3.2. which is AI input and 3.1. (search) is the sub category 

Elaine: In defense of including the phrase "search results,"" because in each of these proposals, there us an issue of overloading terms. Unclear to stakeholders whats meant and implicated and unintended consequences so lumping them in has implications. 

Paul: CF is simple but doesnt represent reality. Doesn't go into enough nuance. essentially reintroducing all the issues we have been trying to resolve. We cannot wish a reality where AI is not involved with the search result and CF's proposal seem to think we can. we need to create more understanding of creating more complexity. This looks much better than what we are producing but it won't work. 

Krishna: I believe in simplicity and thats why I did an ID but this proposal has oversimplified things. if you pick AI category: by saying AI input is no or disallowed all of the safety protocol on the web will go away. this proposal is oversimplified. It's completely not viable. 

Ekr: understand what AI input is doing. but curious why you removed generative AI training. 

Mike: Content creators like our simple approach. Agreed Krishna you can avoid the preference for security reasons. to Eric's point I wanted to go broader. We are covering both.

Suresh: want the WG to look at granular preferences even if complex. 

Mike Gray: submission as a proposal was done last minute but the proposal was well thought out 

Erina: To have distinction between genAI and AI, then we should do that. It might be good to look into an exception. 

Krishna: no exceptions can be ignored 

Mark Gray: preference setting side, the more ambiguity have it's hard to advise clients. Is this AI or is it GenAI especially where we dont have firm definition. If there is too much ambiguity then clients will not be certain what is what

Paul: traditional search" is like Oktoberfest, for a week people run around in lederhosen but it doesn't exist in real life anymore. I wonder saying something about "search" is senstive on both rightsholders and search operators. We need to make it easier and more addressable. maybe we can find common ground if we discuss. 

Christopher Flammang: This recent discussion has been productive and I feel like we are on the right track

Caleb: (lighthearted closing remarks involving Arnold Schwarzenegger)

Gary: Have we ever considered using AI to take notes?

mnot: before the break we had a promising discussion

ekr: fig.1 of current draft: what is the proper relationship between the new preference and the diagram? instead of search, we have AI Output? but then if you want to be included in search, what? 

martin: the new category doesn't say anything about model training. so is model training an essential step of building a search engine? 

erin: not confident we can understand and rank material if we can't train on it. 
the thing a lot of people want to say is "i want the status quo ante with respect to search engines, but not new things"

martin: because the new category doesn't say anything about training, it's irrelevant to this question. when we say yes to this ai output thing we're essnetially not saying anything about the training of the model. if we say there's a big black box and all we care about is what comes out of the box... 

erin: with the hybrid proposal we put together, there's a category of use that is constrained. we need to think more about how training and search interact. 

paul: are you really saying it is impossible to find and rank a piece of content that's opted out. 

erin: maybe one piece of content, sure. if lots of content opts out of training, maybe that's harder.

ekr: if we integrate the ai output options from the hybrid proposal, would we strike out the search box in fig.1? 

all: yes. 

Leah: the charter states we are supposed to be standardizing building blocks that allow for the expression of preferences. Teo kinds of actors here. Web publishers, who want to express preferences -- simplicity helps them do that. On the other side are bot operators, people who want to train models. Simplicity might make it harder for them to know what to do. So to come back to an earlier point, clear definitions benefit both. More accurate to what you want to do as a website operator, and clearer for an ai operator what they can use content for. New proposal lacks a certain amount of clarity. If you just want to be in blue links, you have to combine multiple categories. 

Suresh: Assuming that once this document is produced, some companion documentation will come from Google, Microsoft, that say "hey if you turn this on you'll be excluded from Search results." Maybe Bing will say if you turn this on, we won't be able to do ranking, or something. 

erin: yes we probably would. but the categories still need to be clear. 

Suresh: the vocabulary document will not explain that. 

Gary: managed robots.txt for ten year. Kind of intuitive in its simplest form. When it gets to corner cases, then people go to the documentation. But in its simplest form, it's straightforward. 

Suresh: yes, but AI training = yes is not straightforward to people what that means for Search. 

Martin: possible solution: core insight that we have with Krishna and the hybrid design is to focus on the outputs. saying somethign about what the system can output relative to a given piece of content. The question around AI training can be answered the same way. If we change this from a process that happens in a server to a process focused onthe output, that's better. If we say you cannot use this content to produce a trained AI model, at its application boundary, then we can say something about trainign in the same way we are talking about outputs. We only talk about what's shown to the outside of a system. What artifact does the systme produce? if you think abotu the way in which meta has produced Llama, that process is a box that ultimate has inputs, which are a bunch of assets, and an output, which is a model with a set of particular weights. Might still be questions about substitution and other categories.  A model that is capable of producing somehthing that replaces some input. 

ekr: would OAI need to respect training preferences? 

martin: maybe. they sell access to the model. 

felix: very different from the conception of training in the EUAIAct.

felix: erin you say that if you can't train on some content in the index, then maybe youcan't find it in search. is it possible that the model doing that is not a generative model, and wouldn't be covered by the generative opt out. 
erin: probably fgenerative -- it makes the labels and summaries in the Webguide example, for example. 

ekr: can we go back to the use cases document? see how these structures suit those use cases? 

ekr: seems to me like the nature of the .... new proposal is very output oriented. but the left hand of the diagram is very input oriented. can we reorient that to be more output-oriented as well? instead of google having to say "if you want to appear in our search index you should have these settings" it shoudl be obvious from the document what you have to say. 

chris: if the result of this is that creators or publishers have to say generative ai training yes in order to appear in search, then that will not suit them. not an acceptable outcome for content creators to not have the ability to express the preference for different applications for their data, or using appearance in search as a lever. 

paul: i understand th explanation you've given, erin. but i don't know if it doesn't undermine some of the essential understandings we have had so far. can you separate the use of assets to train models and the use of assets in the output of models? doesn't that violate the code of practice. lots of people had that expectation that these could be separated. if not, our work is much more complicated. 

erin: a statement about a GPAI is not necessarily a statement about a ranking system, but also there are words of limitation for a reason. 

ekr: let's not use this forum to discuss whether companies are complying with commitments. 

pedro: regarding martin's remark -- probably a better approach. but one quesiton is existence of open source models. some of these technologies, the problem is they have multiple applications. technology behind a search engine is very similar to technology behind a generative model. given the state of searhc today, you could probably take a model trained for search and use it to generate content. so then we focus on purpose and output. but then there are some actors training open source models, even funded by the EU to have generative models in their local languages. so these things that are open source get extremely restrained in this scenario, because an end use can use the model in whatever way they want. so what's the solution? 

martin: to the extent you're publishing a model with open weights, those would be governed by the preferences. it gets interesting that in the course of developing a search engine you might also develop a model capable of other things, and then you might not be able to use the model for those other things, due to the preferences. if you release amodel with open weights, and then someone uses that to operate a search engine, that would not be acceptable because they would have had to abide by those restrictions. 

pedro: the scenario that gets a little bit complicated is that if you are a private company that is not releasing the weights, that's ok. but if you want to release your model open source that could be used for more than one thing, they'd be governed by stricter standards. disadvantaging smaller players. 

martin: no. but it does change the dynamics of the situation in ways best discussed in text and with pictures. 

ekr: say i am common crawl. the assumption is i propagate the labels, but don't enforce them. the presumption is that anyone who takes the data and trains a model on it is bound by the various restrictions, and so would people who were downstream users of open-weight models. 

erin: focus on the application of the model, not the capabilities of the model. So not "being capable of generating outputs" but "actually being used for generating outputs"

martin: unless we're more precise, a model trained for public release needs to be trained on the most restrictive subset of material since the downstream uses aren't known. 

pedro: say someone uses common crawl to train a model they release open source. and they say what they trained on, and that's great because common crawl preserves the preferences. but the model will have all the restrictions of all the data on which they were trained. 

paul: we have had this discussion before. the point is if you train a model and there are open weight releases then we have to define ai training and gai training the way they are. gai definition is largely capacity based. therefore you need to make the decision at training time, and you need to filter the stuff out if your model is going to have generative capacity. the entire point of this is to allow people to express these preferences. maybe we need more categories in this space? sometimes there's a rightsholder that says i don't want this to happen and depending on the legal context you're in you have to respect that. 

suresh: following up on pedro. common crawl crawls a lot of things. what stops someone making a smaller dataset that has more restrictive permissions, like gai ok?

erin: maybe we are just at the end of a long day. but why is the open model case different from any otehr case. when you train a model you select the set of content and that conditions what you can use the model for. if you've included content that is not allowed for training a generative model, then you can't use that model for generative ai. 

paul: at which point it is not an open source model anyore because downstream restrictions. 

erin: do people who want to release open source models, do we train on the more restrictive set, or do we allow the models' restrictions to be passed through. 

ekr: this is not the right level of analysis -- the legal issues vary by jurisdiction and are not for us. 

ekr: as a practical matter, all these models are generative. and you either use them generatively or you don't use them generatively. yes? is it even a meaningful distinction. 

pedro: it's difficult, but yes, it's almost always generative. the distinction between ai training and gai training is exptremely complicated from a technical pov. whatever actor takes a general purpose ai they can potentially use it for generative. 

pedro: yes, you can take a subset of common crawl data and take only a part with approriate permissions. but it creates an imbalance. why? because private companies get to train on more things than those training identical models with the intention to release them open source. 

mnot: if we can to make some concrete progress that would be great. some people are going to meet between now and tomorrow's meeting and can bring back more proposed text. 

max: proposes we add an optional pointer to the terms of service. meant to be additive to the attachments draft. modeled on how robots.txt has sitemaps, although that's not part of 9309. hopefully will put i-d around this. comments?

thom: TOS texts are not machine readable. this would just not work at scale. impractical. you can put a pointer if you like, but it would not be useful. 

martin: we have link relations and there's a link relation called terms of service. but others might also be useful. tha'ts already present in http, but if you care about this, adding some generic linking capability in robtos.txt that might be interesting. but also since you're getting robots over http, you could put in a link that way. the qquestion is to what extent is it bound to the resources in robots.txt. 

mnot: web linking rfc also has the concept of an application, such as what are the link relations that are meaningful in that contenxt. perhaps beyond the scope. 

mark gray: is this going to take a single value, or multiple values? many sites have more than one source of terms. 

max: yes, should have multiple inputs. probably place terms of use that is applicable to crawlers here. maye they would consolidate on this is the terms relevant to this use case. 

irina: current problem is that robots.txt sometimes mismatches terms of service. which controls? 

max: we could hammer that out. will probably be a conversation around which parts of this are standardizable, and perhaps TOS is not one of those places. having the pointer is just a starting place for the conversation. 

James: goes to machine readability. if TOS aren't machine readibility, what's the purpose of the pointer? what are people to do with this? does it turn TOS into something machine readable? 

max: briefly a number of fine folks in this room have built some machines that can do some very good reading. generally it is a useful qualifier for publishers to say hey not everything here is covered in robots.txt or by this vocabulary, so hey here's a link to our TOS. at the least it's a useful signal for the ecosystem

james: TOS are a legal mechanism designed for people. and robots.txt is a technical mechamism designed for bots. 

max: yeah, look, i mean the natural language component of terms of service are deisgned for people, but it migth be helpful also for the bots to look at it. 

gary: this was raised and rejected earlier -- the models will continue to hallucinate, different models think about differnt things. if tos is a legal document, how do we deal with the legal ramifications? 

max: it was more like a lukewarm no last year, which i was part of. and now the development of this discussion have convinced me this might be useful. 

rony: just echoing sentiments here. even though it might be useful, how does it help the work we've been doing here, and will it be likely to make things more confusing. 

paul: useful because it makes us face what the alternative is if we don't get our act together here. if we don't let people express preferences they will express them in other ways like TOS. 

mnot: you're of course welcome to work on a draft. questions about how this fits into our charter. kind of short-circuits the effort to fit preferences into a vocabulary. from this initial discussion doesn't look like an easy road.

suresh:doesn't see hw it fits in the charter without knowing what's its purpose and how does it combine with the other preferences. 

max: just wanted to get the brief out there. 

mnot: done for today. best of luck to those who want to work more on the proposal. 9:15 tomorrow. we will eagerly look for any progress made in the intervening time. 

- [Thursday session (13)](https://notes.ietf.org/notes-ietf-interim-2025-aipref-13-aipref) (02 Oct 2025)

## Day 3 Morning

- Chair: Assume good faith in others.

- Chair: Group is not a typical IETF group in that the issues we're dealing with are not purely technical; they're societal.

- Chair: Intend to spend today's time continuing yesterday afternoon's conversation.  Break ~10:15-10:30.

- Chair: Subset group met earlier this morning.  Is there progress to report back to the group?

- Paul Keller: No, and no better understanding of differences.

- Felix: Tension between definitions that are easy to understand and definitions that are technically precise.
    - example of former: "i want to show up in google search, but not in chatgpt"

- Mark Nottingham: One approach would be to make approaches crisp in different drafts.

- Erin Simon: Distinguishing between product types is brittle because those evolve over time. Better to define around behavior.

- Chris Needham: concerns fromt he publishing industry regarding the definition of where content can be used, "all of these things are intermixed aninseperable" is not adequate

- Krishna Madhavan: No easy way to have these conversations, we're all tired, it was nice to have something to ground our conversations on, I am optimistic, nice to see trust.  Questions that still exist: "Do we specify product categories? or do we focus on the kinds of outcomes that come from the technology?"  The focus on AI outputs is a good thing. How do we articulate better in the drafts, **should search be a category? I believe it should not.**  There are still fundamental questions that need answering.  There is a lot more space to have these trusted conversations

- Martin Thomson: If we start to focus on AI output, and not focus on search specifically (we are slowly concluding that looking at the properties of things rather than label app type is the sensible way to do things), so recognising that there is interaction between that concept and model training - we can acknowledge the connection but continue to make progress without getting bogged down with the fact that there are lots of other things connected to it. People keep bumping into interconnected problems.I would ask people to set interconnected things aside and let's try to make progress where we can. It's ok for some things to not be done all at the same time. Focus in discussion.

- Mark N: is it useful for us to spend more time like this (in meeting format) or do we take some time out to have side conversations?

- Ekr: Echoing what Martin said. We shouldn't have to solve everything all at the same time. It's hard to make progress in a room this big.We need to break down the system to understand how the difference between transformer models that enable a search product and using to synthesize and present to users.

- Suresh: How did the difference emerge between groups?

- Paul Keller: Labels are a bit of a red herring. Part of why I am pessimistic after this morning is that we have found no agreement in the training side of the discussions, there's not a single piece that isn't questioned right now. We seem to be disagreeing more and more.  The goal of this group was not to make Google search (as it is now) possible. The goal was to give people the ability to express preferences; we're trying to build a vocab; it is hard to have equal conversation. There is trust and respect at an interpersonal level but at a "bird's eye view" people seem to have lost trust in the process

- Ekr: I would like search to continue to work

[...]

- Thom: People should be informed about the consequences of the controls they are offered.  Analogy to Brexit: country was asked a binary question and not informed about the consequences.

- Mark Nottingham: Systems design principles: make things as complex as they need to be, but no more complex.  Important to prevent ossification.  Maybe we have the conversation in terms of the underlying design principles?

- Suresh: People should be able to express any preference they desire, so long as they understand what the consequences of that preference will be.

- Thom: We in this room need to have a very clear understanding if we want other people outside of this room to understand.

- Daniel: Not all AI providers also operate search businesses.  Unclear if the two are really inseparable.

[...]

Gary: Coffee situation resolved! (Applause.)  Would this change if we had a mechanism for opting out of AI Overviews and AI Mode?

[...]

[1 hour break]

Subgroup report:
- Foundational model training
    - AI Output + associated training
        - "Lederhosen" + associated training

"Lederhosen" is: If Lederhosen is set to yes, it means that using that asset in AI Outputs is allowed, subject to the additional conditions that the AI Output must only consist of an exact quote/snippet/partial representation of that content and that the AI Output must link back to the source.

In summary:
1. AI output is more narrowly defined AI inference/use focussing on output/use
2. Contention on nesting/hiearachy ("Lederhosen" as a subcategory)
3. Shift in training side of things
    - "Foundational model" better matches expectations than "general purpose" or "generative model"

Existing PR has naming issues and is incomplete compared to above: [AI Output and Search categories by martinthomson · Pull Request #176 · ietf-wg-aipref/drafts](https://github.com/ietf-wg-aipref/drafts/pull/176)

Complexity vs nuance: combined exact quote + link back could be separate

