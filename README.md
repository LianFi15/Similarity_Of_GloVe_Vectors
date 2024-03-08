# Similarity Of GloVe Vectors

### Task Description:

This project focuses on analyzing word embeddings, specifically using GloVe vectors, to explore distance, similarity, and analogies among words. The primary tasks include implementing functions for computing cosine similarity, solving analogy tasks, and evaluating the results. The project aims to provide insights into the semantic relationships captured by word embeddings. 

### Implementation and Results
The project delves into vector proximity through cosine similarity, showcasing notable comparisons. 

\[
\text{{Similarity}}(A, B) = \frac{{A \cdot B}}{{\|A\| \cdot \|B\|}} = \frac{{\sum_{i=1}^{n} A_i \cdot B_i}}{{\sqrt{\sum_{i=1}^{n} A_i^2} \cdot \sqrt{\sum_{i=1}^{n} B_i^2}}}
\]


Notably, "car" aligns more with "truck" than "person," and "warm" with "cool" rather than "yesterday." Further exploration involves contrasting {pen, paper} with {pen, ink}. The analysis suggests that "pen" leans towards "writing instruments," while "paper" gravitates towards "writing surfaces," elucidating the observed similarities.

Similarly, we examined {car, driver} versus {car, truck}. Although both involve transportation, "driver" introduces a distinct concept. Surprisingly, "car" aligns more with "truck" than with "driver," highlighting the nuanced associations within the domain.

Additionally, we scrutinized the influence of Euclidean distance on these relations. 

\[
\text{{Euclidean Distance}}(A, B) = \sqrt{\sum_{i=1}^{n} (A_i - B_i)^2}
\]


Intriguingly, pairs validated by cosine similarity failed to corroborate with Euclidean distance, and vice versa. This discrepancy emanates from the inherent dissimilarity in how the metrics interpret vector relationships. Cosine similarity emphasizes directional alignment, while Euclidean distance considers both magnitude and direction, leading to divergent similarity assessments.

