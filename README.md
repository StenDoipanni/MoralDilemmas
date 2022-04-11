# Uncovering Values: Detecting Latent Moral Content from Natural Language with Explainable and Non-Trained Methods

### Table of contents
* [General Information](#general-information)
* [Data and Theoretical Background](data)
* [Details](#details)

### General Information
Moral values as commonsense norms shape our everyday individual and community behavior. The possibility to extract moral attitude rapidly from natural language is an appealing perspective that would enable a deeper understanding of social interaction dynamics and the individual cognitive and behavioral dimension. In this work we focus on detecting moral content from natural language and we test our methods on a corpus of tweets previously labeled as containing moral values or violations, according to Moral Foundation Theory. We develop and compare two different approaches: (i) a frame-based symbolic value detector based on knowledge graphs and (ii) a zero-shot machine learning model fine-tuned on a task of Natural Language Inference (NLI) and a task of emotion detection. 

### Data and Theoretical Background
Our work solely focuses on Haidt’s Moral Foundation Theory ([MFT](https://moralfoundations.org/)). MFT is grounded on the idea that, while morality could vary widely in its extension (for example, what is considered a harmful or caring behavior depends on geographical, temporal, cultural and many others dimensions), its intension presents some recurring patterns that allow to delineate a psychological system of “intuitive ethics”.
At the core of MFT there are six dyads of values and violations: 
• Care / Harm: a caring versus harming behavior, it grounds virtues of gentleness, kindness and nurturance. 
• Fairness / Cheating: this foundation is based on social cooperation and typical nonzerosum game theoretical situations based on reciprocal altruism. It underlies ideas of justice, rights and autonomy. 
• Loyalty / Betrayal: this dyad is based on the positive outcome coming from cohesive coalition, and the ostracism towards traitors.
• Authority / Subversion: social interactions in terms of societal hierarchies, it underlies ideas.

To examine the effectiveness of our approaches in the moral value detection task, we focus on the challenge of recognizing them in the Moral Foundation Twitter Corpus ([MFTC](https://journals.sagepub.com/doi/full/10.1177/1948550619876629)). The dataset, consisting of 35k tweets, is organized into seven distinct thematic topics covering a wide range of moral concerns. Each tweet is labeled from three to eight different annotators trained to detect and categorize texts following the guidelines outlined by Moral Foundation Theory. The MFTC includes ten different moral value categories, as well as a label for textual material that does not evoke a morally meaningful response. To account for their semantic independence, each tweet in the corpus was annotated with both values and violations.


### Details
- The [Zero-shot](https://github.com/StenDoipanni/MoralDilemmas/blob/main/Zero-shot.xlsx) file shows results of the Zero-shot method. Through the application of this methodology we verify how much each value in the Moral Foudation Theory set is semantically correlated to each tweet in the test set (i.e. we evaluate if the concept "cure" is expressed in the text "Commitment to peace, healing and love of neighbor . Give us strength and patience. ").
- The [Emotion-zero-shot](https://github.com/StenDoipanni/MoralDilemmas/blob/main/Emotion-zero-shot.xlsx) file shows results of the Zero-shot method with the addition of the emotional component of the sentence (for example, given the tweet “Peace, Love And Unity <3” represented as a premise, we add to this text both (i) an emotion perception component such as “This sentence is about joy sentiment.” and (ii) an information about its polarity “This is positive.”).
- The [Emotion-zero-shot+](https://github.com/StenDoipanni/MoralDilemmas/blob/main/Emotion-zero-shot%2B.xlsx) file shows results of the joined Zero-shot method and Emotion-zero-shot method.
- The [Random](https://github.com/StenDoipanni/MoralDilemmas/blob/main/random.xlsx) file shows results from the Random method. Given the lack of a reasonable state-of-the-art baseline of non-trained systems, we report a Random lower-bound, obtained by predicting each label with a probability corresponding to the fraction of entries in the ground truth represented by the test set with that label.

For privacy reasons, validated tweets are indicated by the corresponding original ID. For more information, see the [MFTC](https://journals.sagepub.com/doi/full/10.1177/1948550619876629) article.



