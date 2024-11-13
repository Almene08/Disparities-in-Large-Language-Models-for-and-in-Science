# Disparities-in-Large-Language-Models-for-and-in-Science
### Data
This study utilizes two main sets of words as its primary data: target words and attribute words. Target words, used for both embeddings and LLM outputs analysis include entities such as names from less-prestigious institutions, while attribute words used only for the embeddings level are terms relevant to desired scientific characteristics, such as “research productivity.” We selected 10 words per target word and 20 per attribute word and used two sources for these word sets. Caliskan et al. (2017) provided target words for categories like European vs. African-American names, male vs. female names, and science vs. art terms. Additionally, we used GPT-4 to generate target words related to Global North vs. South, socioeconomic status, and prestigious vs. non-prestigious institutions. GPT-4 also generated attribute words related to, research productivity, research, teaching and funding successes, and award recognition, all with their opposite.

### Models
We used two types of models to assess bias: embedding models and a LLM. For embeddings, we evaluated BERT (Kenton et al., 2019), an encoding model that outputs embeddings for word sequences, and SciBERT (Beltagy et al., 2019), a model trained specifically on scientific literature. These embeddings enable analysis of the relationships between terms, allowing us to detect potential biases in training data representation. We also used Claude 3.5 Sonnet, an advanced LLM with 200,000-token context processing, to analyze if and how biases persist in model outputs, especially in scientific contexts.

### Methods
We applied two primary methods: the Word Embedding Association Test (WEAT) and LLM prompting. The WEAT method computes semantic distances between target and attribute word pairs to detect associations that might reveal biases (Caliskan et al., 2017). For example, we compared whether European names were more closely associated with positive research-related words than African-American names.
In the LLM prompting tasks, we designed two simulations to measure bias in response likelihood. First, we simulated email inquiries to professors about Ph.D. positions, varying the gender and location of the sender. Responses were rated on a Likert-like scale from 1 (Highly unlikely to reply) to 5 (Highly likely to reply). A similar approach was used to simulate manuscript cover letter submissions, with the editor’s decision to desk reject or send for peer review rated on a Likert scale from 1 (Highly unlikely to desk reject) to 5 (Highly likely to submit for review).


### References
Caliskan, A., Bryson, J. J., & Narayanan, A. (2017). Semantics derived automatically from language corpora contain human-like biases. Science, 356(6334), 183-186.
Beltagy, I., Lo, K., & Cohan, A. (2019). SciBERT: A pretrained language model for scientific text. arXiv preprint arXiv:1903.10676.
