# AI Preferences - IETF 124 Minutes

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Monday, 3 November](#monday-3-november)
  - [Overview (Martin) slides](#overview-martin-slides)
  - [Foundation Models](#foundation-models)
  - [Search](#search)
  - [AI Output](#ai-output)
- [Wednesday, 5 November](#wednesday-5-november)
  - [Discussion on top-level category](#discussion-on-top-level-category)
  - [Chair summary](#chair-summary)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



## Monday, 3 November

mnot: [slides](https://datatracker.ietf.org/meeting/124/materials/slides-124-aipref-overview-00). updated milestone August 2026, still in question

Goal: go through feedback on definitions for:
*    foundation
*    search
*    ai output
*    automated processing

We need certainty on these terms first, will get to other things if we can.

Suresh: Productive discussions need to rely on these as a foundation

### Overview (Martin) [slides](https://datatracker.ietf.org/meeting/124/materials/slides-124-aipref-vocabulary-status-update-01)

* https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/
* Discussion in Zurich seemed to be a positive direction but turned out to be difficult.
* We started with a picture (in prior drafts as of 2 weeks ago)
* Revelations were the interesting part of zurich
    * We do not have a shared understanding of what search is
        * Know that search uses AI but we differ on how much
        * Some search providers use both trained models, but some also train the models
    * Prior def'n of search primarily directed people to a location from which the assets were retrieved.  
        * This became problematic
    * We ended up with a picture that collapsed into the concept of creating a foundation model
    * There is no certainty about the structure in the presentation. 
    * Definitions are in flux, the picture changes depending on those choices
    * Top level category is at risk.  Lengthy discussion raised pros/cons.  
    * Some people deliberately want a top level category so they can say no to things they don't know abut. Others think that is a terrible idea.
    * This has always been contested
* Foundation model training - preferences over what happens within a system did not generate interest, but if a foundation model is what pops out the other end, that changes interest
    * Foundation model definitions do share a general definition. 
    * Idea is to avoid contention
* AI output - culmination of many discussions, rooted in concepts Microsoft proposed and massaged into different forms
    * Core idea: concentrate on observable outcomes.
    * Idea is that AI systems are substituting for things that have previously been used
* AI Output
    * Additional conditions: if you use a thing to produce an output, you need to take an "excerpt" of the thing it came from.  
    * Current definition: if you will put in output, don't paraphrase just inclue links 
    * Some called it lederhosen but that probably won't stick
* New direction coming out of Zurich did create new problems
* Definition of producing a foundation model is challenged - nobody knows what "fine tuning" means
    * Could include system prompt engineering (to some people) - others shake heads
    * Other techniques like LoRA also are references
* Output
    * what does it mean?
    * Question: "things that are presented to a human" - what does that mean?  What if it is agent-to-agent?
    * Would "once it leaves your domain of control" be better?
    * Unclear what it means to say yes or no, is the output stage decoupled from the system internals? 
        * Eg: Search - many things, ranked then presented. Model may rank, staging may be decoupled.  But search apps have more complexity.  examples of search that does more than rank exists
        * for chatbots, etc - how to determine if internal ranking doesn't "leak" to the external output
        * Goal: what tests would be applied to know if something internal has leaked out.
* Excerpts & Links: 
    *  Naming
* Consensus is emerging 

Mark: Happy to talk about the four terms. Order is based on "solidity". Goal is to get solid things out of the way first

### Foundation Models

Roberta:  foundation models related to the article foundational agents that construct the LLM models?  There is a 300 page article (https://arxiv.org/abs/2504.01990). 

Martin: No not familiar to that 

Roberta: how is search part of this conference? It seems to be unused 

Mark: added search early on because needed a way to accept search for that application so that intent was clear.  In discussion, some want more fine-grained search controls but original intent was.

Martin: understanding is exception would be necessary. Those building search use foundation models. Some are exclusively foundation models. Have been tweaked but are still foundation models

Bradley Silver: question on fine tuning.  right now focus is on foundation models because they have the broadest foundation upon others are based. For some the focus will be on fine tuning, creating different apps on top of the foundation model.  These seem distinct enough to warrant being dealt with separately.  The value/use of the data used to fine tune could be very different.  Eg: medical journals as a fine tuning to a more generic model. The focus on foundation model could become less important over time

Alissa: if we imagine the foundation model production category was an AI production category, would the fan of prophesies be the total span of everything anyone can do with AI?  ie is this a case of input + output = everything (please corroborate)

Martin: I think it would cover a lot but it might not cover everything

Alissa: if the AI output category was the foundation model category, would THAT cover it all?

Martin: I don't know that there would be things that could be called foundation model but would be called AI.  Maybe this is different for everyone

Alissa: other entities have defined these terms, if we can reuse we should

Martin: all of the definitions agree except some specific things might disagree (eg: number of parameters).  Most are very much in agreement. Self-supervised learning is different as it uses the term "probably"

Alissa: because defn's are in flux, a set of use cases to test every time they change that cover all the subjects of discussion would be helpful.  

Martin: we all have our own tests, it would be helpful, but it might be early

Mark: wiki page would work?

Alissa: yes

Ted: IANAL but lawyers shepherdize.  Go back through precedents to look at what is cited in context.  Manual search had citations that you then followed at great pain.  I worry we are focused on how and not why somebody would express a preference.  We are not shipping an org chart but we are close. Given we want to express a preference, what is the middle ground of those who create and those who identify with a preference. Many small creators for example if asked whether an expression could be possible using short crisp words. 

Three broad categories: 1) citations back from interaction.  2) Asking for an answer. 3) I don't want either 1 or 2 I want an interaction.  That is a conversation that can be had in places like a fanfic community.  This is AI preferences, think about the people that need to be expressing.

Shay: came up with a couple of definitions: historical search, where direction exists to original content.  2) pulling data to permanently modify a model 3) summarize but dont modify

Is there a broad category? Don't have, there are other definitions that need to happen first

Eric: thoughts similar to last 2 comments - can we be quantitative about dimensional use - eg, a lot of elements are how much does data get aggregated and mixed in, vs how much is preserved. Foundation model building mixes much together and context is lost, difference is less about things being separate as how many things have been pulled together. Can we have a quantitative scale of 1:1 in/out or "aggregated according to this scale". 

Nick: I like the proposed changes - a way to help decide could be, AI crawlers need to know themselves & which category they fit into.  Teams in companies who build small tools may not know where they fit in, may cause deeper analysis of who does what, but if crawlers can self-categorize that is a good metric

Roberta: when you say other ML techniques I think about foundation models too, to take a foundational model and see it as an LLM it is a way to see how agents will interact within a system. When you put that into perspective there are people in chat talking about singular models, which is broader if we are talking about deep learning we are missing some things, is this a common issue? 

Mark: there is a broader category

Any other feedback?  May not be worth polling. Ted's suggestion could be fruitful. A large part of complexity is that use cases are broader than the search & chat context Ted covered

Farzaneh: we need to be clear that by publisher we don't only mean those with protected content.  Eg: social media/media may be the owner of the content

Mark: interpreting as we need attachment use cases

Farzaneh: yes needs to be transparency from declarant to those doing the declaring

Timid Zehta: want more information on articulating IP/copyright of the declaring party.  Seems counterproductive for expressing preference. While many want expression because they are copyright holder, others want cost(? please corroborate) of the provider making the declaration. Tying back to other legal rights might reduce efficacy and duplicate controls/legislation that already exists
    
### Search

See the slides for 4.4 Search

Martin: "I think the previous search definition was better" (audience laughs)

Alissa: It is easier to consider without nesting

Martin: getting sense that nesting doesn't make sense, according to Ted's principle

Meredith: Search is the only category that lay users don't understand.  Users care why you are using a tool, not what tool you are using.  Is this competitive & substitutional. Search def is good, I don't think it matters what you use, imprecise defs is fine, they care if you create a book that competes in the market, not that you create one for yourself, even if the same tool is used

Martin: tere is a 2nd order effect - something used innocently is then used destructively.

Meredith: can you distinguish a children's book creator from another use such as a disabled person creating a simplified/altered version.

Martin: good point, counterpoint earlier was open white models have no hope/control over what someone does downstream, no ability to differentiate between good/competitive uses  Maybe you mean we shouldn't try

Meredith: little bit

Mirja: people who think they have a preference and want to express may get something else, no way to match to expectations.  What is better is to point out two features - reference & asset.  

Martin: I disagree

Mark: you say these two constraints are not adequate?\

Mirja: they might be but they also may not be 

Martin: providing the location is the very definition of search, we are trying to narrow things down to something that may not match what people are intending to do

Mallory: Instead of search could we define the broader category as derivative? ie a summary or a blurb. CMS or other things train web admins to build metadata for search, eg title, thumbnail.  Search different from any other kind of derivative, not just webpage but also attached metadata.  This is important special case but other things are there too where no metadata taxonomy is needed, there might be more intelligent ways to smash things together.  Important to create a derivative def'n that includes search but has more

Bradley: the 2nd bullet (asset can only be represented) gets us in trouble.   Also concerned about bootstrapping training into these categories.  Puts a blindfold on because those expressing don't know what kind of training will be required. This dilutes the power of making an informed preference.  Biggest problem with nesting: search is about saying "yes", everything else is right to say "no". This creates lack of clarity. Should be brought to higher level so it is clear what prefs are expressed. 

Timid Robot: search is good - evocative but too generic. Solution: add a modifier eg indexing search, citation search etc.

Alissa: comments are addressed by Krishna's draft.  Encourage us to bring those concepts in. 

Martin: we struggled to do that, thought it could be "this plus"additional constraints. Were not sure it was in the charter but it is a reasonable thing to do. Eg: an excerpt could be the entire thing. 

Alissa: fact is we can't ignore it, not worth doing something super simple if it fails to work in the broader context of search

Nate: I run a small travel blog, agree it is important to talk about why this is even important.  This is a simple definition, I could explain it to my travel blogger friends. Concern is that lines between search and other AI applications is blurred. W/o the 2nd bullet point the definition is problematic.  The Why is: is there a fundamental fair exchange where enough people make it bak to the website.  Mere existence of a reference isn't enough because no user will click 91 times (for 91 pages of results). 

Farzaneh: Krishna's draft should be reconsidere.  Need to go back and see what can be taken, not perfect but... I am a small operator but somebody else expresses prefs. I don't know what they do on my behalf when I get busy.

Mark: have been working with Krishna's draft, he has just opened new issues in the draft. If you see things that are missing from Krishna's drafts let us know.

Suresh: One more data point:  mapRG - how many folks ever change the defaults.  Concern exists over why we do the right things

Vitoria: many expressing preferences would find some things missing. Trying to nest search within AI output is confusing, we should separate it out.

Martin: we have overwhelming feedback, consider the separation done.

Timid Robot: asking for more clarity from Victoria, is unintended consequences more about the unlimiting 

Victoria: all these definitions sweep up a lot but search tools now do not include verbatim but summarize helpfully for some users more than other.  It isn't just about search.



### AI Output

Mark: this is new post-Zurich but we want any reflection we can get

Erin: the idea was to focus only on output, use of clients re-introduces the internals that we tried to exclude.  There has to be a way to strongly define this as an external boundary not just internals talking together

Martin: we have a problem with agentic browsing in this context, how do you tell it is a human on the other end.

Erin: clients can be software too

Martin: does the entity that talks to the human have a mandate to protect what happens downstream?  From the outside you seem to have a monolithic thing, but systems take a tiny piece and solve, potentially across administrative domains, which might be integrated etc. If one of those components takes in an asset that relies 3 levels downstream, how do those components fulfill the promise.

Erin: if you are going to express a pref about end state output, nobody should be trying to dictate actions of the internals

EKR: if I have a procedure, have a corpus of data. Spit out 50 exemplars & user hates it. Now foundation model is on, AI output is off. Is this legal.  I don't think org boundary is right - create a foundation model that generates code (true vibe coder). Is that AI output?

Roberta: the idea is the agents talk to each other, no human interaction in the middle.  No visibility for the last node. Think it is a design issue. Building systems where AI is a human in the system. Not covering it such that opt out is clear, yet also not stopping progression of data.  Hard to have all 3 groups agreeing at the same level of control

Elaine:  this is written to be broad.  Can someone explain intention. Don't understand 3rd paragraph. 

I think this is fairly new, if you have suggestions please send. 

Martin: Erin might be better person to define intent

Elaine: Hard to offer suggestions when I don't understand intent

Martin: happy to poke on specific concerns. 

Mark: good feedback, becoming clear more work is needed

Elaine: if we delete that sentence, who screams, what would be missing.

Alissa: Have read 30 times but don't know what it means. Having use cases helps. If there is no use case where a preference expressed doesn't need the organizational boundary - eg if SaaS trains a model then the model is used, maybe there is no need to distinguish between the model training and the output of the model.

Martin: how would you test the difference between respecting a preference and not?

Alissa: how does it happen today?  

Martin: there is a simple test - did this crawler request this resource

Alissa: translated to the real world there is a test - did my stuff end up in that output

Martin: in very specific circumstances can we test whether this expression was respected or not? 

Alissa: everyone will make their own judgements.

Martin: but as a systems builder you need to now where the line sits.  As an expresser you should be able to draw that line.  Fundamental question: 'in the generation of outputs to the system' in 4.3 AI output:  in this definition you could use this system to do anything else other than generating outputs, is that ok?

Ted: definitely more confused now than earlier.   What changes if I take AI out of this?  If I have prefs about how my prices are used, I don't (might?) care about whether somebody builds a price comparator, if you build a weather system where my expression allows an aggregation of weather data, that is meaningful.  All we can do is write what the preferences meant to those that expressed them, and then allow systems to try to interpret.

Mark: maybe we need to re-charter based on this

Martin: Bradley Silver's draft is clear about intent, we haven't had much discussion (ed: this is important but I didn't understand context, please flesh out)

Elaine: do we need something about model training in AI output?

Martin: right now everything is in jeopardy, but that is a good point. Concern is if we don't allow some training, but without search maybe it doesn't matter. 

Meredith: a lot of unintended consequences come back to substantive use may solve some issues but create downstream problems

Roberta: One example for AI prefs: if we are trying to get maximal data about medication information and provide to users.  Whole system will have training etc, but medication might not be open to market yet still be crawled, information could put user at risk, they might know that the content was trained by an AI etc.  Even internally, those models are classified as high risk. Behavior of someone who ignores preferences must be considered. Lots of crawlers ignore robots.txt. Is liability/enforcement out of scope?

Victoria: +1 to unintended consequences, not sure we adequately value all the use cases, or cost vs. benefit. That is not a task for standards bodies, that is policy etc. 

Martin: section 3.2 might address your concerns.

Victoria: does address to some extent, but will still have impacts.

EKR: you  suggested 3rd paragraph, the undesirable consequence: even if you stipulate this is nested, there are other types of training.  Not saying it can't be fixed but you will have trouble

Lila: I agree with those who advocate layperson understandability.  Will try to come up with language. Also concerned about substitutive use, but competition is important for society, need to think the balance of tools give vs. narrowing what people can do on the web.  Section 3.2 very important - need to maintain that there are good reasons not to follow the standards.  Flexibility is important, more risk averse entities may not take advantage so concerns remain, especially for those needing accessibility. 



## Wednesday, 5 November

(Scribe: Christopher Patton)

### Discussion on top-level category

* Whiteboard notes from a previous meeting
    * **For top-level**
        * Valid to express demand
        * Known / unknown / rapid change
        * Complete vocabulary
        * Alignment w/ regulation
        * Suits opt-in / optional
        * Promotes market
        * Ease of use
        * Vocabulary portability
    * **Against top-level**
        * Unintended consequences
        * Inhibits innovation
        * Misalignment w/ regulation
        * Bleed into non-A.I.
        * Inconsistent understanding
        * Charter impact
        * Definitional impossibility
        * Learning sharp tools

* Lila Bailey: Accessibility tools
    * Many use the tools we're talking about here
    * If the only answer to those making these tools is "too bad, you can't follow our standard", then I think we're doing something wrong

* Ted Hardie: We're looking at this as a hierarchy
    * Category of unknown uses
    * Trying to find ways to express how a piece of content can be used
    * Need default behavior for unknown uses
    * Chair followup: What would be a reasonable default?
        * In the absence of a preference on the part of the content creator, the action is up to the consumer

* Timid Robot:
    * If we replace the hierarchy with an undefined-in-stated-preferences category, we don't remove the problem of unintended consequences
    * If we reduce the scope of the top level category, would that address Lila's concerns?
        * Lila: I'm in favor of narrowing the top level category to somewhere in the AI space
            * People use AI tools for accessibility
            * Stomps on rights a bit: There's a lot of things I'm allowed to do with a physical book; I should have the same freedom when consuming a website

* Meredith: What's useful for content creators is not useful for people consuming the web
    * Disabled peoples' advocates aren't in the conversation
    * Some preferences should not be enshrined in the standard because they're not socially beneficial
    * Universal design: we need to default to open (for accessibility and other things)

* Martin T.: We all have different definitions of the top level hierarchy in our heads
    * "human versus automated" maybe one way of slicing the data
    * We're pulling from legislation that is behind the state-of-the-art => we need new text.
    * Need constructive ideas for how to improve things rather than just hearing the standard doesn't work
    * Question of hierarchy or not is not useful: better to try and improve what we have

* Bradley: There's a worry that if we don't define this category, then someone else will
    * "Veto power" is loaded
    * we're not operating in a world where there's visibility into what crawlers do
        * if you don't tell me who you are, then let me tell you what I am willing to let you do with my content

* Alissa: Geopriv WG (from back in the day) had a very similar to debate
    * People do whatever they want with the things you don't define. Nothing we can do about that.
    * Glad Section 3.2 is there, but it's not sufficient
    * I dno't see the value of the top-level category
    * If the other three categories can be defined, then maybe don't bother with this one


* EKR: Structure of the spec: if there is some use that's not written, then there's a "catch all"
    * There doesn't seem to be consensus about whether this is the right thing to do
    * robots.txt says: "googlebot can't scrape me"; it doesn't say "googlebot can't scrape me for reason X or reason Y"

* Ted:
    * AI preferences will change over time
    * We're struggling with whether preferences should be *complete*. But in reality, we're not going to express a preference for every behavior.

* Glenn
    * Concurs with Ted regarding allowing AI preferences to change and be non-exhaustive
    * Act of publishing content along with policy expresses that they want their content to be used in some way

* Roberta:
    * From side meeting this morning: From the point of view of how we deal with privacy and users' rights, users have a limited choice in practice. 
    * we know that robotx.txt is not enforced

* Victoria:
    * Publishers are not trying to limit accessibility
    * fundamental problem of a top-level category is that we don't know what unanticipated good or bad uses there will be
    * We shouldn't do it if it limits unanticipated good uses
    * Maybe useful for publishers or operators, but users are more important

* Paul: Unaware of any EU law that is relevant here
    * Erin Simon: Not true
        * The EU commission will treat the standards that come out fo this group as binding, if the IETF can demonstrate feasibility
        * Naive to think all we're doing is allowing websites to express preferences
        * It's our responsibility to get this right
        * A standard doesn't have to govern every possible use of a piece of content
        * robots.txt applies to crawlers and not users
        * Do we really need a category that applies to every possible use?
    * Chair: IETF is not the protocol police
    * [Back and fourth among chairs, Pual, and Erin about how EU will be applied.]
    * Erin: We all agree that there are some categories that need not be defined. We may also agree that there are some categories that are actively harmful

* Timid Robot: Argument about cost is compelling--curious about whether adding it back later is possible (when it is more mature)
* Meredith: We're thinking of a tech sophisticated users, but most users are going to use commercially available tools to make the web accessible
* Nate: Defaults are working for incumbents

### Chair summary

* No consensus on top-level.
    * Chairs will ask folks what use cases they have for this category and how else we might address it
* "training" term seems promising
* "search" term seems promising
* "AI output" term needs discussion. Text is more of a distraction than basis for future work.
* **Consensus call on the list**