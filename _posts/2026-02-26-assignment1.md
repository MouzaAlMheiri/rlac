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

To explore this, we assembled a corpus of five texts from both the official Harry Potter series and popular fanfiction communities. The corpus contains 441,225 words and 18,063 unique word forms, giving us ample material for analysis. The longest texts are Harry Potter and the Half-Blood Prince (171,668 words) and the fanfiction Wishmaster Harry Potter (107,373 words ), while the shortest are Reconstructing HP (23,880 words) and HP Next Gen (33,391 words). This range allowed us to compare emotional language across long canonical novels and shorter, more experimental fan works.


We chose this corpus because the Harry Potter series is built on strong emotional stakes, and fanfiction often amplifies those emotions, especially in romance and conflict. This made the dataset an ideal case for examining how emotional language shifts across authors and contexts.
 
Our analysis is guided by three main questions:
What emotions appear most strongly across the texts?
How do emotional patterns shift throughout each narrative?
How does emotional language cluster around key characters?


Rather than replacing close reading, our goal was to use computational tools to zoom out and notice patterns that would be almost impossible to track manually.

SECTION 1.5 Background Research and Contextualization

Before analyzing the visualizations, we reviewed the context of the texts. The canonical novels—Half-Blood Prince (2005) and Prisoner of Azkaban (1999) were written by J. K. Rowling and published through major presses, meaning they underwent extensive editing and were designed for a global audience. Because of this, we expected them to show greater stylistic control and more balanced emotional pacing.


The three fanfiction texts Wishmaster Harry Potter, HP Next Gen, and Reconstructing HP, come from a different ecosystem, published online within participatory fan communities. This space encourages transformative storytelling, emotional experimentation, and far fewer constraints than traditional publishing.

We expected fanfiction to be more emotionally dramatic, especially in love and conflict, and assumed the canonical novels would show smoother emotional pacing. Many of these assumptions proved correct, though not all.

SECTION 2 Exploratory Analysis

To explore emotional patterns across the corpus, we combined Voyant Tools with R based analysis in Posit Cloud. Voyant helped us quickly explore large patterns, while R gave us more control to build targeted visualizations. Using both ended up being much more useful than relying on just one method.

2.1 Word Frequency and Emotional Distribution (Voyant Tools)
	
Our first step was to examine the emotional vocabulary across the five texts. Using Voyant’s Terms and Trends tools, we tracked four core emotion words: love, hope, fear, and anger.

<!--	Exported from Voyant Tools (voyant-tools.org).
The iframe src attribute below uses a relative protocol to better function with both
http and https sites, but if you're embedding this into a local web page (file protocol)
you should add an explicit protocol (https if you're using voyant-tools.org, otherwise
it depends on this server.
Feel free to change the height and width values or other styling below: -->
<iframe style='width: 487px; height: 424px;' src='https://voyant-tools.org/tool/Trends/?query=fear*&query=anger*&query=love*&query=hope*&chartType=bar&corpus=e40520433e43902aa62d6a292a0c92b4'></iframe>

Figure 1. Relative frequencies of four emotion terms across the five texts.

Clear patterns emerged immediately. The fanfiction texts especially HP Next Gen and Reconstructing HP show much higher frequencies of love, which the visualization made especially clear.

In contrast, the canonical novels show a more balanced emotional distribution, with no single emotion dominating.

Wishmaster Harry Potter stood out for its elevated levels of fear and anger, giving it a distinctly darker emotional profile. The visualization confirmed that each text carries its own emotional fingerprint.

2.2 Emotional Trends Across Narrative Segments (Voyant Bubblelines)

Next, we examined how emotions shift across each narrative using Voyant’s Bubblelines tool, which visualizes where emotional keywords cluster over the narratives.

<!--	Exported from Voyant Tools (voyant-tools.org).
The iframe src attribute below uses a relative protocol to better function with both
http and https sites, but if you're embedding this into a local web page (file protocol)
you should add an explicit protocol (https if you're using voyant-tools.org, otherwise
it depends on this server.
Feel free to change the height and width values or other styling below: -->
<iframe style='width: 733px; height: 518px;' src='https://voyant-tools.org/tool/Bubblelines/?bins=30&query=harry&query=ron&query=hermione&query=fear&query=love&query=hope&query=death&query=anger*&query=love*&query=hope*&query=fear*&query=death*&docId=77a994e537fa1549ef98f1518408350f&docId=e5b620d91aa973a5d063bfd6e682c913&docId=eef7c2aed7bfbc541120b68169d35fd4&docId=257be3303058857b50d93346c98d8d6f&docId=e76bd1088397aa9f0d9c1a4adf43ea11&corpus=e40520433e43902aa62d6a292a0c92b4'></iframe>

Figure 2. Bubblelines visualization showing the distribution of emotional keywords across all five texts.

What became obvious is Wishmaster Harry Potter shows dense clusters of fear, anger, and death related language. These appear in bursts rather than evenly, creating a more volatile emotional rhythm.

In contrast, Half Blood Prince and Prisoner of Azkaban display smoother emotional distribution, supporting the idea that Rowling’s narrative structure maintains more controlled emotional pacing.

We were surprised that the shorter fanfictions did not spike constantly, instead, they concentrate emotional language around relationship heavy moments. The intensity is still present, but more strategically placed than expected.

We also found that emotional terms often rise and fall alongside character mentions. In the fanfictions, names like Harry, Ron, and Hermione appear during tense moments, which explains the tight clustering of fear and anger around those sections. The canonical novels show a steadier relationship between character presence and emotional language, suggesting a more deliberate balance between plot and character driven emotion. This contrast highlights how fanfiction amplifies emotional extremes, while Rowling’s texts maintain a more even emotional flow.

2.3 Character Centered Emotional Patterns (Heatmap in Cloud R)

After exploring broad trends, we used to Cloud R to look more closely at how emotional language clusters around specific characters. We built a heatmap tracking the frequency of key terms harry, ron, hermione, love, hope, fear, anger, and dead.

We included dead/death because mortality is a central emotional and narrative force in both the Harry Potter series and its fanfiction adaptations. Unlike broad emotions such as love, fear, or anger, death functions as a plot‑defining event that triggers intense reactions. Tracking this term showed where moments of loss or threat cluster around characters like Harry, Ron, and Hermione, and highlighted how fanfiction often amplifies darker themes Half‑Blood Prince and Wishmaster Harry Potter show especially high concentrations of death‑related language. Including dead/death alongside the core emotions gave the heatmap a fuller picture of how both canon and fanfiction use mortality to shape emotional intensity, and we noticed that spikes in death‑related terms often coincided with increases in emotional language in the Rowling novels.

<img src="{{ '/assets/images/image2.jpg' | relative_url }}" alt="Color-coded word cloud">

Figure 3. Heatmap showing the frequency of character and emotion terms across selected texts.

Several patterns stood out. Harry dominates the corpus, which is expected narratively but more striking when visualized. Ron’s presence varies widely he appears heavily in the Ron centered fanfiction but far less in Wishmaster, showing how fanfiction redistributes character focus. Love peaks sharply in Next Gen, supporting the idea that fanfiction amplifies romantic themes and shifts attention to different characters. Meanwhile, fear and anger appear consistently across darker fanfics and the canonical novels, reinforcing Harry’s long standing association with danger and conflict.

The heatmap revealed how emotional language organizes itself around specific characters patterns that would be difficult to quantify through close reading alone.

2.4 Cross Text Comparison (Color Coded Word Cloud in R)

To step back and look at stylistic differences more broadly, we created a color coded word cloud in R. Each word is colored according to the text where it appears most frequently.

<img src="{{ '/assets/images/image3.jpg' | relative_url }}" alt="Color-coded word cloud">

<!-- <img src="assets/images/image3.jpg" alt="Color-coded word cloud"> -->


Figure 4. Color coded word cloud showing dominant vocabulary across five texts.

The differences are clear at a glance Next Gen leans into family and relationship vocabulary, Wishmaster foregrounds darker, conflict driven language, and the canonical texts emphasize dialogue heavy terms like said, wand, and Dumbledore. The visualization highlights these thematic clusters instantly, showing how each text prioritizes different emotional and narrative elements.


SECTION 3 Findings, Interpretation, and Course Integration
3.1 Expectations vs Computational Findings


We expected the canonical novels to show more balanced emotional pacing and the fanfiction texts to push emotional extremes, especially in romance and conflict assumptions based on common patterns in fanfiction culture.

For the most part, the data backed this up. Next Gen and Reconstructing HP show disproportionately high levels of love, while Wishmaster Harry Potter shows dense clusters of fear, anger, and death related language.

One surprising finding was how steady the emotional pacing is in the canonical novels. Even during intense moments, Half‑Blood Prince and Prisoner of Azkaban maintain smooth emotional distributions. Both the Voyant Trends and Bubblelines visualizations show relatively flat lines for love, fear, anger, and hope, with small, evenly spaced clusters rather than the sharp bursts seen in the fanfiction texts. This consistency suggests a more controlled emotional structure shaped by professional editing and narrative planning.

 
<img src="{{ '/assets/images/image1.jpg' | relative_url }}" alt="Color-coded word cloud">

Figure 5. Distinctive words across the five text corpus, showing the terms that appear unusually frequently in each document compared to the rest of the dataset.

Distinctive words reveal that fanfiction shifts the emotional center by elevating side characters who barely appear in the original series. While Rowling foregrounds figures like Dumbledore, Slughorn, and Buckbeak, the fanfiction texts highlight characters such as Teddy, Victoire, Greg, and Skullhammer. This shift creates more intimate, character‑driven storytelling and helps explain the sharper spikes in love, conflict, and interpersonal tension.

3.2 What Computational Analysis Reveals That Close Reading Cannot

Reading all five texts closely would have been unrealistic, even a full close reading could not measure emotional frequency with this precision. Computational analysis let us locate emotional spikes, track which characters cluster with which emotions, compare canon and fanfiction at scale, and detect cross‑text emotional signatures. These patterns only appear when treating the texts as data; distant reading expands our lens rather than replacing interpretation.

3.3 Voyant vs R Complementary Strengths

Using both Voyant and R highlighted their complementary strengths. Voyant is ideal for quick exploration and noticing unexpected patterns, while R offers precision and customization, especially for the heatmap and color coded word cloud. Together, they provided the clearest overall picture Voyant helped us discover patterns, and R allowed us to present them more intentionally.

3.4 Methodological Reflection The Risks of Distant Reading

Ted Underwood’s The Risks of Distant Reading grounded our approach by warning that quantitative analysis can create an “illusory aura of objectivity,” obscuring the interpretive and emotional nature of literature. We kept this in mind by treating word frequency as a signal rather than a conclusion. For example, spikes in fear in Wishmaster led us back to specific passages to understand how tension was built the numbers showed where to look, but interpretation still required human reading. Distant reading reveals patterns, but it cannot explain why literature feels meaningful that layer still depends on close reading.

3.5 Additional Course Connections

Glyndark’s essay, People Don’t Read, But LLMs Do, reinforces the value of computational methods by showing how machines process textual scale far beyond human capacity directly supporting the large corpus work we attempted.

Our findings also echo Underwood’s caution: scale is powerful only when paired with interpretation. The most effective approach is combining distant and close reading rather than choosing between them.

SECTION 4 Conclusion

This project shows how computational methods reveal emotional patterns across large literary datasets in ways traditional reading cannot. Using Voyant Tools and R, we identified emotional differences between canon and fanfiction, tracked emotional movement across narratives, and mapped how emotions cluster around key characters.

Following Underwood’s warning, we recognize that numbers alone cannot explain why these stories resonate. Distant reading works best as a guide that highlights patterns we might miss, deepening rather than replacing close reading.

Collaboration Statement

This project was completed collaboratively by Mouza and Meera. We divided the work evenly: both contributed to corpus selection, Voyant analysis, R visualizations, and writing. Mouza focused on the R heatmap, Bubblelines interpretation, and drafting Section 2, while Meera worked on the word cloud, bar chart analysis, and integrating course readings. We reviewed all sections together for a unified final submission.

Works Cited

Underwood, Ted. Distant Horizons: Digital Evidence and Literary Change. University of Chicago Press, 2019, pp. 143–170.

Glyndark, Glynn. "People Don’t Read, But LLMs Do." Glyndark Blog, 2023, https://blog.glyndarkin.co.uk/ai/people-dont-read-but-ll-ms-do/.

"Fan Fiction." Wikipedia: The Free Encyclopedia, Wikimedia Foundation, 2026, https://en.wikipedia.org/wiki/Fan_fiction.


ALL DONE READY FOR GRADING


