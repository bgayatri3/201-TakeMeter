
# 201-TakeMeter: Planning

## Community Choice

<!-- Write a 2–3 sentence description of your community, your labels, and why these distinctions matter to people in that community. Reasoning: Explain why this community was chosen and why it is suitable for a text classification task. Discuss the relevance of the labels and any interesting characteristics of the community. -->


### Selected Community

[r/Books](https://www.reddit.com/r/books/wiki/relatedsubreddits/) - " a moderated subreddit [with the] intent and purpose to foster and encourage in-depth discussion about all things related to books, authors, genres, or publishing in a safe, supportive environment" (reddit bio)

This community was chosen because book-lovers can be strongly opinonated about what they're reading. There is a lot active discourse which might make it difficult for new readers to navigate. Classification will help those new to the community, find exactly what they are looking for. Reviews are helpful for those looking for new books to read based on their general interests. Long term readers might be looking for literary analyses of their favorite books to discover new nuances. Others seeking community might go to questions/discussions to further engage with others. Readers have a diverse set of goals and perspective and by having clear labels, they will have a better experience engaging with the r/books reddit since it garners 10k+ weekly contributions with 1.3M weekly visitors. 


## Label Taxonomy
### Label Definitions

| Label   | Definition  | Common Signals
| ------- | ----------- | ----------- |
| Questions/Discussion          | These posts focus on inviting conversation, seeking, or sharing information | question marks, what do you think, why does, did anyone notice, requests for clarification/interpretation, news/article shared |
| Review                        | These posts focus on evaluation and personal judgement of a book.| ratings, 4/5 stars, personal reactions, really liked/didn't like, answer the question was it good |
| Literary Analysis             | These posts focus on interpretation, themes, structure, techniques, or meaning. | discussion of theme, symbolism, character develpment, narrative structure, concrete evidence from the text, analysis of author's choices |

## Example Posts for Each Label
### Questions/Discussion 

* **Example 1:** "The Obama and Trump libraries are going digital. Historians aren’t sure that’s a good idea...Modern day burning of the Library of Alexandria. Control of the data can be as destructive as a fire.....Going fully digital sounds convenient but honestly feels risky when it comes to long-term preservation of history" ([source](https://www.reddit.com/r/books/comments/1u70erx/the_obama_and_trump_libraries_are_going_digital/))
* **Example 2**: "Why “book-shaming” won’t solve the children’s literacy crisis — The nation’s official advocate for children’s books says most of them are “crud.” But matters of literary quality don’t explain why kids aren’t reading" ([source](https://www.reddit.com/r/books/comments/1u81wxu/why_bookshaming_wont_solve_the_childrens_literacy/))
* **Boundary Example**: "Does anyone else think Freda Mac Fadens male character are supper repeative....A lot of the male characters seem to fall into either "perfect, supportive guy" or "secretly awful psychopath" with not much in between" ([source](https://www.reddit.com/r/bookdiscussion/comments/1tzt5zs/does_anyone_else_think_freda_mac_fadens_male/))
    - This example is borderline on literary analysis since it interprets character development in a novel. However, since it is posed as a question to the community it falls under this label. 

### Review

* **Example 1**: "Last year I read The Hobbit and The Lord of the Rings trilogy. Some thoughts....This was a rough read for me. Almost all of the little things I hadn't liked in previous books feel like they're crammed into this book" ([source](https://www.reddit.com/r/books/comments/1ualldt/last_year_i_read_the_hobbit_and_the_lord_of_the/))
* **Example 2**: "1984 by George Orwell...The premise alone pulled me in immediately. dark, oppressive, and honestly kind of suffocating. The entire book just reeks of despair and brokenness in a way that feels intentional and relentless. It’s not just the setting, it’s the tone. everything feels controlled, hollow, and stripped of hope" ([source](https://www.reddit.com/r/books/comments/1u4qjkl/1984_by_george_orwell/))
* **Boundary Example**: "With alternating timelines that shift from the present to the past to fill in the backstory, the pacing was too slow, and the story dragged multiple times while reading...With repetitive moments and side characters that didn’t add anything to the story, this was an unmemorable read, and that’s a shame.... give “The Children” by Melissa Albert a 2-Star rating out of 5."
    - This example is tricky since it does bring up some literary elements like pacing and character development. However, it is still overall an opinion pieces and does include a rating. ([source](https://www.reddit.com/r/books/comments/1ua03ru/review_the_children_by_melissa_albert/))


### Literary Analysis

* **Example 1**: "The Hunchback of Notre Dame and the tragedy of mistaken identity....This theme of dualism and duplicity is likewise represented by the character of the cathedral itself. In many ways, Hunchback is Hugo’s attempt to get us to read an essay about Notre Dame and gothic architecture by dressing it up in a novel" ([source](https://www.reddit.com/r/books/comments/1u7we9e/the_hunchback_of_notre_dame_and_the_tragedy_of/))
* **Example 2**: "Men are Shrimp - An Analysis of "The Youngest Doll" by Rosario Ferre...theme of this text is about how women are taken advantage of by men...rawn symbolizes the corruption, exploitation, and objectification of women" ([source](https://www.reddit.com/r/LiteraryAnalysis/comments/1sxxg6r/men_are_shrimp_an_analysis_of_the_youngest_doll/))
* **Boundary Example**: "The Vegetarian by Han Kang is Brilliantly Unsettling...The Vegetarian by Han Kang is Brilliantly Unsettling....he different POVs compliment the themes and intentions of each part well. For example, it definitely sets the tone that we start a book about a woman's decision with a first person POV from her husband"
     - This example does contain some opinion but is still an analysis because it overall focuses more on how literary elements contribute to the overall theme of the book. The focus is still interpretation and explaining how the book works, rather than personal judgement of the book. ([source](https://www.reddit.com/r/books/comments/1u62xne/the_vegetarian_by_han_kang_is_brilliantly/))

### Anticipated Edge Case
The trickest edge case will be between literary analysis and review. Sometimes reviews contain a mix of opinion and are backed by some literary analysis. During annotation this will be handled because the distinguishing features will be if there is more literary analysis or more opinion when looking at the post holistically. There are also some recognizable aspects in a review specifically like a rating or the word review too. 

---

## Data Collection Plan
<!-- Where will you collect examples? How many per label? What will you do if a label is underrepresented after 200 examples? -->

Samples will be collected direclty from r/Books from the all time posts tab. The goal for label distribution is 33% for each label. However, from skimming the community it seems that the Question/Discussion label will be quite popular. Thus, it may skew more towards that specific label. Therefore, the goal will be 25%-40% label coverage of the 200 labels. If a label is underrepresented after 200 examples, then some of the most frequent labels will be swapped out. 


---

## Evaluation Metrics
<!-- Which metrics will you use to evaluate your model and why are those the right ones for this specific task? (Accuracy alone is not enough — explain what else you need and why.) -->

The primary metric will be accuracy since it provides a holistic measure of the classifier's prediction ability. However, some labels may be more common than others and certain mistakes are more costly than others, so other indicators must also be utilized. 

Therefore, precision, recall, and F1-score will also be reported for each label

- Precision measures how often a predicted label is correct.
- Recall measures how often the model successfully finds examples of a label.
- F1-score balances precision and recall.

A confusion matrix will also be used to identify which labels are most frequently confused with one another. This is particularly important because Literary Analysis and Review are expected to overlap conceptually, making them likely sources of classification errors.

The final evaluation will report:
- Accuracy
- Precision per class
- Recall per class
- F1-score per class
- Confusion matrix

---

## Definition of Success
<!-- What performance would make this classifier genuinely useful? What would you accept as "good enough" for deployment in a real community tool? -->

This classifier would be considered successful if it can reliably distinguish between Questions/Discussion, Review, and Literary Analysis posts at a level that is useful for readers browsing the community.

A realistic deployment target would be:
- Overall accuracy above 80%
- F1-score above 0.75 for each class
- Minimal confusion between Review and Literary Analysis

Even if some overlap remains between these two labels, the classifier would still be useful if most posts are routed into the correct general category. For a community browsing tool, consistent performance and understandable mistakes are more important than perfect classification.

---

## AI Tool Plan 
### Label stress-testing: 
<!-- Give the AI your label definitions and edge case description, and ask it to generate 5–10 posts that sit at the boundary between two labels. If it produces posts you can't classify cleanly, your definitions need tightening — do that now, before you annotate 200 examples. -->
After asking ChatGPT to identify patterns with 5 posts that sit at the boundary, I added more keywords that belong to the labels to tighten up the definitions. 

### Annotation assistance: 
<!-- Decide whether you'll use an LLM to pre-label a batch of examples before reviewing them yourself. If yes, note which tool you'll use and how you'll track which examples were pre-labeled (for disclosure in your AI usage section). -->
AI was not used for labeling assistance. Instead, examples were manually labeled by the annotator to ensure consistency and to remain grounded with the dataset.


<!-- Plan to give your list of wrong predictions to an AI tool and ask it to identify patterns before you write up your evaluation. Note what you'll look for and how you'll verify the patterns yourself. -->
### Failure Analysis

After evaluation, all incorrectly classified examples will be collected and reviewed. ChatGPT will be asked to identify common patterns among the errors, such as recurring language features or specific label pairs that are frequently confused.

Potential patterns suggested by the AI will be verified manually by examining the original posts and confusion matrix results. Particular attention will be paid to mistakes involving Review and Literary Analysis, since these categories are expected to have the greatest overlap.
