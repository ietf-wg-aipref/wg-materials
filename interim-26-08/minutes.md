# AI Preferences WG Interim Meeting Minutes

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Monday, 24 August 2026](#monday-24-august-2026)
  - [Attendees](#attendees)
  - [Issue Discussion](#issue-discussion)
    - [AI Training Terminology](#ai-training-terminology)
    - [Break](#break)
    - [Model](#model)
    - [Search](#search)
    - [Context](#context)
- [Tuesday, 25 August 2026](#tuesday-25-august-2026)
  - [New attendees not present Monday](#new-attendees-not-present-monday)
  - [Use - Pre-lunch](#use---pre-lunch)
  - [Use - Post-lunch](#use---post-lunch)
    - [Break](#break-1)
- [Wednesday, 26 August 2026](#wednesday-26-august-2026)
  - [Use, continued](#use-continued)
  - [AI Use (post lunch)](#ai-use-post-lunch)
  - [User/System Split Discussion](#usersystem-split-discussion)
  - [Drawing the line between user and system inference](#drawing-the-line-between-user-and-system-inference)
  - [Extensibility](#extensibility)
  - [Next Steps](#next-steps)
  - [Martin's new text about user/system split](#martins-new-text-about-usersystem-split)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Monday, 24 August 2026

Note-taker: Mike Jones

### Attendees

Mark Nottingham - Co-Chair
Suresh Krishnan - Co-Chair

Cathy Lee - Product Counsel, [Google DeepMind](https://deepmind.google/)
Leonard Rosenthol - [Adobe](https://www.adobe.com/)
August Gweon - [Anthropic](https://www.anthropic.com/)
Kevin Kelley - [Anthropic](https://www.anthropic.com/)
Patrick Wong - [Anthropic](https://www.anthropic.com/)
Chris Needham - [Adobe](https://www.adobe.com/)
Matt Hervey - [Cloudflare](https://www.cloudflare.com/)
Eduardo Jimenez - [Apple](https://apple.com/)
Thom Vaughan - Principal Engineer, [Common Crawl](https://commoncrawl.org/)
Kevin Bankston - [Center for Democracy and Technology](https://cdt.org/)
Timid Robot Zehta - [Creative Commons](https://creativecommons.org/)
Martin Thomson - [Mozilla](https://mozilla.org/) (Vocabulary specification editor)
Paul Keller - [Open Future](https://openfuture.eu/) (Vocabulary specification editor)
Nate Hake - [Travel Lemming](https://travellemming.com/)
Bradley Silver - [Advance](https://www.advance.com/)
Mike Jones - [Self-Issued Consulting](https://self-issued.consulting/)
Erin Simon - Counsel for Search, [Google](https://google.com/)
Krishna Madhavan - [Microsoft](https://microsoft.com/)
Sonia Cooper - [Microsoft <abbr title="Corporate, External, and Legal Affairs">CELA</abbr>](https://microsoft.com/)
Elaine Newton - [Amazon Web Services](https://aws.amazon.com/)
Farzaneh Badiei - [Digital Medusa](https://digitalmedusa.org/)
Sebastian Posth - [Liccium](https://liccium.com/)
Achim Schlosser - [Bertelsmann](https://www.bertelsmann.com/)
Eric Rescorla (ekr) - [Google](https://google.com/)
Alissa Cooper - [Knight-Georgetown Institute](https://kgi.georgetown.edu/)
Max Gendler - [News Corp](https://newscorp.com/)
Glenn Deen - [NBC/Comcast/Universal](https://www.nbcuniversal.com/)
Alex Gibson - [News Corp](https://newscorp.com/)
(behind)
Brendan Quinn [IPTC](https://iptc.org/)
Chris Flammang - [Elsevier](https://www.elsevier.com/)

(remote)
Rony Shalit - Bright Data
Jo Levy
Eyal Gilboa
Priscylla Silva - [IFAL](https://www2.ifal.edu.br/)
Mike Bishop - [Akamai](https://akamai.com/)
Chaerin Lim

(remote - Tuesday / Wednesday)
Paul Farrow - Microsoft AI Product
Caleb Dolandson - Google Copyright Attorney
Malikat Rufai - Meta
Dan York - [Internet Society](https://www.internetsociety.org/)

### Issue Discussion

A number of old issues have been marked `ready to close` -- we intend to close them unless we hear that they still need discussion. 

#### AI Training Terminology

* [Choice of terminology regarding "asset" · Issue #163](https://github.com/ietf-wg-aipref/drafts/issues/163)
* [Use of "synthetic" in AI definitions · Issue #217 ](https://github.com/ietf-wg-aipref/drafts/issues/217)

Choice of terminology "asset"
Well-defined in IETF context - not so much other places

Use of "synthetic" in AI definitions #217

Kevin: Believes "synthetic" is important
... "A model is used to generate synthetic content"
Erin: A perfect example of why search and inference need to be developed together
Bradley: Discussion on substituitive...
Kevin: Attachment happens in the other direction
Bradley: Loophole of "synthetic" could allow substantial training
... Place to have that conversation is at the inference stage
ekr: No information from the crawer to the site about intended use
Alissa: There's a spectrum between search and generative
Timid Robot: We're excluding a group of uses that people can't express a preference on
... I didn't realize how much work "synthetic" was doin
Nate: We need to figure out of this is an issue of wording or if it affects the whole scope of what we're doing
... We have to have a discussion about what is the scope of AI
Mark: We're on the cusp of deciding what the scope of our work is
... Determine what we need to ship versus what we want to ship
Martin: The solution is to throw more words in ... "include this, exclude this"
... It's a very economical definition
... I don't think Chris realized that this was load-bearing at all
Mark: I'm wondering if we can remove "synthetic" and replace it with explanatory text

Paul: ?
Sonia (MSFT): Can we replace "synthetic" with "generative"
Mark: The plan is to replace "synthetic" with explanatory text
... Or make more use of the Terminology section
Timid Robot Zehta - Creative Commons: Our effort is to create categories with meaningful distinctions
... Including preference that are harmful
... The vocabulary would try to be fairly agnostic
... By including "synthetic" or "generative" we seem to be trying to enforce best practices
    Mark: We are not
Timid Robot: Not to make categories that are too broad
Mark: "Generative" seems to be a useful term to have
Paul: This seems to be bringing us back to the very early drafts
Kevin: Definition is intentionally terse
... Trying to describe this without using any of the words that have been shot down is an interesting conversation
Eduardo Jimenez (Apple): New paradigms that we're exposing
... Enumerative set becomes a big challenge
Mark: W3C Privacy Preferences had a very complicated vocabulary and ultimately failed
... Replaced by Global Privacy Controls (GPC)
Nate: A classifier was used against my web site against my preferences
... Concerns that Brad and Chris has raised are legitimate
... In American law, we have the concept of "hearsay"
... Another way of getting to core of whether something is substitutive
... Hopefully it's just a matter of finding words here
Erin: That's a useful question to ask here
... This category is not trying to get at classifiers and ranking
... Is about the creation of a large body of content
... Room for some generation of a label or explaination
... Trust and safety classifier w/ 85% chance of porn
...     Beause I detected these body parts
... We are trying to come up with a usable taxonomy that's simple enough to use
ekr: Kevin's definition say that generic model doesn't generate content even if it could
Cathy (Google DeepMind): A lot of payment processing is about fraud detection
... This group isn't trying to let fraudsters opt out
... We're not trying to do fraud detection
Brendon Quinn (IPTC): We're not trying to legislate for what people are allowed to do if they have a good legal reason to do it - accessibility, CSAM, etc.
... We can't stop people from committing fraud with our preferences
... Equivalent terms already exist in IPTC vocabulary
...    AI ML training - yes/no
...    Generative training - yes/no
... CSAM classification has buckets
... Publishers don't want their content to be used in a substitutive manner
Glenn Deen (Comcast): This conversaion has taken a strange direction
... Today we have mostly content created by humans
... In the future, we'll have hybrid and AI-generated content
... I'd like us to get back to that
... We risk creating categories with too much detail
... The world is always evolving - we can't anticipate future uses
Paul: Where we started this discussion is whether the word "synthetic" is needed/useful
... For that, we need a definition of "content"
... Use some of Erin Simon's suggestion of a de minimis exception to generative output - classifiers, etc.
Leonard: Didn't we agree not to use the word "content"?
Paul: Artifacts and inputs and outputs
Mark: Maybe that's an open question
Martin: We could put more words into the definition of AI Model Training
Mark: Putting more words in the definition doesn't help us
... Having definitions and explanatory text is useful
Erin: I can write an issue about definitions and labels during the break
Chris Needham: Let's use the approprite worlds
ekr: I've heard people say that we need the category "Train AIs that are used to generate new content"
... If people object to that, speak now
Martin: If people want a category for non-generative AI, they need to create a definition
Mark: People need to go have chats and ideally create definitions for Wednesday

#### Break
(20 minute break)

Mark: Go back to issues - https://github.com/ietf-wg-aipref/drafts/issues

#### Model

* [A display-based preferences vocabulary· Issue #149](https://github.com/ietf-wg-aipref/drafts/issues/149)

Krishna: In that issue, we had an AI Training category
... It's OK that you're giving us controls - Can you show them us them in action?
... Very observable and clean
... Formal replacement for grounding
Mark: What the relationship to search be?
Krishna: Current search term - All these controls are available to refine search
... Keeps things similar to what they know in practice
... For search, this is a settled issue - these controls are in use - described in [#149](https://github.com/ietf-wg-aipref/drafts/issues/149)
Mark: This seems like an extension path
... Inclination to contine discussion on "use" and "grounding" and see where it takes us
Krishna: Push to be more transparent with controls
Leonard: My biggest concern is how it's framed - heavy focus on Web crawling / search
... Doesn't get into offline and use cases
... Charter includes offline uses
Suresh: Our charter specifies vocabulary usable online and offline
Farz: I disagree
Leonard: Vocabulary connected to series of attachments
Alissa: I like this as a set of extensions
... Having this our minds as we get into the inference discussion could be useful
Farz: If we read through this, it's not just about search - it's also about training
... When we're discussing AI use, see if we can use the suggested text
... Categories can't be so broad that crawlers can't understand it
... Need to be very clear in preferences when you actually show it to the LMM operator
... To Leonard's concern, our purpose should not be to enable offline use
... This is the *Internet* Engineering Task Force
... If we want to come up with a protocol that's usable offline, we're going behind our scope
Mark: Our scope includes embedded metadata
Farz: If I have an internet shutdown, an offline LMM, and a PDF, do the preferences apply?
Leonard: Yes - they apply no matter where it is
Krisha: I'm OK melding things
... I believe this issue gives way more controls than our current draft
ekr: The issues this issue are raising are exactly the ones we spent the first 1/2 of the meeting dancing around
... I don't see anything in this text that makes it specific to the Web
... The charter is not a command. The charter offers the ability to do things offline.
Mark: Online is a command
Mike: Farz, why do you disagree with having online and offline use cases?
Farz: It could be harmful. If we come up with protocol that is used offline.
... We shouldn't intentionally come up with a protocol for offline use cases.
Mark: We're going to deliver a vocabulary and attachments for robots.txt
... The question is whether we can reuse these for offline use cases
Farz: The argument that we should design for the offline world is not good
Suresh: Generative AI Training has the same pitfalls we have in the draft
Krishna: This is a year old - I haven't updated it
... This was to express things fully
Mark: Right now this is just a status check
Krishna: I still believe that this is relevant
... I agree with Farz that the design is for offline and if it's also usable offline, great
Timid Robot: Express support that is used as broadly as possible
... We sholdn't discard uses that we don't need to
... Providing arbitrary integers in the current draft would be difficult
Chris: There are useful things in the document - Giving control over how the content is used
... I don't think it's a substitue for having a general-purpose inference category
Paul: We have pull requests prepared for this meeting
... I don't hear anybody saying that we should abandon the approach in our draft and replace it with this issue

#### Search

* [Use of the term "non-substantive"· Issue #208](https://github.com/ietf-wg-aipref/drafts/issues/208)

Martin: Search definition makes allowances for accessibility
... Allows to tweak the title to make it fit within the box, etc.
... Do we keep the term "non-substantive" or not?
ekr: If we remove the term, does it change the meaning of the text?
... Does anyone agree with the ability to do machine translation, etc.?
... The purpose of this text is that there are uses that are not in scope of this work
Glenn: My issue is over potential interpretation of what this means
... I don't have a problem with it
Mark: In Toronto and following we had broad agreement on this text
Timid Robot: I want a lablel to bundle with change
... "Non-substantive" is currenly doing this job
... But this label can cause disagrement in its own right
... But I want some other word to put next to "changes" to qualify them
Martin: Is "for purpose of accessibility" such a clause?
Erin: I think we should up-level this to all categories
Paul: We currently only have one category
Mark: We will think about this in discussions of the "use" category
Mark: People have different concepts of what accessibility means
ekr: In the chat, there's discussion about whether the intent is accessibility, then we should craft text using that term
Suresh: Some people have the disability that they can't read long text
... In that case, are AI summaries a disability aid feature?
Leonard: It worries me that we're hiding this under "search"
Timid Robot: I proposed text like this for the entirety of the categories and it received very little support
Glenn: If I produce a piece of content and I publish it in some regions of the world and I produce closed captions
... Does this exception allow people to retranslate the captions and republish the video in territories where it hasn't been released?
Paul: No, it isn't permission to re-release - it's limited to search results
Leonard: It's a preference for translation - not redistribution
Timid Robot: Do you have concerns with transation being an exception for accessibility?
Glenn: If limited to excerpts, I do not have a problem
Martin: "Titles or excerpts"
Kevin: Are you concerned that a bad actor will interpret the preferences to allow them to pirate your video?
Glenn: No, I'm worried about good actors
Mark: It seems like we need people to create proposals for this issue
ekr: I created new text - see https://github.com/ietf-wg-aipref/drafts/issues/208#issuecomment-5396412809
Sebastian: I would phrase it differently to make it clear which qualifiers apply to which case (titles, excerpts, etc.)
Brendon: We've lost that nuance in ekr's rewrite
Mark asked Sonia to add a comment to the issue
Erin: We have tried to avoid the term "summary" because it could be 3 words or paragraphs
... We should have an exception only for de minimus changes
Farz: I am concerned about having an exception. We can't predict the future.
... We should affect accessibility features as little as possible
... We also need to work on the definition so it's not so broad as to be problematic
Erin updated her comment in issue #208 to include "de minimus additions"
Leonard: We're going back and forth improving the "de minimus additions" wording taking into account non-text modalities
Patrick (Anthropic): This feels like a carve-out of a carve-out of a carve-out
Martin: PR time?
ekr: I will create a PR
Nate: Why do we need this now?  The verbatim term isn't in the search definition anymore.
... The purpose of search is to direct people to ???
Erin: I'm concerned: Are people going to perceive translations as summaries
... \#1 I think we would benefit from an accessibility carve-out overall
... The more specific we are, the more careful we need to be
... We could define summaries, then I'd have less concern
... My goal is to define the category such that it doesn't sweep in other lesser things
Achim Schlosser (Bertelsmann): I have a general concern with this type of carve-out, for translations (\[mis]translations can change the meaning of texts and publishers assume legal liability and this is problematic on those grounds)
... This has to be very narrow and clear
... Otherwise, we are assuming legal liability for things
Timid Robot: Is it possible for an original author to be legally liable if someone presents a mis-translation?
Mark: We are not authoritative for this question
ekr created [Try to clean up the text around S 4.2 per WG discussion. by ekr-ietf · Pull Request #232](https://github.com/ietf-wg-aipref/drafts/pull/232)
Martin: A problem is that we don't understand the extent of the accessibility that might be needed
... Therefore, we could rule out needed things without knowing it
... Thankfully, we don't have any need for this text in other sections currently
... When we get to "inference", we might want to use similar text

#### Context

* [Distinguishing Access and Use· Issue #167](https://github.com/ietf-wg-aipref/drafts/issues/167)

Martin: The preference appear to how content us uses - they don't apply to acquisition
... The PR spells out things that should be obvious
Mark: This is largely an editorial task
... I want to be sure people are on board with that
Martin: [Address distinction between access and use by martinthomson · Pull Request #221](https://github.com/ietf-wg-aipref/drafts/pull/221) is for this

* [Introduction: relation to existing laws· Issue #192](https://github.com/ietf-wg-aipref/drafts/issues/192)

Max: Given the updates to 3.2 and 4.1, people haven't engaged in this topic since then
  (See [Update §3.2 Applying Preferences and §4 Vocabulary Definition by TimidRobot · Pull Request #213](https://github.com/ietf-wg-aipref/drafts/pull/213) and [Vocabulary 07 diff from the previous version 06](https://author-tools.ietf.org/iddiff?url2=draft-ietf-aipref-vocab-07))
... Happy to defer to later in our meeting
Mark: Largely separable from the changes to the draft
Suresh: Third bullet in [3.2](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-applying-preferences) most pertinent
Max: This doesn't fully access my concern
... This issue was raised to address language in the Introduction
... This a conversation I want us to keep having
... The issue spells out which text I want to edit
Timid Robot: I would be happy to work with you to create a PR
Mark: There are minor wording changes
... Proposal is to add sentence after "In either case"
Martin: It would be easier to deal with a PR at this point
Erin: There is no need to distinguish between statuatory and common law
... These conflict rules can be dealt with at the attachment phase
... The statement "Without prejudice to existing law" does the job
... The consensus on [3.2](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-applying-preferences) is very hard-fought and I would like to not disturbe it
Brad: A clear statement about hierarchy as far as preferences go is important
... Nothing here is intended to overwrite existing contractual language
Sebastian: [5.2](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-more-specific-instructions) of the vocabulary expresses this
Paul: The language in [5.2](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-more-specific-instructions) is clearer. We can't clarify their intent by putting something in this document.
Max: Agreements may be private. What's the harm of allowing them to have intent?
Paul: You don't know the intent of the preferences
Erin: [5.2](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-more-specific-instructions) is a great place to have discussions about conflict resolution
... For instance, contract terms may override preferences
... It's not a good idea to put it in [3.2](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-applying-preferences) now
Timid Robot: Trying to rehash the intracies of [3.2](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-applying-preferences) and [5.2](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-more-specific-instructions) in the [Introduction](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-introduction) is causing problems
ekr: Next steps are to update the text in [5.2](https://www.ietf.org/archive/id/draft-ietf-aipref-vocab-07.html#name-more-specific-instructions)
Mark: I am reluctant to wordsmith things here

Mark: That's all the vocabulary issues we have queued to discuss other than the Use ones

Leonard: I filed a new issue today - [Examplar vocab section contains material that is general purpose · Issue #226](https://github.com/ietf-wg-aipref/drafts/issues/226)
Mark: This seems editorial
Leonard: This makes some language more general-purpose than it is today


## Tuesday, 25 August 2026

Note-taker: Mike Jones (with assistance by Timid Robot Zehta)

### New attendees not present Monday

(remote)
Paul Farrow - Microsoft AI Product
Caleb Dolandson - Google Copyright Attorney
Malikat Rufai - Meta
Dan York - Internet Society


### Use - Pre-lunch

* See the [Use Proposals Wiki](https://github.com/ietf-wg-aipref/drafts/wiki/Use-Proposals)

Nate: advocate for inclusion of use category(ies)
... Inference is where the value is
... Opportunity to allow an expresssion of preference that would be useful
... We've done a lot of the work already by what we've done in the Training definition
... Cover the substatutive uses
ekr: Once a model is trained, the user types into it to obtain something
... The topic at hand is the provision of externally visible data as part of the inference model
Leonard: Discussiong inference time versus training time and access vs use ([Address distinction between access and use by martinthomson · Pull Request #221](https://github.com/ietf-wg-aipref/drafts/pull/221))
(Discussion about the term "asset" by Paul, Krishna)
Paul: The draft needs to make sense to people not in this room
Nate: I had updated my PR with the "learned parameters" wording ([Add "AI System Inference" and "AI User Input" categories by natehake · Pull Request #216](https://github.com/ietf-wg-aipref/drafts/pull/216))
Timid Robot: Discussion on impact of our definitions and preferences - including impacts to people w/ disabilities
Alissa: We need the ability to say "no" - for instance, matching Nate's preferences - and the ability to say "yes" to particular kinds of inference
Farz: Inference is very broad
Timid Robot: I don't think we have the will to create many refinements of categories
... The alternative is to propose a top-level refinement - but there didn't appear to be an appetite for that approach
... The other alternative is to make it possible for people to create their own refinements
... Meets the need of different stakeholders
Glenn: Publishers are going to need categories to meet their needs
... The space is going to continue evolving
... Likewise, the AI consuming the requirements will also continue evolving
... I'm aligned on the point that extensibility is critical
Nate: We need to be thoughtful in our definition of "Generative AI"
... Nearly everything is output. Even a classifier generates "yes/no".
Paul: Consider that people may want security by not inference
... Scope that language as closely as possible to generative - an addition to 3.2
... 3.2 is currently defined to be flexible (and is not bullet-proof)
Caleb: I'm thinking about a model that improves itself
... If the model has to track preferences for the different pieces it assembles, things get complicated
Timid Robot: There are already very well documented AI harms in the world
... I like being able to differentiate between structural differences versus details and specific carve-outs
... Push work out until we have functional categories
... 3.2 is both insufficient and as good as this group of stakeholders is going to get
... Creative Commons would love to be able to recommend a sequence of preferences
Brad: Training is massively broad. Training and inference are closely related.
... One harm is that there are parts of the world that don't have local news anymore
... There are going to be lots of examples of hypothetical harms
... It begins to sound like we're creating DRM - even though we're not
... We shouldn't let that stop us from reaching consensus
... Publishers are in the business of communicating the work to the public. AI models are part of that value chain.
... We're not going to be able to come up with bullet-proof exceptions
Glenn: As a publisher, I'm not here because I want to say "no" to everything
... Publishers may want to say "yes" in the same way
... Our mission is not to create an enforced mandatory "yes" for AI
... The examples are are citing in our discussions are from the last war - the Internet
Chris Needham: There are AI-related harms such as misrepresentation of journalistic output
... We don't want our work to be to the detriment of people creating content
... I suggest that we focus on the technical definitions
Martin: There's difficulty differntiating between what we call "inference" and what we call "grounding"
... The intent behind the definition is grounding 
Mike: Asked Timid Robot to describe what he means by "structural differences"
Timid Robot: System directed versus user-directed is a structural difference
... Accessibility carve-out is structural
Mike: Pointed out to Martin that neither "inference" nor "grounding" appear in the vocabulary document
Martin: PR #216 proposes to add them

Mark: I propose that a small group go off and create a concrete proposal
... Along the lines we've been discussing for inference/grounding that has a chance of gaining consensus
... It's effectively a design team. It's output has no more standing that anyone else's input in the working group.
... Come back at 1:30pm

### Use - Post-lunch

* See the [Use Proposals Wiki](https://github.com/ietf-wg-aipref/drafts/wiki/Use-Proposals)
  * [Design Team Output](https://github.com/ietf-wg-aipref/drafts/wiki/Use-Proposals#design-team-output)

Martin: We don't have a name for the thing
... It's important to first focus on what the thing is
... The use of an asset is input to a model
... It's important to focus on the distinction between the capabilities of the model and way that it's used
... Focus on the ephemerality of the process - requesting a result - as well as the explicit exclusion of training
Mark: This is a proposal for a single vocabulary term
... What qualifies as a request?
ekr: Concerned about the use of stuff for vulnerability or malware research would be bad if the nasty code "opted out" of this category
Kevin: We know what we want to talk about and had terminology requests
... Focusing on the ephemerality of the input that is discarded after the requests
Martin: The concern is that this will sweep in some use cases that people care about
... Vulnerability research, general research, accessibility
... We're going to have to work on the boundaries of it
... Intent to capture the generative systems that people are using - not just categorization with yes/no answers
Timid Robot: I'm curious if you considered putting "ephemeral" in the definition such as "ephemeral use" or "emphemeral process"
?: "No"
Cathy: Are we setting aside the difference between autonomous fetching of the model for grounding purposes versus the user providing content?
Mark: Yes, temporarily
ekr: We want to test the text against people's intuition of where things they care about fall inside and outside the line
ekr via chat: There are two concerns here: (1) the one raised by Cathy about trust and safety and (2) a potentially broader one about what I would call "non-competitive" applications where what you are producing is very qualitatively different from the input. An example of (1) is adult content detection. An example of (2) is vulnerability research. The conceptual difference here is that (1) might just emit some sort of rating or score, but (2) emits a lot of content, such as an attack trace
... Though I think there is a spectrum of these.
Mark: Any other reactions?
Mike: I think this a good synthesis of what we've been talking about for some time
... I like ekr's suggestion to test the text about particular examples and where they fall inside or outside the line, and then refine accordingly
Suresh: That's the point of the use case document - for people to record these examples for us to test
Martin: At this point we're trying to assemble a set of tests to determine where they fall
Glenn: Timid Robot had the term "public interest"
... I'm concerned that this group may be trying to determine what's in the public interest
Alissa: We're assuming there will be a preference for all generative uses
Nate: I don't know how random Web site operators will understand this
Kevin: There are lots of sites that block ClaudeBot but want to allow users using Claude
... Caching is completely beside the point
Brendan: Journalists often look at questionable content (leaks, etc.) because it's in the public interest
... The legal system sanctions this
... We could say the minimum amount possible about it in our document
Timid Robot: We are not doing public interest carve-outs. We leave that to legislative work.
Glenn: We don't put in statements about the public interest
Timid Robot: Put a notice in that we are not putting it in
Erin: We need to build a system that works
... Categories that everyone opts out of doesn't help anything
... I'm concerned about us copping out saying "Let the legal system sort it out"
... We should do something that's useful in its own right
Alissa: Used the term "training adjacent"
... Distinction between altering the system as a whole versus altering the output for a particular user
Farz: Carve-outs don't remedy the situation if our definitions are not precise
... We have a document on impact on the end-user
... In Toronto, Meredith Jacobs talked about the impact on research
... I think carve-outs are good but they're not enough
Timid Robot: I think we are continuing to be too specific
... We're talking about very detailed specific patters that will be different for each category of stakeholder
... We can shift out thinking that the categories we're defining serve as carve-out containers (categories as scaffolding, foundation, etc.)
Paul: We are reaching the point where we can consider the impacts of our categories
... They look like a viable candidate for the overall architecture
... We may need to discuss distinction between user-initiated and autonomous inference
Nate: This may get us there
Mark: We're not a point where we close off any of the definitions yet
... But having a set of definitions to work from is good
Timid Robot: Distinction between "alter the system" and "alter the output" useful (said by Alissa)

Mark: Maybe focus rest of our time today on getting the terms clear without focusing on the impact
... Then tomorrow look at the impact
... Meaningful step forward on how we use that time
ekr: "Origin of the asset" discussions important (for tomorrow)
Mark: Tomorrow 1/4 of time on impact, then 1/4 on system
Mark: Talk about synthetic phrasing in AI training today
Leonard: I would prefer that we not do this in a small group
Paul: Perhaps the editors and interested can try to create a proposal as a starting point
... 1/2 hour should be enough

#### Break
(30 minute break)

Martin: Reported on work occurring during the breakout
... [More explanation on the generative aspect by martinthomson · Pull Request #235](https://github.com/ietf-wg-aipref/drafts/pull/235)
... Retains "that is used"
... Simplifies "AI Model Training"
... Models can have multiple purposes, some of which may be non-generative
... Those are not subject to this category
... Classifiers, rankers, etc.
... Decided not to do anything with "training adjacent" discussion
... These are general software engineering practices being performance by businesses, etc.
... If inference is used in those processes, it may make these processes more difficult
... [Restore "make available for use" in generative defintion by martinthomson · Pull Request #236](https://github.com/ietf-wg-aipref/drafts/pull/236/changes)
... Modifies the definition to add subclause "or made available for use"
Mark: What about "as available as a request"
Martin: We didn't deal with that
Mark: Would it be useful to incorporate the design team output into the editor's draft so people can see it in situ?
Martin: I can work on refining the wording and then we can do that
... (approved a change suggestion with the comment "Timid Robot is excellent")
Elaine: ISO document contains defintion for generative AI (looking for document/reference) to be considered or compared
Mark: Merging gives us an integrated editors' draft (on a branch) to work from tomorrow
... Evaluate it against the issues we have open
Martin: Observed that the definitions are not great and that people in different domains tend to create their own
Chaerin Lim via the chat: https://www.iso.org/obp/ui#iso:std:iso-iec:22989:dis:ed-1:v1:amd:1:v1:en
... AI system (3.1.4) based on techniques and models (3.1.23) that aim to generate new content
Note 1 to entry: Examples of generated content can include text, audio, code, video, and image.
Note 2 to entry: Generated content encompasses new information or new ways to express pre-existing information. That pre-existing information can be drawn from the input, a dataset involved in building the model or an external repository.
Brad: We're starting from the supposition that everyone understands what "synthetic" means
... We're actually creating more ambiguity
... The solution we're creating is a bigger problem than the problem we're trying to solve
Timid Robot: This undermines the category
("this" being "The training of models that are used to perform exclusively non-generative tasks, like ranking or classification, are not included in this category, even if the model is capable of generative tasks.")
ekr: I thought this text wasn't a substantive change to what we already have
... Is it a preference for not making it available in a generative model?
Paul: Common Crawl always passes the preference for the content along with the content
Thom: Common Crawl has committed to doing that
... It might be useful to have a list of the problems and harms that people have identified distinct from the use cases
Mark: It sounds like you're signing up for work :-)
Thom: We can then ask "What is the semantic distinction necessary to express this?"
... Does the vocabulary we're writing address this?  If not, then let's do.
Chris Needham: Hearing Brad explain his reluctance to this category resonates with me
... I feel this is a regression over the current text, which doesn't have this exception
... We should 


## Wednesday, 26 August 2026

Note-taker: Mike Jones (with assistance by Timid Robot Zehta)

### Use, continued

`dt-plus` branch with changes from yesterday for review today:
Rendered: [https://ietf-wg-aipref.github.io/drafts/dt-plus/draft-ietf-aipref-vocab.html](https://ietf-wg-aipref.github.io/drafts/dt-plus/draft-ietf-aipref-vocab.html)
As a diff: [https://github.com/ietf-wg-aipref/drafts/compare/dt-plus](https://github.com/ietf-wg-aipref/drafts/compare/dt-plus)

ekr: Previously a definition of AI Training in definitions and then in normative text
... Now definition of user vs autonomous/system occurs nowhere
(voices) user vs autonomous/system remains an open question that will follow this discussion

Discuss: `[, or made available for use,]` in Generative AI model definition
ekr: I continue to have the same object as I did yesterday
... Consequence is to make open weight models extremely difficult to deploy
... Responsibility to carry preferences with content
Kevin: The person assembling the model respects the preferences when including the preferences as metadata
... Each party can only be responsible for their own behavior
Paul: ekr's analysis of the language is correct
... If you train your own model, we assume that you act responsibly
Glenn: I think we're digging ourselves into a hole
... But we're not here to write regulation
... Simplify text to "Generative AI is..." - drop text about "is used" and "made available for use"
Suresh: If we use "make use of" we need text about that
Mike: Eric, what it is about open weight models that could make them difficult to distribute?
ekr: In a closed model, the harness can forbid particular uses - for instance, it can restrict the output to numbers
... In an open weight model, anything can be done
Nate: wants text to stay, seems aligned with goal of AI preferences
Timid Robot: I like Glenn's suggestion to remove words about "use" (replace beginning of definition with "An AI model that generates synthetic content")
... This puts the relevant information in a better place (better place: [Add model context documentation requirement by TimidRobot · Pull Request #239](https://github.com/ietf-wg-aipref/drafts/pull/239))
... We're not writing regulations.  What we're trying to do here is *communicate* preferences.
... Everyone has to decide whether to follow the preferences (open models are not prohibited)
... Both Search and AI Training are responsible for maintaining the preferences
... (They wrote that in [#239](https://github.com/ietf-wg-aipref/drafts/pull/239))
Chris Needham: Is in favor of dropping use language
... Wants to keep the qualifier "[This does not include classification, ranking, or scoring, or the generation of brief explanations of the outputs of those operations.]"
ekr: There's a narrow question about whether it's acceptable to train a model for classification on text with the preference "AI Training: No" if it's also usable for other purposes
Discussing text in #239: "If a model is trained under a search allowence preference, that context must be documented alongside the model."
ekr in favor of this along with keeping the bracketed text
Erin: Not in favor of changing the definition to a use case-based one
... Not appropriate to make prescriptive declarations to model builders
Martin: We seem to be resolving on something
... PR #241 my attempt to do the same thing as #239
Leonard: There are three other PRs that would go well with Martin's
... Maybe we can break out and work on combining them
Martin: It's important to retain that the preferences are carried with the model
... for subsequent uses
Matt: Do open weight models in practice require more restrictions because they are more general purpose?
... Merely repeating preferences alongside a model is in practice, insufficient, because there are many more actors
... increasing the probability of not respecting the preferences
Timid Robot: I retract my support for removing the bracketed text
... I was not aware of how it was modifying the meaning
... This is implicit in the Search term but it's worth being explicit and even potentially redundant
... I disagree that publishing the preferences with the model is insufficient
Chris N: It's not clear to me that a capability-based definition isn't possible here
... There are complexities involved in carrying the preferences along with the model
ekr: I'm in favor of Martin's text
... We spent a tremendous amount of time creating the text so we should muck with it as little as possible
Kevin: Making this more general doesn't both me
... This might be the only term where it seems relevant at the moment, but that may not stay true as the vocabulary grows
Martin: The majority of open-weight models are built for generative purposes
... Therefore, if people are to respect preferences, they won't feed "Train AI: No" content into them
Alissa via the chat: "And this is my re-write of what I think MT's text is trying to say:
Although models can be trained to be able to perform non-generative tasks by using assets that have indicated preferences to not be used in training, such models ought not be adapted to enable any generative capacity. An entity that distributes such a model is expected to communicate a preference to potential users of the model that the model not be used for generative purposes."
Nate: Distributing preferences with the model is impractical. There are too many parties who would have to respect them.
... If we say don't train an AI model with an asset, then don't train it with that asset.
... This exception could pull the rug out from under the whole thing.
Mark: We don't want to make it difficult to distribute models intended for non-generative uses.
Kevin: Here's a real-world example: OpenAI released a PII classification model
... But it is still generative
Timid Robot: The fundamental problem is that there's no such thing as non-generative AI
... If a content owner is concerned, they might say "no" to training
... To address your concern, Nate, we might need another category with no carve-outs
Nate: We're operating in such a low-trust environment, we need definitions that are clear and broad
Erin: I think there are better ways to do it than embed it in the category
Erin via the chat: ""compliance with this preference entails conveying the preferences associated with the training data of a model along with that model" is a little less YOU MUST DO THIS"
Erin: There are cases where people have a legal right to use content irrespective of preferences
... For instance, university researchers
... We shouldn't be in the business of prohibiting distributing models enabling exercising that legal right

(morning break)

Mark: Before the break, we were going back and forth about the parenthetical text
... It doesn't seem like we're going to converge in this meeting. We have other things to discuss.
... I plan to remove the bracketed text and have ekr create an issue about his concerns
Timid Robot: ekr, are your concerns the same as those of publishers?
ekr: My concerns are probably not the same as those of publishers
Paul: Suggested a text change - summarized in Martin's [PR #244](https://github.com/ietf-wg-aipref/drafts/pull/244)
... Make qualifier for generative use part of "making available"
Erin: The purpose of the text is to distinguish between generative models and all models
... We are not trying for iron-clad enforcement
Chris: The intent of the person releasing the model doesn't constrain how they will be used downstream
Nate: It's the act of making it available that the preference applies to
Mark: There may be enough support for #244](https://github.com/ietf-wg-aipref/drafts/pull/244) text on "Generative AI model" definition to move forward with it
Timid Robot: That text is better than what we have
Martin: I'm going to merge this text into the branch

Discussion of `[This does not include classification, ranking, or scoring, or the generation of brief explanations of the outputs of those operations.]`
...
Timid Robot: in thinking about the examples that have been provide 1) cancer classification with generative rationale provided and 2) movie classification with generative rationale provided, with assumption that 1) is good and 2) is bad, i don't think we can draw a line between them here
... the question is are we ok with shipping a definition that contains that conflict or do we need additional complexity in the vocabulary document (i.e. a new training category)
*(continued wordsmithing)*
(support for the word "rationale" instead of "explanation")

*(wordsmithing moved on from "AI Model Training" definition to "AI Use" definition)*
Discussion of `[as the result of a request]`
Timid Robot: I find the AI Use definition text in brackets confusing. I'd rather we elaborate more as we did in the Search definition.
(multiple people expressed concern about needing scope of use be defined to inform this discussion)
Leonard: context of this definition in small group included concept of emphimerality
Nate: The text "[as a result of a request]" is a non-starter
... People sell content to third parties to use as reference material
... Some small publishers don't know this is happening
... This is why it's necessary to have a broad use category
Alissa: This definition now references the Generative AI definition, therefore it is more limited
ekr: I would still like to see people create examples to test for whether they're in or out
Nate: The big crawlers don't advertize their scrapers under expected names
... They don't know to block Vertex AI (a Google Cloud platform)

Mark: After lunch, I want us to talk about
1. User/system split that Farz was referring to
2. Extensions to the vocabulary
3. Return to exceptions and how we phrase them
4. Wrap up the day with a next steps discussion

(lunch break)


### AI Use (post lunch)

Kevin: Kevin and Nate and Erin worked on AI Use text over lunch
... `[as the result of a request]` is misleading
... Replace with "for the purpose of generating synthetic content"
Erin: Other suggestion is to not try to define time period of use
... Instead just a declarative statement about "used to generate synthetic content"


### User/System Split Discussion

Mark: Three possible options:
1. one combined category \(a)
2. two categories (user and system) \(b) + \(c)
3. only system category \(c)

... Options 2) and 3) require defining where the split is

Martin drew boxes on the whiteboard
(a) AI Use
  \(b) User
  \(c) System
    Asset selected by the system
    
... (b) could be out of scope

Leonard: We allow users to not to have their assets used for purposes of inference
... Adobe respects this in Photoshop, Lightroom
... I'm OK with this being in an extension
... Users can override the preference after being warned
Timid Robot: I like User stuff being in scope somehow
... If I as a user supply a URL, I'm not necessarily visiting that URL
... Concerns about a System providing a thing don't go away just because the User is supplying the URL
Brad: I agree with what Timid Robot said
... There's a lot of difficulty on where to draw that line
... We're moving towards more blurriness - not less
... Consider opportunities to use the Website in a way that gives the publisher benefits
... For instance, advertizing, subscription opportunities, etc.
Farz: We are putting people in the position of deciding whether to follow preferences or not
... Example: Medical PDF that they want AI to translate
... System could refuse to do the action because it's against the preferences
... We need to not take away people's power
Paul: I'm with Nate on splitting this
Mark: So I hear you recommending System only plus extensions
Paul: Yes
Erin: I don't think this charter is about restricting user's ability to utlize content they already have
... The photocopier and VCR were also challenged in their day but their use became normalized
... I agree that there's a line-drawing problem but that's not a reason to not draw the line
Alissa: I'm in favor of 3
... I think drawing the line is too hard
Leonard: If a company purchases the rights to an asset, does that make it equivalent to User use?
Timid Robot: A user-directed inference could be good - not a reason to throw the whole thing out
... UX is going to play a huge rule in user-directed inference. We can't argue for/against categories based on assumptions about the UX.
Elaine: I lean towards \(c)
ekr: I don't think it's that hard to draw the line
Brad: Often a user doesn't "have" an asset.  It's often the case that the user has access to it somewhere on the Web.
... There are many legal contexts that differ by jurisdictions
... We should try to not oversimplify it because it's actually complicated in practice
... I feel like splitting it is out of reach
Mark: I'm hearing a lot of interest in trying to draw the line
Erin: This is about what users are able to do with content they have and tools they have
... Categories could end up overbroad and interfering with legitimate user actions
Farz: We should focus on the System AI
Timid Robot: I agree that there will be instance where a n all-inclusive inference or user-directed preference will be bad for end-users
... That doesn't mean that we should throw out the preference
... This is not DRM. The goal is to communicate the preferences.
Mark: It seems that a productive use of our time this afternoon would be to try to draw the line
Sebastian: Restricing user's use of content is already happening
Mark: ekr favors \(c) plus extensions

### Drawing the line between user and system inference

Mark cited https://github.com/ietf-wg-aipref/drafts/wiki/Use-Proposals#ai-grounding, specifically "where the asset is not directly provided by the client"
Mark: Is this a reasonable place to draw the line?
Brad: It is vastly different to fetch a URL versus providing the URL to an AI
... User-directed actions related to crawling are often not respecting robots.txt today
Nate: How would extensions work?
Mark: If we enable extensions, there would be a registry with our definitions and rules for others to add entries
... There would be rules about how categories relate to one another
... Currently we have no registry.  A new RFC would be needed to add categories today.
(back to original discussion)
Leonard: regarding "where the asset is not directly provided by the client" is fine, but more work will be required to clarify
Paul: I believe that direct vs. indirect is totally meaningless
... If I have access to content, I'll find a way to get it into the system
Brad: I don't think it's helpful to say "People will circumvent so why bother"
ekr: Seems to be support for line between user-provided and system-provided
... We're arguing about by-reference or by-value but that's a relatively narrow point
... We're looking for a viable way forward overall
... Maybe talk about extensions now
Eduardo: There may be cases where things are being done on behalf of a user but without a crawler in between
... These things should be OK
Achim: Change "clients" to "users"

(afternoon break)

### Extensibility

Mark: IETF working groups often accomidate protocol evolution via extensibility points
... For instance, defining a new vocabulary term
... IETF registries maintained by IANA - see iana.org
... Registries come with instructions
... Spectrum between first-come-first-served and RFC-required
... We're currently effectively at RFC-required
... Some middle points allow other standards organizations to also create registry entries
... A registry would be a pressure relief value in our process
... "Specification required" policy has several variants
... Designated experts validate that the registration policies are followed
... Registry guidelines are defined at https://www.rfc-editor.org/info/rfc8126/
... Mark is proposing a "standards required" pattern in IANAbis allowing other standards orgs to create entries
    https://datatracker.ietf.org/doc/html/draft-nottingham-ianabis-spec-reqd-03
Martin: A point of the registry is to have the same code point mean the same thing to everyone
... Tension between setting the bar too high and too low
... Want to avoid off-the-books use of code points
Glenn: IETF standards are open for everyone to read and implement
... IANA registries help facilitate interoperability
... The IETF doesn't prevent people from branching our specifications
Suresh: "We are not the Internet police"
Timid Robot: Created a draft a while back about exclusions to preferences
... Would like to be able to register a new category
... Even though we're saying "no" to generative AI training, there are some instances where we want to say "yes"
... Creative Commons could advocate for this extension category
ekr: Protocol has to be defined in a way that the extension points function
Timid Robot: I'd like to be able to define exceptions that work across attachments modalities
Mark: (1) what are the extension points, (2) what are the rules for them, (3) what constraints to put on them
Martin: Described difference between must-understand and must-ignore extension mechanisms
Kevin: Yes, we can't predict the future
... On the other hand, we need to be very clear about what conformance means
Sebastian: How regulators can understand conformance matters
Mark: We already have this problem because our attachment mechanisms are extensible
Glenn: Other SDOs do publish conformance suites - the IETF doesn't
Suresh: Some extensions are mandatory to implement
Mike: Some IANA registries include status/recommendations fields with values like Required, Optional, Recommended
Mark: And what to put in those fields is never contentious ;-)
Martin: I can imagine products advertising which preferences they implement and respect
Elaine: This is a base standard.  There are already companies with their own non-standard categories.
... Some may be optional
... There are no MUSTS right now
Mark: RFC 2119 keywords targetted towards interoperability
... We have shied away from that because of how many caveats there are in this space
Elaine: We would like a standard that makes it clear what it means to conform to the standard
Martin: Would be be helpful to talk about in the document what it means to conform to the document?
... Such as what vocabulary terms you understand
... And describing what you will do with those terms
Erin: Mandating transparency about compliance is going too far
... But describing what compliance means is reasonable
Mark: The next steps for this are for those interested in extensibility to create a proposal
Mike: I'm willing to volunteer for this subcommittee

### Next Steps

Mark: We've discussed substantive text changes this week
... Get that out to those who weren't in the room and have people review it
... I suggest we update the draft with the caveats on where there may not yet be consensus
... Request a more substantial time block in the IETF 127 meeting in San Francisco in November
... October interim didn't appear to work
... Do schedule multiple virtual interim meetings
... Do consensus calls
... Future in-person interims wouldn't have until January or February
Leonard: We have 18 open PRs
... Do we have a process for merging or closing them?
Mark: That's up to the editors
... There's a clean-up process after each of these meetings
ekr: I'm not fully conformatable with our current AI Use text
Suresh: There are lot of moving parts. We need to enable people not in the room to put the pieces together.
Mark: I want to give you concrete text to file issues against
Elaine: What will we cover in San Francisco?
Mark: We'll cover what the open issues are at the time
... We'll also try to communicate to the rest of the IETF where we are
Mark: We're getting close to being able to say that we've met our initial charter goals
... I'm hearing from many people that it's important to ship something from this working group

### Martin's new text about user/system split

Martin via the chat: "Use of an asset as input to a generative AI model,
where the asset is not directly provided by the user\[,
either as a URL or by supplying the asset itself\].
 
<!-- Choose either the above or the below. -->
 
\[If a system that needs to perform inference
in order to determine which asset to use,
that does not qualify as a user directly providing the asset.\]"

Timid Robot: I like the second choice.  But I don't know how it relates to the first choice.
... First lines make it seem that this is about system-directed inference
Martin: Yes, that's what we're talking about

Brad: I thought we got away from using URLs
Erin: What's the difference between going to a Website and having your AI use the Website?
Brad: I explained earlier that a user going to a Website as it was intented is different than an AI using

Brad: I still think there should be another category about the User piece but that's separable from this
Martin: A tool refusing to fetch a URL is just being inconvenient
Glenn: I hate the second language option
Timid Robot: Speed bumps are OK
... It matters who fetches the content
... If the user loads the content, it may move liability to the user
... The second option moves things from User to System
Paul: The category we're descibing is AI System Use
... This is the outcome you want
Nate: This works for me only if there's still the option to express preferences about the User
... This works in world (2) - not in world (3)
ekr: It seems like we have a clear lack of agreement on the URL point
... The questions of agentic browsers are not particularly apropos
... If the browser fetches content, all the indicators will be stripped anyway
Erin: Speed bumps need to serve a purpose
... There's no usefulness to forcing a user to download and re-upload content

Mark: I think it would be useful to put links to issues in the text to help direct conversations
Martin: The editors would guidance on which issues are worth calling out
Mark: We're looking to kick the ball down the road

Mark: Thank you to Adobe!
... It's been somewhat productive
