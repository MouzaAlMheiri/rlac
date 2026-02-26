---
title: "Assignment 1"
categories:
  - Blog
tags:
  - Post Formats
  - quote
---


Emotional Extremes in the Wizarding World: A Computational Study of Canon and Fanfiction

SECTION 1 Corpus and Research Questions
If there is one thing the Harry Potter universe does extremely well, it is emotion. Fear, loyalty, grief, anger; everything in this world feels just slightly heightened. Because of that, we started with a simple curiosity: does the language actually reflect that emotional intensity, and does fanfiction push it even further?

To explore this, we assembled a mixed corpus of five texts drawn from both the official Harry Potter series and popular fanfiction communities. Altogether, the corpus contains 441,225 total words and 18,063 unique word forms, which gave us more than enough material to work with. The longest texts are Harry Potter and the Half Blood Prince (171,668 words) and the fanfiction Wishmaster Harry Potter (107,373 words), while the shortest are Reconstructing HP (23,880 words) and HP Next Gen (33,391 words). This range actually worked in our favor because it let us compare emotional language across long canonical novels and shorter, more experimental fan works.
Image1.png

We chose this corpus very intentionally. The Harry Potter storyline is built on emotional stakes, and fanfiction communities are known for amplifying those stakes even more, especially when it comes to romance and interpersonal conflict. That made this dataset a really good test case for tracking how emotional language shifts across authors and contexts.
Our analysis is guided by three main questions:
What emotions appear most strongly across the texts?
How do emotional patterns shift throughout each narrative?
How does emotional language cluster around key characters?


Rather than replacing close reading, our goal was to use computational tools to zoom out and notice patterns that would be almost impossible to track manually.

SECTION 1.5 Background Research and Contextualization
Before jumping into the visualizations, we needed to understand the context behind the texts themselves. The two canonical novels in our dataset, Harry Potter and the Half Blood Prince (2005) and Harry Potter and the Prisoner of Azkaban (1999), were written by J. K. Rowling and published through major commercial presses such as Bloomsbury and Scholastic. These books went through heavy editorial processes and were written for a massive global audience. Because of that, we expected them to show more stylistic control and more balanced emotional pacing.

The three fanfiction texts, Wishmaster Harry Potter, HP Next Gen, and Reconstructing HP, come from a completely different ecosystem. They were published online within participatory fan communities. As the Wikipedia article on fan fiction explains, this space encourages transformative storytelling, emotional experimentation, and far fewer constraints than traditional publishing.

Going into the analysis, we honestly expected fanfiction to be more emotionally dramatic, especially in categories like love and conflict. At the same time, we assumed the canonical novels would show smoother emotional pacing. As the analysis shows, many of these assumptions were correct, but not all of them.
SECTION 2 Exploratory Analysis

To explore emotional patterns across the corpus, we combined Voyant Tools with R based analysis in Posit Cloud. Voyant helped us quickly explore large patterns, while R gave us more control to build targeted visualizations. Using both ended up being much more useful than relying on just one method.

2.1 Word Frequency and Emotional Distribution (Voyant Tools)
	
Our first step was to look at the overall emotional vocabulary across the five texts. Using Voyant’s Terms and Trends tools, we tracked four core emotion words: love, hope, fear, and anger.
Insert Image 1 here (your bar chart of emotions across 5 texts)
Embedded code:
<!--	Exported from Voyant Tools (voyant-tools.org).
The iframe src attribute below uses a relative protocol to better function with both
http and https sites, but if you're embedding this into a local web page (file protocol)
you should add an explicit protocol (https if you're using voyant-tools.org, otherwise
it depends on this server.
Feel free to change the height and width values or other styling below: -->
<iframe style='width: 100%; height: 800px;' src='https://voyant-tools.org/?view=Trends&corpus=a815ebe65cb4c2b0801510d2473dace2'></iframe>
Figure 1. Relative frequencies of four emotion terms across the five texts.
Right away, some patterns stood out. The fanfiction texts, especially HP Next Gen and Reconstructing HP, show noticeably higher frequencies of love. This was not exactly shocking, but seeing it visualized made the difference much more obvious.

Meanwhile, the canonical novels look much more emotionally balanced. Instead of one emotion dominating, the distribution stays relatively even.

Wishmaster Harry Potter was probably the most interesting case. It shows elevated levels of fear and anger, which gives it a noticeably darker emotional profile. Seeing this visually really confirmed that each text carries its own emotional fingerprint.

2.2 Emotional Trends Across Narrative Segments (Voyant Bubblelines)

Next, we wanted to see how emotions move across the timeline of each story. For this, we used Voyant’s Bubblelines tool, which shows where emotional keywords cluster throughout the narrative.
Embedded code:

<!--	Exported from Voyant Tools (voyant-tools.org).
The iframe src attribute below uses a relative protocol to better function with both
http and https sites, but if you're embedding this into a local web page (file protocol)
you should add an explicit protocol (https if you're using voyant-tools.org, otherwise
it depends on this server.
Feel free to change the height and width values or other styling below: -->
<iframe style='width: 100%; height: 800px;' src='https://voyant-tools.org/?view=Bubblelines&corpus=a815ebe65cb4c2b0801510d2473dace2'></iframe>
Figure 2. Bubblelines visualization showing the distribution of emotional keywords across all five texts.

What became obvious very quickly is that Wishmaster Harry Potter has dense clusters of fear, anger, and death related language. These spikes are not evenly spread; they come in bursts, which creates a much more volatile emotional rhythm.

By contrast, Half Blood Prince and Prisoner of Azkaban feel much more controlled. Their emotional terms are spread more smoothly across the text. This supports the idea that Rowling’s narrative structure carefully manages emotional pacing.

One thing that surprised us was that the shorter fanfictions do not spike constantly. Instead, they tend to concentrate emotional language around relationship heavy moments. So the intensity is definitely there, just more strategically placed than we initially expected.

We also noticed that emotional terms often rise and fall alongside specific character mentions. In the fanfictions, names like Harry, Ron, and Hermione tend to appear during moments of heightened tension, which may explain why fear and anger related words cluster so tightly around those sections. In contrast, the original novels show a steadier relationship between character presence and emotional language, suggesting a more deliberate balance between plot events and character driven emotion. This difference highlights how fanfiction often amplifies emotional extremes through its characters, while Rowling’s texts maintain a more even emotional flow.

2.3 Character Centered Emotional Patterns (Heatmap in Cloud R)

After exploring broad trends, we used to Cloud R to look more closely at how emotional language clusters around specific characters. We built a heatmap tracking the frequency of key terms harry, ron, hermione, love, hope, fear, anger, and dead.

We included dead/death as one of the tracked terms because death is a central emotional and narrative force in both the Harry Potter series and its fanfiction adaptations. Unlike love, fear, or anger which represent broad emotional states death functions as a plot defining event that often triggers intense emotional reactions in characters and readers. Including this term allowed us to see where moments of loss, threat, or mortality cluster in relation to key characters like Harry, Ron, and Hermione. It also helped highlight how fanfiction sometimes amplifies darker themes texts like Half Blood prince and Wishmaster Harry Potter show noticeably higher concentrations of death related language, reinforcing their more volatile emotional tone. By tracking dead/death alongside the core emotions, the heatmap captures a fuller picture of how both canon and fanfiction use mortality to shape emotional intensity. We noticed that when themes of death were high there was an increase of the emotion of emotion specifically present in the two JK Rowling novels we chose.

Image2.png
Figure 3. Heatmap showing the frequency of character and emotion terms across selected texts.

A few things became immediately clear. First, Harry completely dominates the corpus. This is expected narratively, but the scale of his dominance is much more striking when visualized.
Second, Ron’s presence fluctuates quite a bit across texts. He appears heavily in the Ron centered fanfiction but much less in Wishmaster. This suggests that fan fiction authors redistribute character focus depending on the story they want to tell.

Third, love peaks sharply in Next Gen, which strongly supports the idea that fanfiction often amplifies romantic themes and has a focus on other characters rather than just the main ones in the novel. Meanwhile, fear and anger appear consistently across both darker fanfics and canonical novels, reinforcing Harry’s long standing association with danger and conflict.

What this heat map really helped us see is how emotional language organizes itself around specific characters, something that would be extremely difficult to quantify through close reading alone.

2.4 Cross Text Comparison (Color Coded Word Cloud in R)

To step back and look at stylistic differences more broadly, we created a color coded word cloud in R. Each word is colored according to the text where it appears most frequently.
image3.png
Figure 4. Color coded word cloud showing dominant vocabulary across five texts.
Even at a glance, the differences are pretty clear:
Next Gen leans heavily into family and relationship vocabulary
Wishmaster foregrounds darker, conflict driven language
The canonical texts emphasize dialogue heavy terms like said, wand, and dumbledore
This visualization is especially helpful because it shows thematic clustering almost instantly. Without reading a single page, you can already start to see how each text prioritizes different emotional and narrative elements.

SECTION 3 Findings, Interpretation, and Course Integration
3.1 Expectations vs Computational Findings

Going into this project, we expected the canonical novels to feel more emotionally balanced and the fanfiction texts to push emotional extremes, especially in romance and conflict. That assumption came from what we already know about fanfiction culture.

For the most part, the data backed this up. Next Gen and Reconstructing HP show disproportionately high levels of love, while Wishmaster Harry Potter shows dense clusters of fear, anger, and death related language.

However, one of the more interesting surprises was just how steady the emotional pacing is in the canonical novels. Even during intense moments, Half Blood Prince and Prisoner of Azkaban maintain relatively smooth distributions. That level of consistency likely reflects professional editorial structuring.The Voyant Trends and Bubblelines visualizations both show that the canonical novels maintain much steadier emotional pacing than the fanfiction texts. In Half Blood Prince and Prisoner of Azkaban, the lines for love, fear, anger, and hope remain relatively flat across the narrative, with no dramatic spikes. The Bubblelines view reinforces this pattern, emotional terms appear in smaller, evenly spaced clusters rather than the dense bursts seen in the fanfiction works. This consistency suggests a more controlled emotional structure, likely shaped by professional editing and narrative planning.

 
![Distinctive Words Screenshot](/assets/images/image1.png)


Figure 5. Distinctive words across the five text corpus, showing the terms that appear unusually frequently in each document compared to the rest of the dataset.

At the same time, the distinctive word patterns revealed how fanfiction shifts the emotional center of the narrative by elevating side characters who barely register in the original series. While Rowling’s texts foreground predictable anchors like Dumbledore, Slughorn, and Buckbeak, the fanfiction works highlight names such as Teddy, Victoire, Greg, and even Skullhammer. These choices signal a move toward more intimate, character driven storytelling, opening emotional space that the canonical novels leave unexplored and helping explain why the fan texts show sharper spikes in love, conflict, and interpersonal tension.

3.2 What Computational Analysis Reveals That Close Reading Cannot

Realistically, reading all five texts cover to cover within the project timeline would have been overwhelming. More importantly, even a full close reading would not allow us to measure emotional frequency with this level of precision.
Computational analysis made it possible to:
Locate emotional spikes across each narrative
Track which characters cluster with which emotions
Compare canon and fanfiction at scale
Detect cross text emotional signatures
These patterns only really become visible when you zoom out and treat the texts as data. In that sense, distant reading did not replace interpretation; it just gave us a much wider lens.

3.3 Voyant vs R Complementary Strengths

Working with both Voyant and R made their differences very clear. Voyant is great for quick exploration. The interactive interface makes it easy to notice patterns you were not even looking for.
R, on the other hand, is much better for precision and customization. Building the heatmap and color coded word cloud gave us far more control over exactly what we wanted to track. Using both together ultimately gave us the clearest picture. Voyant helped us discover patterns, R helped us present them more intentionally.

3.4 Methodological Reflection The Risks of Distant Reading

Ted Underwood’s chapter, The Risks of Distant Reading, was important for grounding our approach. Underwood warns that quantitative analysis can create what he calls an "illusory aura of objectivity," which can make scholars forget that literature is still an interpretive and emotional experience.
We kept that warning in mind throughout this project. Our goal was never to treat word frequency as the final answer. Instead, the visualizations acted more like signals pointing us toward places worth examining more closely.

For example, noticing the fear spikes in Wishmaster pushed us to revisit specific passages to understand how the author builds tension. The numbers showed us where to look, but interpretation still required human reading.

Underwood’s broader point still stands. Distant reading can reveal patterns, but it cannot fully capture why literature feels meaningful. That emotional layer still depends on close reading.

3.5 Additional Course Connections

Glyndark’s essay, "People Don’t Read, But LLMs Do," helped reinforce why computational methods matter in the first place. The piece argues that machines can process textual scale far beyond human capacity, which directly supports the kind of large corpus work we attempted here.

At the same time, our findings also echo Underwood’s caution. Scale is powerful, but only when it stays connected to interpretation. The most productive approach is not choosing between distant and close reading, but letting them work together.
SECTION 4 Conclusion

Overall, this project shows how computational methods can make emotional patterns visible across large literary datasets in ways that traditional reading alone cannot. By combining Voyant Tools with R visualizations, we were able to identify clear emotional differences between canonical Harry Potter texts and fanfiction, track emotional movement across narratives, and map how emotions cluster around key characters.

At the same time, following Underwood’s warning, we recognize that numbers alone cannot explain why these stories resonate emotionally. Distant reading works best as a guide, something that helps us notice patterns we might otherwise miss. In the end, the goal is not to replace close reading, but to deepen it.

Collaboration Statement

This project was completed collaboratively by Mouza and Meera. We divided the work evenly both partners contributed to corpus selection, Voyant analysis, R based visualizations, and the written synthesis. Mouza focused primarily on the R heatmap, the Bubblelines interpretation, and drafting Section 2, while Meera focused on the word cloud, the bar chart analysis, and integrating course readings. We reviewed and edited all sections together to ensure a unified final submission.

Works Cited
Underwood, Ted. Distant Horizons: Digital Evidence and Literary Change. University of Chicago Press, 2019, pp. 143–170.

Glyndark, Glynn. "People Don’t Read, But LLMs Do." Glyndark Blog, 2023, https://blog.glyndarkin.co.uk/ai/people-dont-read-but-ll-ms-do/.

"Fan Fiction." Wikipedia: The Free Encyclopedia, Wikimedia Foundation, 2026, https://en.wikipedia.org/wiki/Fan_fiction.


