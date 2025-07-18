AIPref Design Team meeting London 2025/07/17



Agenda overview from Martin going over issue list:

Main topic today is confirming the definition of terms within the vocabulary. To be used to define preferences from the content owner. Specifically:
- Overarching TDM term, and potentially renaming
- AI / Gen AI terms
- Search and inference categories
- How to combine the terms and extend the categories in different directions is part of today's agenda

Overview of exemplary syntax with examples.

Overview of attachments: attach the preferences to the specific content. Different methods. Currently two:
- HTTP headers
- robots.txt
- Expect over time different content formants (for example metadata in file). Currently not discussed.

Start of meeting discussion

Main contentious points:

Most prevalent critique is the TDB name, not the substance.
AI/Gen AI: not much discussion.
Search: still some discussion including some sub categories. Feels like search needs a bit more discussion. Sub categories should be discussed after the definition of "search" is agreeb by the group.
Inference: Also still need alignment to group all AI use cases vs split out futher. Even here sub category discussions should be delayed a little.

//Ted Hardle:
//Search: Is this a summary providing system or a reference providing system? does it impact all users or just atuomated systems.

**Chair (Mark) kicks off TDM discussion**

Some folks believe TDM term is important to link it to what is happening in Europe. Others beleive that's a bad idea as some of the legal definitions have not really been settled yet, therefore we should change the term.

The text definition is quite generic at this point. TDM is the only term left that could be linked to legal definitions.

Member: would like name change. People are getting caught up on the definition of TDM whilst the purpose of this document is meant to be more generic.

Member: name change would be great because we go towards a more jurisdiction agnostic definition. Concern: if it becomes too broad then if they disallow automated processing it's going to exclude a whole range of non commercial purposes that are probably good.

Martin: the preference is broader than what the law allows you to express. Reinforcing that this is a preference. Definition is good as is.

Member: largely agrees with renaming TDB. Understands the concerns of the legal alignment.

Chair: our role here is providing tools to allow preference but not make policy decisions. 

Member: "Computation Analysis". 

Member: Broader possible all ecompassing category is important as it will likely be above any jurisdictional differences. 

Member: Support everything has been said. Happy with top level definition. As long as it's short.

Member: if we have a too broad of a category like "all" it becomes the same as robots.txt original purpose. But if you do look at HTTP headers then indeed you need a broad category.

Member: There will be many cases where preferences listed here will not be applicable. There is a distinction to be made that robots.txt talks about crawling. The rules here govern the use of the content after it has been obtained.

Member: "automated access"

Member: Should we consider non machine automated access. Creative Common licences. 

Member: Need to be crisp on collection VS use. Are we saying that these preferences are agnostic to how the crawling is happening? understand this is a theoritical distincition but in reality they will be linked.

Member: we do have a distinction between collection and use. What we are not clear on, by choice, is who makes the distiction and when. But out of scope.

Member: propose to continue to focus on "use" in the same way we decided not to deep dive on too many sub categories.

Member: agree that people out of this room are not making the disctinction between crawling and use.

Chair: everyone seems to be re affarming to focus on "use". 

Member: "Computational Use".

Chair: should not need to bike shed the name here, as long as we are directionally in agreement.

Member: Reminder for it to be short label.

Chair: move on to next topic. AI / Gen Ai.

**Chair (Mark) kicks off AI / Gen Ai discussion**

Member: AI/Gen AI seems to be quite well defined and overall in a good spot.

Chair: any suggestion for improvements?

Member: No issues. Long answer: I have issues but not sure how to fix them without another 9 months of time. So for the target "ASAP" this is the best I can imagine.

Chair: Agreed. And is looking to a "good enough" while leaving doors for improvement open.

BREAK

Chair: raises the concern of Presence of regulators

Member: we are here just to understand. Are not part of the legal team. That's why regulators are here and absolutely not here as a legal hammer and just here to understand.

Member: here as an observer just to learn and understand. It's refreshing to hear the broader view and very interesting to be here.

**Chair kicks off the topic of the delineation between genAI and AI training**

Member: if gen ai is general purpose models...

Member: AI training is for any purpose (e.g. classification). Gen AI is a subset for generation of content. It's not about specific purpose models.

Member: Most, if not all, current large foundation models are capable of generating content. Wouldn't the AI training category then be empty?

Member: When only looking at large foundation models, yes. But there are also specific-purpose models that are not designed for generating content. Those would fall into the AI training category. For example models for medical applications. Having two separate AI training categories allows declaring party to say yes to such applications while saying no to GenAI, or say no to both. The GenAI category is where most of the concerns/desire to make declarations lie.

Chair: we should add examples maybe to better deliniate the definition?

Member: supplemental material as they would very quickly become outdated.

Member: Lots of protections built in gen AI models...

Member: Where to classifier and preference models fall? As gen AI models can *also* do classification....

Member: Agrees that delination need to be clear. Classifiers falls under which... it really depends on underlying tech

Member: the current definition is the best balance we could come up with. 

Member: Should we drop "training" from the vocabulary.

Member: training is needed as it's all about usage of the asset. And training is a core use case.

Group: Additional discussion around adding more examples.

Member: This is going to move fast, how are we going to keep up with updates in the context of the IETF process

Chair: definitely being considered how we keep updating this over time

Member: These two categories are fine. One view is that translation is generative, because it generates text or audio based on an input (contrary to what others have said, who argue that translation is not generating *new* content). But the question is valid: does it need to be generating of "new" content to fall under the Gen AI category? If so, "new" should be added to the definition of Generative AI Training.

Chair: we should move on and discuss this issue futher over lunch.

Member: Anything we do now should allows us to add "more" to the definition later, but should make sure we don't "change" definitions at a later date.

Member: Remove capitalisation of "General Purpose".

Member: will be making a number of tweaks to the definition. Idea of "new" content will be considered. Still some things to think about.

Member: translation is condiered as derivative content under copyright.

Member: We are talking about the trainining of the model that performs translation. not the actual use of the content as input for translation.

Summary: Concerns that one of the categories will be emtpy and might collapse. That might be fine. 

Chair: focus on expression of preferences. Time to move on.

**Chair kicks off the topic of the search catgory training**

Member: This category is important to have as it's a use case very relevant to online content creators and did not want to risk the other categories excluding "search" as the use case.

Member: note, this is not longer about training. This is about more "classical" search functionality. The goal here is to make sure that this use cases is not affected by other terms in the vocabulary.

Chair: the elephanet in the room is the summarisation. From the chair perspective this could be not we are focusing about here, but understood that if this is an importnat use cases it might pop up in the vocabulary.

Member: the intent is important here. One way to think about it: is the intent to send traffic back to source or keep the user on the search engine site.

Member: Reminder this is a spearate use case from training.

Member: distinct set from AI training.

Member: This category falls into more "old school" search.

Member: this is an important category. Referrals, accuracy. It's not clear that this category enbales that.

Member: this section may have lost some flow as the context here is very different. Transformation of the content is importnat to consider as if you transform it may lose the intent of the author.

Chair: reminder this category here is to make the "search" use case explicit even if someone dissalows the use of AI.

Member: the disctinciton - ca content be used in AI system VS can content be used in a search product that uses AI.

Member: worth investigating specific points to transformation. primary concern is comparison and how the preferences are reslved. What has been said is search is more specific is AI. If someone says AI as NO but search in YES - but that's not reppresented in the model.

Member: this specific category will have a lot of focus. Robots.txt does not really address search direcly. It's focused on who but not what. Just flagging it.

Member: Definition feels fine, although transformation is important topic.

Member: is snippet generation transformative?

Chair: there is a range of transformation even in just "snipper" generation.

Member: All search engine offer opt out of snippets. There is a difference between generative VS non generative.

Member: two concerns: linking back and accuracy. The document only addresses linking back. Accuracy we can't address here.

Member: search category addresses traditional search....

Member: Suggestions were made towards defining more precisely the use of the content.

Member: reminder this is not just about "web search". Think about document search.

Member: we've moved towards down a paired down version of search category. We should supplement this with some additional text. This does not speak to the use of the AI. Some of the concerns being raised feel a lot more related to the inference category. These are distinct and separate.

Member: traffic from AI systems is increasing.  Should we have a separate category for agentic AI.

Member: what about search that happens in locally implemented applications? Should it be an addition to the document.

Chair: we put search in because we wanted to avoid uncertainty. This discussion has gone a lot broader around controlling the "behaviour" of search. And although our charter does cover that, it is a specific use case and very narrow so let's move on. Goal here is to get the basics in. Group agreed.

Editor: overall fine but need more context, so more text.

Member: in the IETF process how are adjacent technology handled. How we invoke adjacent solutions that might answer the questions people have that are addressed elsehwere.

Chair: we do have some tools, documentaiton guides, wiki, applications guides and similar.

Editor: explanation of process.

LUNCH BREAK

**Chair kicks off the topic of the inference term**

Editor: General consensus on the need for an inference category and that there is a contextual seperation from the training category. There is some feedback though that the inference (or RAG) category coinflates with "operating" on the data VS simply "retrieving" data. But so far no one has suggested a separate category about this.

Member: is there a scenario where there is no inference at all after a model has been trained? Is there word "inference" the wrong word.

Member: there are definitely different cases: RAG, lookup/fetch, style reference, composition.

Editor: also note that the end user initiating an action (or not) should be considered. Some say we need to find narrower definition of inference.

Editor: is there a difference between a user requested task VS a background long running taska and full automation.

Member: I'm in the broader definition camp. Does "inference" only applies to gen model? A classifier type model, assuming that is inference, should it be seperated? Feels like it's naturally more tied to the gen AI side of things.

Member: Back to seperating based on user action vs automation. With agent in the mix at this point that line gets blurred very quick so not worth exploring that path.

Member: example use case: legally acquired a copy of a PDF report. Nobody could argue I could use a PDF reader to read it. If I use an AI agent instead, is that meaningfully different?

Editor: Those are different because it's about controlling presentation. Arguably that's why it's a PDF report.

Member: each vendor will need to make a decision around how to process these preferences. Not controls. PDF has a lot of this built following up on the example given. And a lot of viewers don't follow a lot of these...

Member: back classification/vs gen ai inference: I think a narrower definition makes a lot more sense. And it should be focused on machine readable as the consumer is bots, not humans. In that context, we should focus on "automated" use cases. Not humans driving an agent. In favour of narrowing the definition.

Editor: reminder that this is not an tool to satisfy legal compliance. It can be an input.

Member: would it be better to focus on an inference category that is aimed at the actual "use cases" we are trying to solve, rather than define "inference" globally. Basically focus on the use cases: summaries, creating an image etc. etc. Current definition if very wide.

Member: it is difficult that it is so broad. One thing to consider is just accepting the specificity and then accepting the sub categories will be handled later.

Member: agreed. But we should add at least one sub category (like summary) else it won't be useful.

Group: further discussion on broad vs narrow as part of this first iteration.

Member: proposal from member on reframing the category.

Member: I think we are in the "how do we not paint ourselves into the corner" discussion now, and I think that' s probably the right place for us to be.  The previous speaker suggested we create a hierarchy, but I think it makes sense to split the categories and decide later whether or not they nest. From my perspective, the issue is not where the content comes from, but whether the content owner permits the creation of synthetic output using this or not. We can then decide whether a specific thing is synthetic output or not (I don't agree that text to speech is, and I also don't think translation is, but that's still for discussion).

Member: Likes the training/inferece as two parallel paths. Gen training VS ai training - generating inference vs ai inference. Maybe that's enough of a distinction to cover translation etc.

Editor: that's a useful symmetry.

Member: prefers broader approach w/o specifics as we are going to miss out others. Do the specifics later.

Member: disagrees and says generative/classifier inference is a good split to do now.

Member: provides a definition for the split in writing.

Member: likes the idea of mirroring the two categories (training vs inference).

Member: still hard to distinguis the two suggested categories if the question is asked to a gen AI model, as that can also do more standard classification.

Chair: hearing approaches and concern of schedules. Show of hands on splitting VS keeping generic.
O1: prefer broad: 11
O2: prefer narrow/split: 4
O3: strongly oppose broad: 5
O4: srongly oppose narrow: 5
O5: need more info: 9

Member: This topic is evolving so fast that it needs to be carefully considered.

Member: what needs to be known to achieve more clarity. Needs to dive into more specific uses. Is it better to include an overly blunt? not satisfied with or remove it alltogether...?

Group: discussion on show of hand options. 

Member: making progress on MVP - better for future compatibility - then start with a narrow category only, this can still allow for extensibility.

Member: scoping it down feels like better for solving use cases right now.

Editor: risk of broader definition only is that it catches things that become collateral damage.

Member: from the end user perspective what are the implication of having such a broad definition. How will it affect their experience. So it's better to define it very narrowly.

Member: there are too many uses to be narrow. Is it possible to have a slowly defined definition?

Chair: you can't coordinate across the Internet so you can evovle a definition, but you can add new terms.

Member: then we should keep it broad and add terms afterwards.

Member: the specification can be broad and supplmented by external documentation.

Member: Given the concern about the broad category - but it's still a better outcome than not having the preference at all. So we need to start somewhere.

BREAK

**Chair kicks off hierarchy conversation**

Editor explains hierarchy over a whiteboard. Discussion aroind hierrachy logic and priority. Overall everyone in agreement and understands the model. All is good here for everyone.

**Chair kicks off extensibility conversation**

Adding items as leaf nodes is straightoforward. The "sandwich case" is the harder one and should be avoided (adding a new category between a leaf node and a partent node). Explanation of the "sandwich case".

Discussion around registry and updates to the vocabulary / tracking and so forth. If we did not have a registry, we would have collissions. So updates will be provided by new RFC.

Member: should be hard to update values given the complexity in defining the terms.

Member: agree. Having a registry makes it too easy.

Editor: agrees. Publish documentation on process but IETF group should ovesee additions to the vocabulary.

Member: one extensability factor not controlled here is the attachments. Need to keep that in mind.

Member: need website with all the relevant RFC. HTTP working group does a good job at that.

Editor: other type of extensions may specificy additional variables. For example, on the snippet sub category the max limit of the snippet string. This type of extension is allowed and should not be problematic. Three types of extensions:
1) new categories
2) new attributes and adding new semantics
3) new stipulations of refinments to the existing categories
Plan is to tackle new categories and remove any possibility of a registry.

Member: leaf categories don't need too much scrutiny.

Member: two concerns about hierarcy. Not sure TDM is that useful. Cateogry only makes sense if the sets are distinc sets. Else hierarchy falls above.

Editor: combinations. Assets only have one definitions (image metadata for example). Should be compatible. For now we are defining robots.txt and HTTP header. Issue is what do you do when there is a conflict? robots.txt saying yes and header saying no... current document says least permissive.

Member: advocating for two levels of override. Unit based override location. Specific user agents override * in robots.

Discussion on hierarchy. 

Member: need to be very cautious when discussing overrides especially if thigs get used in other context.

Discussion on the meaning of three states: y, n, I don't know.

Member: ability for changes to propagate will also be very important in the future.

Member: In a world of preferences we just need to make it clear what the ovveride logic is. But beyond that it's out of the scope for this group.

Member: having overrides is best solution. As described is also adequate. Second: domain is not tackled.

Editor: relevant meta data applies to relevant copy of content, even if the copies are identical.

Member: very worried about the overrides. As ultimatley the owner is not necessaily the entitity defining the preferences.

Editor: maybe we don't do any override logic. We find a generic way that simplifies and simply says: whatever signal you find you process. And make that explicit in the standard.

Member: Back to preference - find it hard to consider this as a preference when in some jurisdication robots.txt is already mandatanted as the official methord to declare content use.

Members: Discussuon on registries.

Editor: no general framework of combincation. As we can't predict the attachment forms.

Member: worthwhile adding link back to combination in attachment document.

Member: it is in scope to make it easier to make it easier for crawler to figure out how to make a decision on a given piece of content.

Chair: currently out of scope but can be added at a later date.

CHAIR ENDS MEETING











aipref Design team meeting Day 2

Open work for the day:
- attachment: robots.txt syntax
- vocabulary: inference time category


## Attachment (Morning)

### robots.txt Syntax

Goal: no breakage of robots.txt usage for folks not using Content-Usage / preferences

Goal: easy to add preference declarations

Martin: rough existing syntax is that User-Agent defines groups, and unexpected/unhandled lines should be ignored. Confidence that most implementations are robust to this (will not be disruptive to add new lines).

Gary: combination of preferences seems like an important issue

Martin: bots will generally look at up to two groups: any "star" ("*") default group, and then any specific/local group

Some (newer?) bots don't respect "star" default groups, only named bot sections. Discussion that this violates the spec.

Overall, any AI preferences need to be repeated for each group (aka, each named bot). Can't simply rely on "star" group as a default.

Gary (with Google hat on): A recent issue has been robots.txt files have been getting large with many hosts listing a growing number of bots by name, in particular to control AI usage. May need education around robots.txt usage.

Despite specification, in the wild crawlers often attempt to combine crawl path directives because robots.txt files contain repeated groups for the same bot name.

Q: doesn't "star" group set a default, which bot-specific group refines?
A: no, if there is a group with exact bot name, that is used and "star" group is ignored

Current draft text: if there are repeated preferences for the same path ("equivalent path"), then they are treated as separate attachments and combined according to the rules in VOCAB Section 7.1

In robots.txt, Content-Usage lines *do not* combine like HTTP header folding, because they (can) have a path component

Conversation around the combining roles having flipped behavior from Allow/Disallow combination rule for robots.txt, and whether to stay consistent with AI preferences combining rules or robots.txt combining rules.

Comment that many folks writing robots.txt files are less technical, and concern that there may be confusion around this flipped behavior.

Chair: counter-proposals are needed for combination rules; preferably later today or next week

Timid Robot: requiring path part to always be present (visible) instead of empty-string implicit behavior, could help reduce confusion

Comment: in the examples in the draft text, the Content-Usage lines should follow the Allow/Disallow lines

### Time of Attachment

Content might be crawled at one point in time, with specific preferences expressed. They might then be used at a later point in time.

Some attachment mechanisms may have different behaviors around this; particularly location-based (robots.txt) vs embedded or HTTP header.

Presumed expectation from publishers that if new preferences are expressed, they will be factored in eventually.

Cases where websites change structure, or content is no longer online.

Discussion of web archiving, and whether attachment information might be re-fetched (distinct from re-crawling the content itself).

Registries are likely to be distinct and introduce complications, because they do explicitly allow updates.

Chair summary: the general expectation is that for the current attachments, preferences will be computed at time of acquisition and ride along

Comment about the specific point-in-time change when the work of this group is released. Some actors might intentionally decide to use historical captures/crawls which pre-date AI preferences, and interpret those as being permissive

### Discovering Relevant Attachments

How do folks doing a specific task (such as web crawling) know which attachment mechanisms 1) exist 2) and are relevant to their task or use case.

For example, a registry, or guidance in an RFC.

Short discussion of motivation for having multiple attachments: limitations of robots.txt, different parties involved, etc.

Current draft text mentions specific other attachments (embedded) but not others (fingerprint/registry).

Chair and Editors: recommend submitting PRs to discuss further attachment mechanisms

### Clarify Distinction between Usage and Acquisition

Consensus this should be clarified.

### Clarify lack of preference

"No preference is no preference"; moves to editorial status.

### Discussion of Other Attachments

(filling extra time for discussion before lunch)

Clarification that the string serialization may be common between HTTP headers and robots.txt, but are not necessarily universal: for example embedded prefs may be file-format specific.

Discussion of HTML embedding via HTTP header meta equiv, versus robots.txt metadata. That specifying HTTP header can happen entirely in IETF.

Discussion of whether this group should specify *anything* about embedded attachment. For example, requiring that the semantics match.

More discussion of embeddings and obligations. For example, proprietary formats which may need a licensed parser implementation; these concerns are out of scope for this group.

### Alternative Vocabulary Term to 'tdm'

Question raised whether there is consensus on having a top-level grouping in general. Discussion about process, references to mailing list, referencing previous conversations.

Timid Robot: recommends "usage" as alternative term to replace "tdm"


## Inference-Time Categories

The question whether to have a single broad inference-time umbrella cateogry, or to provide narrower granularity; either with a sub-category or multiple parallel categories.

Reminding from the informal vote yesterday, there are many opinions and not broad agreement.

Paul: summarizes current language: "using assest as input to a trained AI/ML model as part of the operation of that model (as opposed to the training of the model)". Could include or exclude user input versus external sources.

Leonard: has submitted a PR which aligns inference-time categories with training-tame categories.

Martin: distinction at training-time has to do with capability of model being trained; while inference-time should be about use of the model

Discussion of definitions and examples: asset as input for prompts such as "how many words in this text" versus "translate this text to another language".

Comments expressing concern with the overall concept of inference-time restrictions, trading off a large amount of potential social benefit; centering end users as decision makers in uses (versus intermediaries); legal backing (or not) for restricting certain uses.

Chair: overall framework has been that preferences are preferences, and exceptional uses for accessibility, research, etc are already carved out.

Martin: need to have text in the core specification (VOCAB?) that certain uses, such as anti-spam, are not in scope for these preferences.

Discussion of unintended consequences on businesses; rights of users and creators to express preferences in general. Many comments on social impacts of AI applications in general and role and enforcement of preferences. Perspectives of publishers versus AI businesses.

Reminder of discussion from yesterday that it isn't possible to go from narrow to broad (versus narrow to broad).

Mention that having no inference-time category at all could result in many parties expressing preference "tdm=n,search=y", which would rule out an even broader set of uses.

Chairs: not feeling consensus

Discussion of what to put off versus include now, and what the impacts (harms/benefits) are with having a time gap.

Mention of existing tools implementing inference-time preferences, making an inference preference important. Chair reminder that this important input, but not decisive.

Discussion of what it means to be compliant with a specification in the abstract; example of Content Security policy.


## Next Steps on Inference Category

After a snack break, discussed next steps to resolve inference category.

- changing the name
- adding more context
- giving a conformance target

Chair: plan to get out additional language by next week that we can discuss

Timid: additional work to be done includes user education

## robots.txt Combination

A bit of discussion around combination questions: multiple matching lines with different preferences; and possibly differences between robots.txt HTML metadata and robots.txt text file.

In the court of editors.

## End of Day

Checking in on next steps. This may be last dedicated in-person meeting for this group (distinct from meetings at IETF itself).

Discussion of re-chartering.

Chair: will share feedback upwards about this type of working group, which is more policy-oriented.