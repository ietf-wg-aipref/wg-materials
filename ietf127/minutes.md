AI Preferences - IETF 127


## Monday, 16-Nov-26 11:30-12:30

Agenda: https://datatracker.ietf.org/meeting/127/session/aipref/

Chair slides: https://datatracker.ietf.org/meeting/127/materials/slides-127-aipref-chair-slides-00


### Issue #223: Propagation of preferences in PUT
 
Martin Thomson: The current version of the draft doesn't say this anymore
... Far more defensible than the previous text
 
Eric Rescorla (ekr): Not meaningful of what the browser does
 ... I think this is silly
 
Mark Nottingham: Asked if ekr if OK closing the issue.  Yes.
 ... Issue closed
 
### Issue #193: Carrying preferences with stuff
 
Martin: Suggested continuing discussion in the Vocabulary draft
 
### Issue #166: Add non-enforceability provision similar to what is in the Vocab document
 
Jo Levy: Concern that we have the same language in the Vocabulary document as the Attachment document
 
Mark: We've taken the enforcement language out of the Vocabulary document, so we can probably close this
 ... Closed
 
### Issue #103: Should the path in Content-Usage of Robots.txt be part of a structured field?
 
Martin: I'd like to hear from Kevin on this point
 
### New draft posted last week
 
https://datatracker.ietf.org/doc/draft-kelley-aipref-training-preference-signal/
 
Mark: Goal this week is to make sure people understand it and have an opportunity to ask questions about it
... The IETF likes to see early adoption of protocols
... Want to make sure there aren't objections to it

Suresh: We want to talk about the ideas behind the draft

Kevin Kelley: Presented deck Attaching Preferences with cross-vendor policy tokens

https://datatracker.ietf.org/meeting/127/materials/slides-127-aipref-sessa-attaching-preferences-with-cross-vendor-policy-tokens-00

Kevin: Try to get as close to what people expect out of robots.txt
... Eliminate duplication
... robots.txt files are size constrained

Goals:
- Path-specific bindings
- ...

Decomposing the problem
- Defines usage namespace
- __usage_ai-use (namespace, label)

Policy token:
- Label you look for in a user-agent string

A goal: Cross-vendor policy tokens

Kevin described ambiguities and quirks of robots.txt
... Implementations vary

Piece 1 of proposal: Namespaced labels
- Use __namespace_label

Piece 2: The "usage" namespace
- Discussed particular interpretation rules
- Allow opt-in and opt-out
- Paths allowed
- Described reasons for proposing particular behaviours
- 

Would love feedback on PR #260 and draft-kelley-rep-namespaces

Should we define a structured equivalent of robots.txt that we can extend to our hearts' desire?
... JSON syntax

Mark: Whether we adopt this draft, we will consider the issues raised
... I'd like to hear reactions from editors of the Attachments document
... Clarification questions...

Ted Hardie: Using string in user-agent to indicate cross-vendor preferences?

Kevin: In this proposal, no new line types are created

ekr: Referred to the "Deployed parsers complicate things - Here be dragons" slide

Watson Ladd: (Asked clarifying question about user agents)

Alissa Cooper: Understand that proposal desires to integrate with existing parsers
... Replacing robots.txt seems like a bigger effort on everyone's part

Kevin: Gosh, this is really painful
... We may have missed quirks of existing implementation on the Internet

Mark: Our path forward is understanding these issues
... And feedback on PR #260
... Now feedback from the Attachments editors

Martin: I'm not wed to the existing spellings
... Kevin has identified problems
... We want to make sure that when we extend robots.txt, we aren't changing existing behaviours
... New syntax is ignored when not understood
... I was surprised by some of these things - but at the same time, I'm not surprised
... This is how the Internet works
... The empty groups issue concerns me

Mark: It sounds like there is work to do here

Timid Robot Zehta - Creative Commons
... (Withdrew question)

Nick Doty - Center for Democracy and Technology
... Described situations where Google drops clauses

Kevin: Product strings can appear in outbound requests

ekr: Think about the decision tree
- First question: What is the effect of updating robots.txt on existing crawlers
- Are we in a position where it is straightforward to update robots.txt without breaking things ?
- Next: What should the structure of the semantics be?
- I don't want to spend next two years thinking about how work around existing parsers

Will Earp: Trying to coerce user-agent string into something that's not about the user-agent is the wrong thing to do
... Content usage is probably not the right path either

Kevin: I don't like this either to be clear. It's the best of the bad options.
... Once you introduce new MIME types, there are other problems

Watson Ladd: This is a clever signalling thing
... There is cost of humans understanding it
... No, this is not a user agent

Teresa O'Connor - Apple
... I appreciate the analysis of breakage
... We sometimes implement hacks when they solve problems
... This violates the semantics of the user-agent string

Rüdiger Martin - European Commission: This is the right forum for discussing attachments

Mark: Might be useful to have a design team forum for discussing these issues
(Some volunteered)
... Mark asked Kevin to coordinate the design team

Mark: We will have an interim meeting in February
... We hope to have an announcement about this very soon

Mark: We will have a discussion about the Vocabulary on Thursday

## Thursday, 19-Nov-26 11:00-12:30

Mark: Today we're talking about the Vocabulary document


### Issue #217: Use of "synthetic" in AI definitions

Mark: Discussed extensively in London

Martin: If no argument is strongly present in either direction, then the issue is editorial

Mark: A word in the specification should have an effect.  If it doesn't, that's a reason to remove it.

Chris Needham: AI system could produce outputs that are not synthetic.  Inviting us to make a distinction that not's useful.

Mike Bishop: Asked if the right people are here to discuss the issue

Nate Hake: I think the word is very clear.  The definition includes "Made artificially".

Kevin Kelley: We were trying to be evocative of something like Brad Silver's "substantive use"

Timid Robot Zehta - Creative Commons: Having it or not could cause things to be excluded or not in ways that we don't want.  The challenge is finding word to address those things separately.

Paul Keller: Asked on the mailing list for people wanting to keep it to provide definitions.  Having heard nothing, I believe we're trending towards removing it.

Eric Rescorla (ekr): I don't feel strongly about this.  If people can produce examples of where this word helps, we can keep it.  Otherwise, I suggest we drop it.

Pablo González: The opposite of synthetic is natural.  What are examples of generating natural content?  I strongly believe it should be removed because it could draw an useful distinction, causing some generated content to not be regulated.

Mark: If we don't have examples of where the word helps by the next meeting, we'll remove it then.

### Issue #231: De minimis content generation

Mark closed today, per the comment in the issue two weeks about intending to close it.

### Issue #167: Distinguishing access and use

PR #252 is about this.

Mark: My inclination is to go ahead and merge this.

Martin: My observation of this process is that if you say things three times, sometimes they will stick.

erk: This seems fine

Chris Needham: I agree this is fine.

Mark: Editors, please go ahead and merge

### Issue #193: Carrying preferences with stuff

Closed recently

Martin asked to discuss it anyway

Martin: The PR that I just merged closed this
... The text that we already have in the draft that is marked at risk is also relevant here.

Mark: It seems like we need to see these things in situ

Martin: I agree.  I've reopened the issue.
... My preference would be to keep merging things
... I'll avoid closing issues as much as possible

### Issue #245: Concern about redistribution of models

Martin: We just merged #252.
... This is not responsive to the question about carrying things with models
... We already have language in the draft about this, but it's marked "at risk"

Timid Robot: Section 3.3 is the one satisfying #245
... This is marked whether to be included or not

Mark: Should we just close the issue?

Timid Robot: I would be in favor of that.

Martin: We don't have consensus about any of this stuff
... Rather than closing the issue, maybe we can remove the note in the draft

Lila Bailey: Referred to Mark Kelley's presentation yesterday
... My question is whether this will break crawlers that have nothing to do with AI

Mark: We should be careful not to place requirements on other kinds of crawlers on the Internet

Bradley Silver: There is a distinction...  I'm not sure that something needs to be changed.

Jo Levy: It's kind of weird to have an attach in the vocabulary

Martin: The point that Brad seemed to be concerned about is in the 3.4 section.  That was affected by what we merged.

Mark: We'll remove the note

### Issue #246: Address concerns of caching, embeddings and other derived forms

Martin: Now we get to talk about PR #253.  That adds language distinguishing between access and use.
... I'd like to know whether Jo finds this too vague

Farzaneh: Are we talking about the preferences that are embedded in the artifact?

Martin: This is the Common Crawl scenario.  They crawl the Web and put it in a database.
... If the preferences are lost, that's unfortunate

Achim Schlosser: I would add excerpts explicitly
... You should still communicate the preferences

Pedro Ortiz Suarez: I don't think this is the Common Crawl case
... We do do extraction but we always keep the robots.txt file with it.
... This is more concerning to model developers
... This can also lead people to do recrawling
... This can have unintended consequences for Webmasters

Lila Bailey - Internet Archive: In US copyright law, the word "transform" has a very specific meaning
... Maybe use a different word like "derive"

### Issue #249: Does direct provision include URLs

Mark: Talked about this a lot at the London interim

Paul Keller: Somewhat downstream of the larger discussion about the AI Use category
... Substantial discussions about things that it's desirable to include in AI Use
... There are fundamental conflicts that we're unlikely to resolve

Paul presented a table of three possible options:
- AI-Use
- AI-Use+Exclusion
- AI-Use+AI-User-Directed

Paul: Our charter is about the expression of preferences
... It's not about out personal views on what the consequences of these expressions might be

Francesco Marinoni Moretto: As a publisher, the third row is the one I could use, but only if “user-directed” is defined by the access the user already has, not by format (URL versus bytes).

Alissa Cooper: Thanks, Paul

Nate Hake: I think Paul has done us a favor
... I think the third row is the best way forward
... There seems to be a split between people who say we are just expressing preferences and those who feel that we are potentially limiting access
... Some believe we're doing access control
... Content grounding is currently happening
... Tech companies are only paying for content that is not publicly available on the Internet
... This divides up the market
... It raises antitrust concerns
... It keeps small content producers out of the market
... We have to trust communities to decide how to implement preferences
... We have to enable the full spectrum

Alissa Cooper: I believe the best path is in the third row, because we can decompose the problem
... AI Use and AI User Directed can be distinct

Bradley Silver: Focusing on anything that doesn't offer a full spectrum could have the consequence of making choices for the marketplace
... A substantial portion of the value is user directed
... It almost gets to the concept of intent
... Substantial pushback on the concept of a user providing an asset themselves to a model
... Use versus user directed is a difficult divde to draw

Farzaneh: I have consistently objected to bringing in the user and what the user does with an AI
... I have explained how it can hamper access, even if it's voluntary
... It could have the consequence of blocking users from relevant content
... If we have categories about the user, it could impact access

ekr: We've recently been talking about philosophy.  Our job is to craft text.
... A useful place to start would be to look at Martin's text about this

Chris Needham: I think the third row is the way forward
... We need to cover the full range of potential usage
... What kinds of usages fall into those buckets
... The question of what it means to provide a URL to a system versus having the system suggest a URL to you

Timid Robot: +1 to a full spectrum of preferences
... Try to not be prescriptive or too concerned with what you might consider misuse of preferences

Nate: It will be easier to find agreement of where the line should be if it's a place within the full spectrum, rather than the border
... There need to be consent signals
... (Brought up the potential use of extensions)
... Creators are removing their content from the Internet because they don't think AI is working for them

Achim Schlosser: I want to reaffirm that I'm going for the full spectrum

Mark: There seem to be a broad variety of people in favor of exploring the third option

Farzaneh: I would object to having the AI Use category
... Let's have a broader discussion about AI Use

Mark: It's unclear how it will appear in the spec
... If you have comments on the text, please express them

### PR #258: Use Alissa's proposed AI Use definition

Alissa: The point is to have a definition of user-chosen input
... Martin's version includes user-chosen URLs
... I would like to call it system use

Martin: Includes a definition of what directly provided means
... Removes ambiguity
.. The group needs to decide between 1, 2, and 3
... The biggest line is between 1 and 2&3

Mark: Is this text a better alternative than the existing text

Martin: This is much clearer than the previous

Mark: Let's proceed to 


# Second Session : Thursday, 19-Nov-26 11:00-12:30 


Agenda: https://datatracker.ietf.org/meeting/127/session/aipref/

Chair slides: https://datatracker.ietf.org/meeting/127/materials/slides-127-aipref-chair-slides-00

Note-taker: Altanai B

## Agenda for thursday : Vocabulary 

### Issue 127 on use of synthetic in AI definitions

Martin Thompson: redundant words dont do good ...

Chris Needham: preferences should be expressible

Mike Bishop: find historical references from interim

Nate: Artificial vs synthetic

Ken: keep the word synthetic

Timid :  ?

Paul : remove it

depends on the model if it is generating new or reusing natural content

split vote on this issues in general

chairs : group leaning towards removing it, remove it by next meeting

### Issue 231
closed 

### Issue 167: distinguishing access and use

Martin: insists on language clear

### Issue 193

Already closed  with PR 252

Martin: will not preemptively close issues 

### Issue 245

P@ 253 and 252 address this 

Timid: on communicating preferences with trained models 

Martin: remove the note in the draft ... 

Question from Audience: obligation on crawlers that are not AI related, will they break compliance.

chair: cannot control all actors

risk associated 

Bradley: improvements needed 

suggestion to the chairs from audience : Editorial issues 


### Issue 246: Caching concerns, embedding and other concerns

Martin: PR 253 adds the required phrasing for preferences 

minimum common preference 

Martin: Common crawl is what this para is calling out

Achim: maintain pref to downstream use

Jon:..

Pedro: not a common crawl case

Suggestion ( Lila): tranform has a legal meaning in US copyright
use like "derived"

Mark (chair) : "user provided artefacts" 

Paul : have discussion elsewhere first

slides on matrix of conflicting opinions 

Full / limited Spectrum 

All or nothing/ limited/ Selective

Audience more or less agree 

Nate: agrees

Alissa: AI use + AI user directed makes the most sense 

Bradly: subjected to pref

audience suggestion: do not want the access separated like open source developers

Eric: .. ( sorry i missed grabbing the conclusion of this)

chris: 

Timid: Misuse of preferences

Nate : artists and creators have a use case for preference

Chairs : option 3 

Alisa presented a standalone def for user chosen input and URL

Martin: already work on removing ambiguity

chairs : no consensus on URLS

Tess : not believe this is the best approach cites Wikipedia turtle page

Audience : User experience will get bumpy with URLS " did u really mean this ".. 

Eric: directly provided is good

Chris: content should be user visible 

Alissa: introduces a use case of user provided a content but doesn't interact 

### Issues Accessibility 

tbd 

Timid: Supportive

chairs mentioned the Interms are shaping up. Asked audience to look out for them in the mailing list. 


