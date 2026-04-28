---
title: "Assignment2"
last_modified_at: 2016-03-09T16:20:02-05:00
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---

Computational Analysis of Sci-Fi Corpus

Corpus Background and Expectations

Before starting this assignment, we already had some experience with science fiction from earlier introductory classes. We had read texts like Frankenstein, which showed us how the genre often mixes real scientific ideas with imaginative possibilities. From those earlier readings, we understood science fiction as a place where writers test the limits of reality by asking “what if” and exploring how science, technology, or unfamiliar environments might reshape human life. We also knew that speculative fiction often questions the world by imagining alternative futures or new scientific outcomes.

However, we had never worked with a full corpus of science fiction texts or analyzed them using computational tools. This corpus gave us a new way to see patterns that are difficult to notice through close reading alone.
The texts in the corpus are not all the same length. Some works are short magazine-style stories, especially those by Philip K. Dick, which move quickly and use tighter, more repetitive vocabulary. Others, such as Andre Norton’s Plague Ship and Star Hunter, are longer and read more like full adventure novellas, with more world-building and slower pacing. These differences in length and structure led us to expect that computational methods might treat the texts differently, since longer works naturally include more variation in vocabulary while shorter ones repeat certain words more often.

Author Style and Thematic Differences

The writers in this corpus approach science fiction in very different ways. Andre Norton writes in a straightforward and immersive style, focusing on survival, exploration, and adventure. Her works feel structured and consistent, with strong world-building. Her style is closest to Leigh Brackett, who also writes fast-moving adventure stories, though Brackett adds a more atmospheric, almost noir tone to her planetary settings.
Some authors blend science fiction with fantasy elements. Marion Zimmer Bradley is a clear example, writing about psychic abilities, alien social hierarchies, and emotional, character-driven conflicts, which creates a softer and more mystical tone. Henry Kuttner also mixes genres, combining science fiction with horror or humor depending on the story.
Philip K. Dick writes in a very direct, idea-focused style centered on paranoia, unstable realities, and psychological tension. H.G. Wells stands apart with a more formal, descriptive, and philosophical voice, especially in his nonfiction.
These differences in tone, pacing, and thematic focus led us to expect that the computational methods would separate the authors in distinct ways.

Close Reading and Initial Impressions

As part of our process, we close-read one of the texts during a class exercise, focusing on Andre Norton’s writing. This helped us understand her style more closely before analyzing the computational results. Reading her work directly showed how straightforward and adventure-driven her storytelling is, especially her focus on survival and world-building.
We also looked at Goodreads reviews of her books to understand how general readers describe her writing. Combining our own impressions from close reading with public responses helped us build a clearer understanding of her style before comparing it to the patterns we later saw in the computational analysis.

Thematic Range of the Corpus

The corpus contains a wide range of themes because each author approaches science fiction differently. Some writers focus on adventure and survival, particularly Andre Norton, who emphasizes exploration and the challenges of unknown worlds. Leigh Brackett combines adventure with planetary romance, lost civilizations, and colonial tensions.
Other authors blend science fiction with fantasy elements. Marion Zimmer Bradley focuses on psychic abilities, alien social hierarchies, and emotional conflicts. Philip K. Dick explores paranoia, unstable realities, and the effects of war and technology on identity. H.G. Wells introduces futuristic speculation and social commentary, especially in his nonfiction. Henry Kuttner mixes science fiction with horror or humor depending on the story.
Overall, the corpus shows a wide range of themes, from adventure and survival to psychology, politics, fantasy, and social critique. Even though all texts fall under science fiction, each author brings different interests and approaches, creating a diverse thematic landscape.

Bootstrap Consensus Tree (Stylo)
<img src="{{ '/assets/images/imageA.jpg' | relative_url }}" alt="Color-coded word cloud">
<!-- <img src="assets/images/imageA.jpg" alt="Color-coded word cloud"> -->

The Bootstrap Consensus Tree helps us understand stylistic similarities between authors. This method groups texts based on writing style rather than content, because it relies on function words such as “the,” “and,” “of,” and “to.” These words are used by all writers, but in different patterns, revealing pacing, sentence structure, and stylistic habits.
In our tree, Andre Norton’s texts cluster together because her writing is consistent and adventure-driven. H.G. Wells separates from the others due to his more formal and descriptive style. Marion Zimmer Bradley also stands apart because of her blend of science fiction and fantasy with an emotional tone. Leigh Brackett and Henry Kuttner sometimes cluster closer together, likely because they share similar pulp-style pacing.
We understood these patterns by researching each author’s style and connecting those findings to what we saw visually. This confirms that Stylo focuses on how authors write, not what they write about.

PCA Scatterplot (1000 MFW)

<!-- <img src="assets/images/imageB.jpg" alt="Color-coded word cloud"> -->

The PCA scatterplot using 1000 most frequent words gives the clearest view of thematic separation. Because it includes more content words, the clusters become stronger and easier to interpret.
Norton’s adventure-focused stories cluster together due to shared vocabulary related to survival and exploration. Wells separates because his texts use more political and philosophical language. Marion Zimmer Bradley forms her own cluster due to fantasy-driven vocabulary such as “telepathy,” “culture,” and “hierarchy.” Philip K. Dick also forms a distinct group due to vocabulary related to paranoia, war, and technology.
This PCA highlights thematic differences and shows how authors diverge based on what they write about, complementing Stylo’s focus on style.

PCA Scatterplot (200 MFW) and Early Thematic Drift

<!-- <img src="assets/images/imageC.jpg" alt="Color-coded word cloud"> -->

The 200 MFW PCA is more crowded, but still reveals meaningful patterns. Words like “eyes,” “turn,” “away,” “came,” “dark,” “face,” and “behind” cluster together, suggesting descriptive or action-based language. Another group includes “before,” “not,” “yet,” “men,” “between,” and “set,” which feels more structural or narrative.

At the center, we observed common words such as “place,” “most,” “year,” “good,” “want,” and “little,” which makes sense because PCA pulls frequent, neutral words toward the middle.

We also saw early author separation. Wells’ The Salvaging of Civilization appears far to the left, showing strong thematic difference. Zimmer Bradley’s Jackie is isolated on the right. Norton’s texts cluster tightly together, as do Brackett’s. There is also a small pairing between Kuttner’s The Ego Machine and Dick’s The Defenders, suggesting some shared vocabulary.

Even though the visualization is dense, it clearly shows early thematic drift and demonstrates how PCA moves from style toward content.

Comparing Stylo and PCA

When comparing both methods, we see that they analyze the corpus in different ways. Stylo focuses on writing style through function words, grouping authors based on pacing and structure. PCA focuses on content words, separating authors based on themes and vocabulary.

This reflects Ted Underwood’s argument that distant reading depends on modeling relationships rather than simply counting words. As he explains, numbers help “establish comparative relationships between different parts of the historical record”.

Using both methods together allowed us to see both stylistic similarity and thematic diversity across the texts.

Computational Insights and Word Patterns

The computational analysis showed that science fiction authors cluster together not only by theme but also by shared vocabulary patterns we did not expect. Authors like Norton, Brackett, and Dick share descriptive language that creates tighter clusters in PCA.

This supports Ted Underwood’s idea that distant reading reveals “patterns shared by many other books” when we zoom out.
Stylo’s wordlist is dominated by function words, while PCA highlights distinctive content words such as “dark,” “face,” “behind,” “before,” “yet,” and “between.” These words drive thematic separation.

We also observed that changing the number of most frequent words changes the PCA results. With fewer words, clusters are less stable. With more words, separation becomes clearer. This reflects Underwood’s point that models “learn concepts entirely from illustrative examples” 

Differences Between Methods and Clustering Behavior

Gender did not produce stable clustering patterns. Writers of different genders were mixed across both methods. This aligns with Underwood’s observation that gender signals in fiction are “extremely volatile” 

Themes, however, did produce stable clusters. Authors with similar topics clustered together more consistently.
A clear disagreement appears with Zimmer Bradley’s Jackie. In Stylo, she clusters closer to others because her function-word usage is similar. In PCA, she is strongly separated due to her distinct thematic vocabulary. This difference highlights how Stylo measures style while PCA measures content.

Comparative Insights Across Methods

Both methods reveal patterns of similarity, but in different ways. Stylo produces clear hierarchical groupings, while PCA shows spatial separation and drift between texts.

Some patterns remain consistent. Norton’s texts cluster together in both methods, and Brackett’s texts also remain close. However, PCA shows more spread and thematic separation, while Stylo keeps authors tighter due to its focus on style.

This confirms that Stylo is effective for detecting stylistic similarity, while PCA is better for detecting thematic relationships. Our results align with Underwood’s argument that distant reading reveals patterns across many texts.

Trends, Surprises, and Reader Engagement

One of the biggest surprises was how differently the same texts behaved across methods. Authors who clustered closely in Stylo became more separated in PCA due to differences in content words.

Zimmer Bradley’s separation in PCA was especially unexpected, since she blends in stylistically in Stylo. This showed how strongly theme can influence clustering.

The analysis also made us more curious about specific texts. Wells’ The Salvaging of Civilization stood out due to its separation, making us want to understand what makes its vocabulary so different.

LLMs, Style, and Generated Texts

Although we did not complete the bonus task, we expect that an LLM-generated text would cluster closer to the original author in Stylo than in PCA. Stylo focuses on function-word patterns, which LLMs replicate well. PCA relies on distinctive content words, which LLMs may generalize or flatten.
The LLM appears to understand surface-level stylistic habits, such as sentence rhythm and pacing. This reflects Underwood’s idea that models “learn concepts entirely from illustrative examples”. While LLMs can mimic style, they do not fully capture deeper thematic structures.

Style, Content, and Interpretation

Our results suggest that style and content are not fully separable. Even when methods aim to isolate one, traces of the other remain. Stylo clusters sometimes hint at thematic similarity, and PCA groupings can reflect stylistic tendencies.
As Underwood explains, when we zoom out, “details… organize themselves into larger patterns shared by many other books.” This matches what we observed: style and content are always intertwined.

Science Fiction, History, and Cold War Context

The corpus, largely from the 1950s, reflects strong thematic consistency. Even before close reading, the PCA vocabulary suggested tension, fear, and uncertainty. Considering the post–World War II and Cold War context, this makes sense.
These texts respond to historical anxieties such as invasion, nuclear threat, and rapid technological change. At the same time, they provide a form of escape. Science fiction allows these fears to be explored indirectly through imagined worlds.
As Underwood notes, fiction often moves “farther away from the language, themes, and narrative strategies of nonfiction,” which explains how sci-fi transforms real-world fears into speculative narratives.

Reading Like a Computer

Working with computational tools required developing a new kind of literacy. Instead of focusing only on sentences and meaning, we had to interpret patterns, clusters, and relationships.
This aligns with Ted Underwood’s idea that numbers help us “establish comparative relationships.” Reading like a computer involves understanding how models work, how data is processed, and how patterns are formed.
This approach does not replace traditional reading but expands it, allowing us to analyze literature at a larger scale.

Conclusion

Using both Stylo and PCA allowed us to analyze the corpus from two perspectives. Stylo revealed stylistic habits through function words, while PCA revealed thematic differences through content words.
Together, these methods provided a more complete understanding of the texts, showing both consistency and diversity across science fiction writing.

Collaboration Statement

This project was completed collaboratively by Meera and Mouza. Mouza focused on producing and organizing the computational outputs and visualizations, while Meera focused on analyzing the results and interpreting the patterns. Both of us worked together on refining the final write-up, polishing the structure and language, and developing the overall conclusions together.

Works Cited


Primary Corpus


Brackett, Leigh. The Blue Behemoth. 1943.

Brackett, Leigh. Enchantress of Venus. 1949.

Brackett, Leigh. Black Amazon of Mars. 1951.

Dick, Philip K. Second Variety. 1953.

Dick, Philip K. The Defenders. 1953.

Dick, Philip K. The Variable Man. 1953.

Bloch, Robert, and Henry Kuttner. The Black Kiss. 1937.

Kuttner, Henry. The Ego Machine. 1952.

Kuttner, Henry. Thunder in the Void. 1942.

Norton, Andre. Plague Ship. 1956.

Norton, Andre. Star Hunter. 1961.

Norton, Andre. Voodoo Planet. 1959.

Wells, H. G. The Island of Doctor Moreau. 1896.

Wells, H. G. The Salvaging of Civilization. 1921.

Wells, H. G. The War of the Worlds. 1898.

Bradley, Marion Zimmer. Falcons of Narabedla. 1957.

Bradley, Marion Zimmer. Jackie Sees a Star. 1954.

Bradley, Marion Zimmer. The Door Through Space. 1961.


Secondary Source

Underwood, Ted. Distant Horizons: Digital Evidence and Literary Change. University of Chicago Press, 2019.


READY FOR GRADING
