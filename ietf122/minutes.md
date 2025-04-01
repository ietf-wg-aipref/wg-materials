# AIPREF Working Group - IETF 122

*13:00 - 14:30 Thursday Session II - Chitlada 1*

Chairs: Suresh Krishnan, Mark Nottingham (absent); Tommy Pauly filling in

Slides: https://datatracker.ietf.org/meeting/122/materials/slides-122-aipref-chair-slides-00.pdf

Notes: Tommy Pauly, Brian Trammell, Jaime Jiménez 


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Questions for the Group](#questions-for-the-group)
  - [Vocabulary](#vocabulary)
  - [Attachment by location](#attachment-by-location)
  - [Opt-In/Out](#opt-inout)
  - [Attachment mechanisms](#attachment-mechanisms)
  - [Combining Preferences](#combining-preferences)
  - [Licensing Schemes](#licensing-schemes)
  - [Matters for Policymakers](#matters-for-policymakers)
- [Candidate Drafts](#candidate-drafts)
- [Open Mic](#open-mic)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


## Questions for the Group

Jonathan Hoyland commented about authentication and authorization being out of scope, and that being potentially an issue.

David Schinazi said that can happen elsewhere, and we can assume that will be done elsewhere or later.

Mirja Kühlewind disagreed with Jonathan; Lucas Pardue echoed Mirja: lots of examples of cases where trust is defined separately from hints (such as HTTP). Don't want to relitigate the charter.

Martin Thomson points out that the content is at least as public as the content itself. Assertions are therefore equally public. Access control might be a technical enforcement strategy, but that's an orthogonal problem and solution space.

### Vocabulary

Suresh requests input from the group on the proposal that we leave the vocabulary scope simple, based on workshop output.

Glenn Deen asks whether we've decided on opt-in/opt-out? Martin Thomson agrees we should take some time to discuss that. 

Martin Thomson points out the principle of a simple vocabulary scope is a very good one, largely because we need to deliver something soon.

Alissa is concerned about the slide text about vocab being "relatively" simple; hard to discuss this in the abstract, but flagging that we need to be careful about what we think of as simple.

Suresh says that if it isn't something we agree easily is "simple", then it's not simple.

Alissa agrees this makes sense in principle, but "the simplest set" is not commonly understood. For instance, the search/AI distinction is a spectrum. Noncommercial/commercial is another axis which is very important to some and not to others. It'll be easier once we get into details.

Mirja points out that there are two sides; a side expressing the preference, and another side trying to consume the preference. We should have preferences that are possible to act on and make a difference in behavior and outcome. There are different entities that perform crawling, use the data, etc.

Glenn points out that there are many people joining this conversation who aren't often in the IETF process, and we should make sure we have a good way to ensure they are included.


### Attachment by location

Gary Illyes has concerns. robots.txt is not enough on its own. Large media sites will have millions of specific URLs, etc. 

Martin Thomson points out that it *is* where all the bots are already looking. I don't like it, for a number of reasons. Gary's point is spot on: it doesn't scale. You might also not want it to. This argues for HTTP headers.

J-F Quéralt notes that if most of the industry is looking at a particular file, could we use robots.txt as a bypass/redirect? (web linking like)

Martin agrees it is possible, but questions if it will have an advantage to do so.

### Opt-In/Out

Glenn talks about lessons learned from defining previous grammars; opting in and opting out are difficult to make consistent.

Martin waves his hand, indicating ease.

David Schinazi (not an AI enthusiast): to me opt-in means if you do nothing, the result is "no", opt-out means if you do nothing, the result is "yes". what does both even mean?

Martin says this is straightforward. You have three states (there will always be cases that don't express a preference). But depending on which set of rules you have, the intersection with laws etc, is the harder part (how to interpret the lack of signal). The preference expression is relatively easy.

Richard Barnes points out this is not a dichotomy. Suresh asks whether we have to specify what to do in the absence of a signal. Can we assume a default model? Richard says the default has to be the current status quo. 

David says we can think of this as allowlist and denylist, versus opt-in/opt-out.

Glenn says we don't have anything today as a baseline; Suresh points out that there is a current status quo of behavior that is the baseline.

Alissa suggests we write down what Richard was saying; that we are not changing the definition of the default status quo, but instead only allowing a preference to be explicitly expressed. We have no ability to change the meaning of not expressing preferences.

Richard says that opt-in and opt-out imply a particular state of the default, which is wrong — the default is unknowable.

Suresh names this Richard Barnes' Uncertainty Principle. 

Gary Illyes (unenthusiastic): The internet has been a free-for-all for thirty-five years. Changing that will be very difficult to do.

Lucas Pardue: Cases I'm familiar with in the UK, there are cases where organizations want you to sign a contract that gives up your rights to X, and these contracts are not valid by law. Can you do that? Does this principle apply to opt-in or opt-out here?

Tommy Pauly echoes Lucas, that in the same way that the absence of a signal exists in the context of the underlying laws, etc; the presence of a preference is still just a signal that still exists within the context of other considerations (and that context may nullify the preference's effectiveness)


### Attachment mechanisms

Suresh: Http header fields, link relations, JSON formats and other protocols. Anything else?

Thomas McCarthy-Howe: This vocabulary is a good candidate for the vCon WG to describe "consent for purpose" 
for the audio/video/messaging/email the virtual conversation contains. 

Glenn Deen... cryptographic binding.

Martin points out that bringing cryptographic binding into scope would be a good way to make sure this WG never finishes.

Suresh points out that we do need to make progress quickly. Just because we don't get started on something now doesn't mean we never do it.

Martin talks about identifying the few places and mechanisms where we can have the most impact.

Dapeng Liu asks if we have considered liaising with other SDOs.

Suresh jumps to the slides around working with organizations, and requests that if people think of cases where we need this liaison work, that people bring it up early.

Mirja doesn't think an abstract discussion is useful here: if we want something, someone has to do the work. The same is true for other org. This is also true for binding and auth, it really depends on the protocol. 

Colin Perkins asks if we are expecting to define a single grammar across different formats, and if so, is it abstract or something specific that will be able to fit into all formats. Suggests that abstract format is more achievable.

Gary: when we rolled out robots.txt for this, switched to structured values. These could fit into different formats. It might be difficult to convince everyone to use the same format, but it's something we've done before. Suresh summarizes as concrete format with extensibility.

J-F: Notes that we may want specific liaisons with *** (ITU SG 13 / 17, please correct if wrong)
SG17 definitely working on existing and new Work Items that may be related to this WG's work.
Wondering if some of the work of the new SG21 will also be "relatable", even if it's media/broadcast oriented.

Alissa: Question for leonard (who isn't here), we often get liaison statements that "this work is kicking off", without much more. Should we be sending something out that makes other groups aware in a similar way?

### Combining Preferences

Suresh points out that this charter point is the most complex to deliver (reconciling multiple expressions of preference). Our timeline is to deliver by August. (!!)

Mike Bishop (as responsible AD): :surprised-pikachu:

Farzaneh: I thought August was vocabulary-only? Can we do both in parallel?

Suresh confirms that vocabulary and preference expression are both due in August.

Farzaneh asks to do this work in parallel, don't wait for vocab to finish.

Sarah Jennings: Question about the combining point; can be when you have two explicit expressions that are in conflict, vs cases where the same content shows up in different spots with different preferences. The latter case is more like a copyright issue, and might be out of scope.

Jari Arkko wonders why this is complicated. yes, there is logic about how to combine things, but most of the argument should be about the vocabulary around the things are combined.

Martin thinks the vocab questions are most important. Would like to get more time to discuss interesting questions there. Questions like are we talking about "gathering" or "training", purposes, etc. Best to have that discussion with more people who may not be here.

### Licensing Schemes

Suresh points out that we ruled out the licensing schemes from our initial work. If you're interested, please go do the work and bring it back, but that's not where we're working to start.

### Matters for Policymakers

Suresh says that it is key that we express clearly to policymakers what we are working on (and not), and continue the dialog. Be clear about the limits of the technical mechansisms. Planning to meet with more policymakers in Brussels.

Farzaneh agrees this is important. Robots.txt is explicitly mentioned in documents, and mentions subsequent work in IETF.

Glenn asks if there will be a dress code in Brussels. Suresh says no =)

## Candidate Drafts

We have some drafts already being proposed!

https://datatracker.ietf.org/group/aipref/documents/

Martin brings up his draft https://www.ietf.org/archive/id/draft-thomson-aipref-sup-00.html
This is as simple as he can manage. HTTP header and extensions to robots.txt. Combines usage and training, does not distinguish them. We should have a debate about that. Does not have many attributes: just "yes", "no", or lack of signal. There's a bit of hierarchy, with gen AI is a subset of AI, which is a subset of TDM (text and data mining).

Gary talks about https://datatracker.ietf.org/doc/draft-vaughan-aipref-vocab/ and https://datatracker.ietf.org/doc/draft-illyes-repext/. Doesn't change robots.txt. Does changes robots headers (moves it out of X- header space). Changing the header key also lets the value format change. Moves to structured fields. Different spelling from Martin's draft for the header. Gary urges that we shouldn't have a new header, but a redefining of an existing header.

Thom Vaughan (https://datatracker.ietf.org/doc/draft-vaughan-aipref-vocab/) isn't here, but please look at his draft.

## Open Mic

Lucas Pardue is hearing a lot about scraping. Are we also considering posting, i.e., sending data in the other direction? Suresh has noted that this been discussed on the list. Design should support this.

Martin Thomson notes that robots exclusion expresses things about the whole server, while the robot headers bind to the resource; the header field Martin proposes is about the content of the message, which could support Lucas's case.

Martin notes that Thom's draft includes an expiration time, which is a constraint on the constraint. We should discuss whether this, in general, is a useful thing to have.

Suresh: The way we're thinking about this is, if it's not positively needed, it's out

Glenn Deen: That ability might be useful for content embargo, if the constraint refers to a not yet valid URL.

Gary: :mind exploding emoji:

Alissa: This was brought up in the case where the preference might be passed through between different parties, where someone downstream needs to decide what they are allowed to do. I can see why they want to pass down the set of preferences. Points out that unless there is a norm to respect expiration time, it will likely be ignored.

Suresh agrees we should keep it simple, but check if there's something we're missing out on.

Jonathan: Speculative idea of news organization that says you need to pay, and if you don't, you need to wait 15 minutes.

Lars: Along the lines of what Alissa said -- unless someone can explain a compelling reason to keep this, we should have this go.

Max Gendler: In use cases where publishers declare future or conditional access to content, this isn't generally done via open feeds, it's behind an API. So this use case here doesn't make sense in this context.

Sarah: You might want control over using out of date data, for reputational risk purposes.

Martin refers to a lot of discussion in the chat about RAG. It might be interesting to separate training from generation usage, but we probably can't make progress in seven minutes...


