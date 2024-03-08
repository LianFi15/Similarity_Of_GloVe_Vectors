# Similarity Of GloVe Vectors

### Task Description:

This project focuses on analyzing word embeddings, specifically using GloVe vectors, to explore distance, similarity, and analogies among words. The primary tasks include implementing functions for computing cosine similarity, solving analogy tasks, and evaluating the results. The project aims to provide insights into the semantic relationships captured by word embeddings. 

### Word Embeddings
The project delves into vector proximity through cosine similarity, showcasing notable comparisons. 

$similrity=\cos({\theta})= {\frac{A\cdot B}{|A||B|}}  = {\frac{\sum\limits_{i=1}^{n}A_i B_i}{\sqrt{\sum\limits_{i=1}^{n} A_i^2} \sqrt{\sum\limits_{i=1}^{n} B_i^2}} }$


Notably, "car" aligns more with "truck" than "person," and "warm" with "cool" rather than "yesterday." Further exploration involves contrasting {pen, paper} with {pen, ink}. The analysis suggests that "pen" leans towards "writing instruments," while "paper" gravitates towards "writing surfaces," elucidating the observed similarities.

Similarly, we examined {car, driver} versus {car, truck}. Although both involve transportation, "driver" introduces a distinct concept. Surprisingly, "car" aligns more with "truck" than with "driver," highlighting the nuanced associations within the domain.

Additionally, we scrutinized the influence of Euclidean distance on these relations. 

$Euclidean Distance(A,B) = {\sqrt{\sum\limits_{i=1}^{n}(A_i-B_i)^2}} $

Intriguingly, pairs validated by cosine similarity failed to corroborate with Euclidean distance, and vice versa. This discrepancy emanates from the inherent dissimilarity in how the metrics interpret vector relationships. Cosine similarity emphasizes directional alignment, while Euclidean distance considers both magnitude and direction, leading to divergent similarity assessments.

### The Analogy Test

To solve analogies using semantic vectors, the relationship between words *w1*, *w2*, and *w3* can be expressed as follows: *w1* is to *w2* as *w3* is to *x*. In this context, the goal is to find a word *x* such that the semantic relationship between *w1* and *w2* is analogous to the relationship between *w3* and *x*. This is achieved by calculating a vector $y = {e(w_2) - e(w_1) + e(w_3)}$ and identifying the word whose vector is closest to $y$.

For instance, if we consider the analogy *France*:*Paris* :: *England*:*x*, the result might be that *x* is most likely to be *London*, based on semantic vector calculations.

Here are some examples of successful analogies:

- *small* is to *smaller* as *big* is to ['bigger', 'smaller', 'larger', 'biggest', 'much']

And an example that did not work as well:

- *guitar* is to *music* as *brush* is to ['scrub', 'dry', 'music', 'aside', 'brushes']

In the less successful case, it's suggested that trying a different type of musical instrument might yield better results. For instance, a different musical instrument may provide a more suitable analogy for the relationship between *brush* and *music*.
