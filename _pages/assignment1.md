---
layout: page
title: Assignment 1: Emotional Extremes in the Wizarding World
permalink: /assignments/assignment1/
---

# Emotional Extremes in the Wizarding World: A Computational Study of Canon and Fanfiction

## SECTION 1 Corpus and Research Questions

If there is one thing the Harry Potter universe does extremely well, it is emotion. Fear, loyalty, grief, anger; everything in this world feels just slightly heightened. Because of that, we started with a simple curiosity: does the language actually reflect that emotional intensity, and does fanfiction push it even further?
To explore this, we assembled a mixed corpus of five texts drawn from both the official Harry Potter series and popular fanfiction communities. Altogether, the corpus contains 441,225 total words and 18,063 unique word forms, which gave us more than enough material to work with. The longest texts are Harry Potter and the Half Blood Prince (171,668 words) and the fanfiction Wishmaster Harry Potter (107,373 words), while the shortest are Reconstructing HP (23,880 words) and HP Next Gen (33,391 words). This range actually worked in our favor because it let us compare emotional language across long canonical novels and shorter, more experimental fan works.

![Image 1](/assets/images/image1.png)

We chose this corpus very intentionally. The Harry Potter storyline is built on emotional stakes, and fanfiction communities are known for amplifying those stakes even more, especially when it comes to romance and interpersonal conflict. That made this dataset a really good test case for tracking how emotional language shifts across authors and contexts.

Our analysis is guided by three main questions:

* What emotions appear most strongly across the texts?
* How do emotional patterns shift throughout each narrative?
* How does emotional language cluster around key characters?

Rather than replacing close reading, our goal was to use computational tools to zoom out and notice patterns that would be almost impossible to track manually.

## SECTION 1.5 Background Research and Contextualization

Before jumping into the visualizations, we needed to understand the context behind the texts themselves. The two canonical novels in our dataset, Harry Potter and the Half Blood Prince (2005) and Harry Potter and the Prisoner of Azkaban (1999), were written by J. K. Rowling and published through major commercial presses such as Bloomsbury and Scholastic. These books went through heavy editorial processes and were written for a massive global audience. Because of that, we expected them to show more stylistic control and more balanced emotional pacing.

The three fanfiction texts, Wishmaster Harry Potter, HP Next Gen, and Reconstructing HP, come from a completely different ecosystem. They were published online within participatory fan communities. As the Wikipedia article on fan fiction explains, this space encourages transformative storytelling, emotional experimentation, and far fewer constraints than traditional publishing.

Going into the analysis, we honestly expected fanfiction to be more emotionally dramatic, especially in categories like love and conflict. At the same time, we assumed the canonical novels would show smoother emotional pacing. As the analysis shows, many of these assumptions were correct, but not all of them.

## SECTION 2 Exploratory Analysis

To explore emotional patterns across the corpus, we combined Voyant Tools with R based analysis in Posit Cloud. Voyant helped us quickly explore large patterns, while R gave us more control to build targeted visualizations. Using both ended up being much more useful than relying on just one method.

### 2.1 Word Frequency and Emotional Distribution (Voyant Tools)

Our first step was to look at the overall emotional vocabulary across the five texts. Using Voyant’s Terms and Trends tools, we tracked four core emotion words: love, hope, fear, and anger.

Embedded code:

<!-- Exported from Voyant Tools (voyant-tools.org). -->
<iframe style='width: 100%; height: 800px;' src='https://voyant-tools.org/?view=Trends&corpus=a815ebe65cb4c2b0801510d2473dace2'></iframe>

Figure 1. Relative frequencies of four emotion terms across the five texts.

### 2.2 Emotional Trends Across Narrative Segments (Voyant Bubblelines)

Next, we wanted to see how emotions move across the timeline of each story. For this, we used Voyant’s Bubblelines tool, which shows where emotional keywords cluster throughout the narrative.

Embedded code:

<!-- Exported from Voyant Tools (voyant-tools.org). -->
<iframe style='width: 100%; height: 800px;' src='https://voyant-tools.org/?view=Bubblelines&corpus=a815ebe65cb4c2b0801510d2473dace2'></iframe>

Figure 2. Bubblelines visualization showing the distribution of emotional keywords across all five texts.

### 2.3 Character Centered Emotional Patterns (Heatmap in Voyant)

After exploring broad trends, we used Voyant to look more closely at how emotional language clusters around specific characters. We built a heatmap tracking the frequency of key terms harry, ron, hermione, love, hope, fear, anger, and dead.

![Image 2](/assets/images/image2.png)

Figure 3. Heatmap showing the frequency of character and emotion terms across selected texts.

### 2.4 Cross Text Comparison (Color Coded Word Cloud in R)

To step back and look at stylistic differences more broadly, we created a color coded word cloud in R. Each word is colored according to the text where it appears most frequently.

![Image 3](/assets/images/image3.png)

Figure 4. Color coded word cloud showing dominant vocabulary across five texts.

## SECTION 3 Findings, Interpretation, and Course Integration

## SECTION 4 Conclusion

This project shows how computational methods can make emotional patterns visible across large literary datasets in ways that traditional reading alone cannot. By combining Voyant Tools with R visualizations, we were able to identify clear emotional differences between canonical Harry Potter texts and fanfiction, track emotional movement across narratives, and map how emotions cluster around key characters.

### Collaboration Statement
This project was completed collaboratively by Mouza and Meera.

### Works Cited
Underwood, Ted. Distant Horizons: Digital Evidence and Literary Change. University of Chicago Press, 2019.
Glyndark, Glynn. "People Don’t Read, But LLMs Do." Glyndark Blog, 2023.
