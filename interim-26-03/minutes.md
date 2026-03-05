# AIPREF Working Group Interim Meeting - 2026-03

[AIPREF Working Group Interim Meeting Agenda - 2026-03](https://ietf-wg-aipref.github.io/wg-materials/interim-26-03/agenda.html)

## terminology issues
terminology issues search: https://github.com/ietf-wg-aipref/drafts/issues?q=is%3Aissue%20state%3Aopen%20label%3Aterminology

### RE: [Use of “fine-tune” in “Foundation AI Model Production” category · Issue #179](https://github.com/ietf-wg-aipref/drafts/issues/179)

Phase in question: "Fine-tuning can specialize a general-purpose foundation model for a narrower set of use cases." ()

Martin: Overly broad is objectionable as overly emotive language.  However, this is about the scope of the definition of what we call "AI training".

Timid Robot: Maybe some folks at AI companies can help us come up with a definition. It should be clear what we are trying to get at, so maybe people can suggest ways to phrase this.

Chris Needham: We need to all aspects of what we have currently called foundational model production.  This fits within this definition.  I don't think that it is helpful to include all the aspects of production.  To the extent that fine tuning is part of the creation of models, it should be included.

Alissa: Something to think about that might help is "when does a model stop being produced", which might be the boundary condition.  Asking what defines production might be answered by asking when the production process ends.

Pedro: There is something that can be done from a technical research point of view, this can mean several different things.  But if we worry about just production, it might be easier to talk about whether the model weights are changing.  That might be a better framing.  There is no single technical term, but weights changing might be more specific.


### RE: [Replacing: "digital assets" with "digital content" · Issue #163](https://github.com/ietf-wg-aipref/drafts/issues/163)

Martin: Asset often means someone owns something (agreeing with issue description). Maybe too tied to the notion of copyright.

Lila: Agreeing (avoid "asset"). "Asset" seems too specific. "Content" seems better.

Farzaneh: Agreeing (avoid "asset"). Could lead to complications with asset-level signaling.

Sarah: Agreeing (avoid "asset").

### RE: [Removing normative language: respect, ignore · Issue #162](https://github.com/ietf-wg-aipref/drafts/issues/162)

No comments

### RE: [Use of 'Machine Learning' · Issue #152](https://github.com/ietf-wg-aipref/drafts/issues/152)

Timid Robot: I have heard this term being used constructively that carries far more meaning than an unadorned "AI".

Nate: Also agree.  AI is marketing that doesn't mean anything. Without the term machine learning it is too amorphous.

### RE: [Definition of AI · Issue #151](https://github.com/ietf-wg-aipref/drafts/issues/151)

Martin: Hard to find good definitions.  This extrapolates from a bunch of other definitions, with an eye to our goals.

Erik: Until we have a better alternative, then we have to stick with what we have.  It would be helpful to have people identify specific failings in the definition, so if it includes things you don't want to include, maybe specific exclusions could be used.

Chris: I think we should have a definition, rather than leave it to interpretation.  This is a reasonable attempt to use existing definitions to create our own.  This is not far off what a reasonable definition is.  But I'd worry about omission.

Meredith: Having use cases might be useful in moving forward on these.  You have to start with use cases and evaluate the definition against them.  Things get circular without concrete tests that w can judge against.

Chris: Would be helpful, but willing to help in a limited fashion.

Elaine: Has a decision been made that OECD definitions are not good.

Suresh: If you have proposals please make them; e.g., ITU definitions were discussed and not felt to be to purpose.

Martin: Happy to look at other definitions. What we have is close to the OECD definition; however a few parts of that are weird. There's an academic paper about this, it's a persuasive analysis. This is captured in another issue.

Alissa: Not sure there's broad support for the concern raised here.

Erik Stallman: There's a separate NIST definition. My sense was that the OECD definition was considered; is that correct?

MT: yes. It was one of the main sources; it is a pretty good definition, there were a few adjustments necessary because they're so broad.

## training issues
issues search: https://github.com/ietf-wg-aipref/drafts/issues?q=is%3Aissue%20state%3Aopen%20label%3Atraining

### RE: [Quantified thresholds in definition of Foundation Model Production are ambiguous · Issue #183](https://github.com/ietf-wg-aipref/drafts/issues/183)

Pedro: there's an issue if we say it's too small or too large. could be easy to confuse with foundation model and clasical search

Martin: all defitions appear to share a comon setem, but diverge significantly when concrete numbers are used. Agreeing with Pedro, we should use other means to distinguish.

Suresh: EU doesn't talk about specific numbers.

Martin: yes, but American models do.

Pedro: Talking in terms of parameters is extremely dangerous.  Current research is about retaining capabilities, but reducing the number of parameters.  Smaller models that are more capable.

Chris: Trying to quantify is likely to be counterproductive.  This needs to be usable by creators and publishers.  They aren't going to be experts on model creation.  They just need to understand the scope.

Alissa: asn't Maybe take the "large" part out.  Focus on the operative part: capabilities, etc...

### RE: [AI Training and Generative AI Training are Too Broad · Issue #157](https://github.com/ietf-wg-aipref/drafts/issues/157https://github.com/ietf-wg-aipref/drafts/issues/157)

Martin: overtaken by events. Current draft has "Foundation Model". Don't need to remove "AI training" from 5.2. We do still need to address previously discussed issues on terminology.

## search issues
serach issues: https://github.com/ietf-wg-aipref/drafts/issues?q=is%3Aissue%20state%3Aopen%20label%3Asearch

### RE: [Search Cateogry May Lead to Unintended Effects · Issue #187](https://github.com/ietf-wg-aipref/drafts/issues/187)

Caleb: happy to propose a resolution. 

Suresh: Krishna has a similar issue. May be able to resolve multiple with a poposal.

Erik: need clarification on what is/isn't allowed by this category

Pedro: reminder that currently there is no non-AI search. only the output differs between "classic" and "AI" search

### RE: [Search category definition attempts to redefine established search behavior · Issue #181](https://github.com/ietf-wg-aipref/drafts/issues/181)

Alisa: may be worthwhile to use specific categories in issue instead of single category. not sure if it was considered/discussed

Martin: we did discuss, couldn't make sense

Alisa: they make more sense to me

Martin: may be worth more discussion, maybe room for split into discrete categories

Mark: there wass concern about additional attachment mechanisms

Meredith: If there is any difference between search and model building: would it be considered neutral/negative if people change their technology to work around definitions.  Is that a likely outcome and would that be good?

Pedro: Maintaining two technologies, especially if one is outdated, is not practical. I don't see people doing that to avoid policy.  I would see people not indexing content that they couldn't use with their preferred technology.

Paul: It is fair to say that we didn't discuss this in full detail.  It is valuable to discuss them.  Two points to make: we need clarity for the context: vocab or specific attachment.  Some items in Microsoft's draft are very attachment-mechanism-specific.

### RE: [Search is too Broad · Issue #173 · ietf-wg-aipref/drafts](https://github.com/ietf-wg-aipref/drafts/issues/173)

Mark: already covered in previous dicussions

Chris: no further dicussion needed (pending proposal from Caleb)

### RE: [Search should be removed and replaced with display-based preferences · Issue #171](https://github.com/ietf-wg-aipref/drafts/issues/171)

Mark: also previous covered, with more discussion in Toronto

## use issues
issue search: https://github.com/ietf-wg-aipref/drafts/issues?q=is%3Aissue%20state%3Aopen%20label%3Ause

Mark: encourage group to add/update proposals to move this forward

Nate: there must be something to ground RAG--to address summaries

Martin: please provide proposals 1+ weeks before meeting (ideally 2+). this is the central issue, very important for the future of the web

Mark: also see https://github.com/ietf-wg-aipref/drafts/wiki/Use-Proposals

Chris: agree with Nate--this is fundamental. vocabulary must address RAG, post-training, etc. Misattribution.  Can cause reputational damage unless we have some way to cover post-training usage.  Not sure on why things stalled and happy to work on something.

## model issues
issues search: https://github.com/ietf-wg-aipref/drafts/issues?q=is%3Aissue%20state%3Aopen%20label%3Amodel

### RE: Hierarchical structure is problematic and introduces unnecessary complexity · Issue #170

Martin: in limbo pending other category discussions

### RE: Focus on purpose of use rather than time of ingestion · Issue #159 

no comments

### RE: [Defaults · Issue #154](https://github.com/ietf-wg-aipref/drafts/issues/154), [Difference between "unknown" and "allowed" · Issue #153](https://github.com/ietf-wg-aipref/drafts/issues/153)

Martin: EKR is trying to 'refactor the code'; I'm struggling to identify the concrete reason to change here. What's proposed is reasonable but I'm not sure there's value in doing so. Not substantive. Prefer we defer this.

## context issues
issue search: https://github.com/ietf-wg-aipref/drafts/issues?q=is%3Aissue%20state%3Aopen%20label%3Avocabulary%20label%3Acontext

### RE: [Introduction clarity re: relation to existing laws · Issue #192](https://github.com/ietf-wg-aipref/drafts/issues/192)

Max: Want to spend a lot of time at April meeting on this. Two perspectives: 1) work we do is isolated 2) work is more contextual. We need more time to get into nuances.

### RE: [Distinguishing access and use · Issue #167](https://github.com/ietf-wg-aipref/drafts/issues/167)

Margin: we haven't been clear in our intent. there are two actions involves with robots.txt: 1) existing crawl directives 2) AI Pref only apply to downstream uses of "stuff"

Timid Robot: much of our conversations have focused on access. we may need more documentation about how preferences travel with "stuff" so they are available to downstream users

Martin: will oppen an issue to track that

Lila: concern about bundling preferences with "stuff" (or concern about it not be adequately bundled). Thank you Martin.

Victoria: echo what Lila said. the importance of clarity is hard to overstate for users, if not done well will have chilling effects

Jo: what we did in ARDC standard, was to specify it should be carried with.

### RE: [3.1 Conformance · Issue #164](https://github.com/ietf-wg-aipref/drafts/issues/164)

EKR: is non-conformance possible with volunteer document

Suresh: it's not about compliance

Mark: if an entity claims conformance--separation of conformance to porocessing and conformance to prefernces

Jo: my concern is that it pertains to enforcement. if there isn't an enforcement mechnaism built in, it should be obvious

Paul: there mighte be some misunderstanding about what layer this applies to. this is about conformance of attachment layers to the vocabulary. it is not about enforcement. (compliance vs conformance)

Elaine: i found it confusing because there are very few MUSTs and MUST NOTs.

Mark: ask for proposals that clarify

### RE: [3.2 Respecting Preferences · Issue #160](https://github.com/ietf-wg-aipref/drafts/issues/160)

no comments

### RE: [Bots Collect Data for Multiple Purposes · Issue #158](https://github.com/ietf-wg-aipref/drafts/issues/158)

Mark: appears to be related to use

EKR: may be fine, now, the way it is, given the direction it is moving