# AI Preferences WG Interim Meeting Minutes


## Wednesday, 21 October 2026

Mark introduced the meeting, as a checkpoint before IETF San Francisco, to continue the conversation.

The most recent draft is vocabulary-08. It doesn't have consensus, but we want to get to consensus soon. This meeting will go through the issues list.

### Issue 208

Can we close 208? The word "substantive" doesn't appear in the draft. No-one voiced a concern about closing.

### Issue 172

Mark: Issue 172, RAG and grounding category, we now have the ai-use category. Closing.

### Issue 150

Mark: Issue 150, substitutive use category, from Brad. Brad confirms this can be closed.

Keep open the display based preferences issue.

### Issues 153 and 154

Two issues from EKR, 153 and 154. EKR wants to re-read those.

### Issue 163

Issue 163: Asset terminology. Martin has waited for other discussion to settle down, but has now created a PR to replace "asset" with "artifact", and suggests leaving until other issues are settled. Timid pointed out that the PR needs updating to change the terminology section. Mark suggested sending objections to the list.

### Issue 167

Issue 167. Distinguishing access from use. Martin created a PR to edit section 3.3. Mark suggests the word "prevent" might be too strong, an alternative might be "restrict" or "constrain". EKR suggested how it correspond to things like robots.txt, and not to focus so much on the mechanisms. Kevin agreed with EKR.

### Issue 192

Issue 192, relation to existing laws. Max should come back with a revised proposal if he still wants to pursue this.

### Issue 217

Issue 217, use of "synthetic". The draft still uses that word. Chris explain that synthetic opens a distinction where material that's quoted. Mark suggested that the word should do work, if we included. 

Kevin: <missed>

Timid: It's about trying to create a line between classifier type uses and more generative, or where content is completely new and not cited. We need to make the line clearer. I prefer to keep "synthetic", but it's not successful drawing the line.

EKR: The sentence below talks about classifiers, so more load-bearing than the word "synthetic". Identify which things are or aren't synthetic. Try to agree what's in scope vs not, as a suggestion. I'm uncomfortable with it being load-bearing.

Mark: For people who want to keep it, can they create a definition?

Brad: Agree with Chris, and share EKR's concern. The main rationale that's already covered. There needs to be a line between a generative and non-generative AI mode. I worry about keeping the word, your suggestion to define it makes sense. I'd vote for deleting it.

Nate: I also think we should delete it. In copyright context, AI companies can argue that the content is original content. Absence evidence the word is load-bearing, we should remove it.

Kevin: The output Nate describes is what the definition intends to cover. We're not trying to create a loophole, there needs to be trust.

Nate: I recognise your good intent. But we need this to work for companies not represented here.

EKR: It's not an issue of trust, but we need to be clear for people who haven't participated in this process. The document should stand on its own feet.

Timid: Maybe better to remove it and ask people to make the case to add it back in. I'm hearing more investment from the people who want it removed.

Chris: Happy to work with others offline, or go with Timid's proposal

Paul: Concur with Timid

Matthew: Also agree with Timid's proposal and EKR.

Mark ran a straw poll, "Do you feel strongly that we should keep the 'synthetic' term in the draft"?

Farzaneh: We don't have enough background on why synthetic is there, can we defer a poll to the IETF meeting?

Poll result: Yes: 3, No: 15, No Opinion: 1

Mark and Suresh asked that people coordinate to make the case, and to come up with a definition, and to flesh out the argument for removing, going into San Francisco.

### Issue 231

Issue 231, de-minimis content generation. Erin suggested that it may have been folded into the draft already, but wasn't sure. Martin pointed to the last comment in the issue, which explains where it's addressed. There was discussion about whether the issue operates at a higher level across the draft, so will need to be reviewed carefully.

### Issue 245

Mark: Issue 245, redistribution of models.

Kevin: I think we agree on the intent, redistributing a model shouldn't be a way to launder preferences, but how to phrase it in the vocabulary?

Martin: There are two PRs that address this. One from Timid, which was closed, but there's 253 that includes text that could address the issue, albeit not directly. There's text in the current draft, that Timid proposed, on conveying.

Timid: That's old, look at draft 08 section 3.3. I'm happy to close 245.

EKR: If I scrape sites and convey the data, I don't have to convey preferences. But if I train a model I do. It's an odd asymmetry.

Mark: If you're training models, wilful blindness isn't compliance, is what we're saying.

Eric: If A scrapes and distributes the data, and B trains on it. B can simply elide them.

Mark: Agree, A scraping and eliding the preferences should not protect B.

Martin: EKR's concern is reasonable. I opened PR 252 and 253 to address a different point, but that text would address the retention of preferences with crawling and scraping, and then transformation. Leonard and Nate have voiced concerns. If you want symmetry, look at those PRs.

Brad: For us, separating use preference from crawling through to distribution of the model. It's important that it does travel. Don't like introducing the idea of wilful blindness, legal constructs.

Mark: As written it's a requirement on someone not doing AI training, which is weird. You can't comply with preferences if you don't have full information about them.

Brad: There's substantial activity in crawling that aren't those developing or distributing models. It would leave a big gap if we require the crawling and model developing to be the same party.

Mark: We'll revisit in San Francisco.

Timid: Common Crawl already bundles preferences with headers and robots.txt. They help with internet archive, so a significant part of the archiving community is already doing this.

### Issue 246

Mark: Issue 246, caching and embedding.

Martin: There was a concern that someone would collect stuff and apply a transformation, e.g., HTML to markdown or creating an embedding and distributing it. We expect preferences to be carried forward. Leonard raised 240, which is an alternate spelling of it.

Timid: I like this text (in 253). It empowers people to honour preferences if that's their intent.

Suresh: I prefer the term "ensure" from PR 252.

Martin: Sounds good, we can align the two.

Kevin: What does 253 change? In an AI system, text is tokenised and transformed into embeddings in an implementation of the system. It seems that trying to identify the component parts of the system if problematic, things not invented or thought of now might be considered not in scope.

Timid: This tries to target processes pre-training and pre-tokenisation. Nate spoke about existing markets where third parties selling data APIs, where the data has been transformed from the data crawled or collected.

Nate: There are 3P APIs that will sell the embeddings, drawn from the materials. It's important that the preferences applies to those embeddings. Tyler also raised the concerns.

Kevin: Does this make sense as part of the crawling conversation, if that's the case you want to cover?

Nate: Maybe, I'd need to review the whole thing. Also, someone with more technical knowledge.

Matt: Would it address Kevin's concern to say that it happens between different parties?

Kevin: In the past we've tried to avoid caring about organisational boundaries.

Martin: A system could span organisations. We could say different parties if it would help clarify things.

Mark: We nee more discussion, e.g., on the list.

### Issue 247

Mark: Issue 247 on creating a data model, from Leonard.

Martin: I see this as an editorial issue. It doesn't change the meaning. But the discussion is whether the draft describes the data model clearly enough.

### Issue 249

Martin: This is where Chris and Kevin's proposal to come in.

Kevin: The RAG/grounding distinction. We landed on a two part definition. The user has to express specific intent to interact with a resource and it has to be a specific resource. If you ask a question and the AI system finds resources, it's in scope. If the user gives the URL, that's outside.

Other categories are worth talking about also.

Chris: That's right, this is an attempt to define what's directly provided.

Timid: I think it's a good definition of what was previously called system use. I think people want to express a preference of what's excluded here. That shouldn't hold this up, but the naming needs to be more specific.

Brad: I find this to be in the opposite direction. Rather than provide the asset to interact with the asset. I thought providing it was the dividing line. What's excluded is the part that's more damaging: I want you to go find this article and summarise it (what does interact mean?) This is the intermediation that we want to express a preference about. Just because you've identified a specific asset it shouldn't bypass.

Alissa: Two questions. Who is doing the interacting? Implies the intent is for the AI system, but not clear. Hypothetically, I talk to a chatbot and say go to the bbc.co.uk homepage, is that providing the asset.

Kevin: In our discussion, that would not be interacting with a specific asset.

Chris: To Brad's point, my intent was it's for cases where the user has already seen the asset, so the intent isn't to include substitutive use.

Nate: Need categories to cover all use. On line drawing, I gave an example of clicking a link in search. This is a difficult line to draw in practice, and hard for courts to determine. The line still is unclear.

Eric: What does specific intent mean here? If it's unambiguous and you don't need AI to distinguish? Drawing the line between a general asset and specific asset.

Mark: The question is where to draw the line, then how to. A couple of options, have a definition with the carve-out or all use. We'll discuss the other aspects, but the task here is the line drawing. Encourage work on proposals on how to draw the line.

Martin: This is an admirable attempt with economical use of words. The line requires some precision, on how the resource is identified. There could be different interpretations.

Mark: Agree. Write proposals with more words that we could cut down later, include explanatory cases to communicate intent.

Alissa: Would it be easier to define the exception? Previous discussion of things that don't change weights. Figure out what the exception is.

Martin: A specific category?

Alissa: Agree you'll need more words to describe it, but honing in on the exception might be more straightforward conceptually might be easier. It would be a defined term, then has relationship to prior definition of things that don't change the weights, that was discussed in London.

Nate: If we have an exception, we need to be clear about what it is. I proposed two expressed categories. What do we intend to exclude, and for what purpose? Example of a dance video that people use AI to make copycat videos. It happens at scale. Spammers are users too. Why are we drawing the line? What do we actually want to exclude?

Farzaneh: In London we talked about carve-outs for accessibility and text to speech. We should discuss that as well, similar to what we have for search.

Mark: That's still to do, yes.

Mark: Good discussion today. There's things to work on for San Francisco. Bring to the mailing list. We haven't declared consensus on anything yet. We want too run some consensus calls soon. If issues need more consideration, bring them to our attention soon.

Suresh: Farzaneh, you were going to write a document on the use case. Please do for San Francisco if you can.

Nate: Important we don't abandon artists, and make this a publisher focused protocol. I've been told to add to the use case wiki, but it's not being used in the discussion. If we have a carve out for user intent, the onus needs to be on those proposing it. Arguments for accessibility usage being non consensual. If there's other usage that animates it, let's discuss. I've put forward examples in the wiki that are harmful, but there's no engagement. Some of us want to preserve a human internet. We're talking about abandoning artists and creators. That perspective is under represented here. I'm concerned about the direction here.

Mark: We're at time. Take thoughts to the mailing list. Be ready for San Francisco. Thanks all.
