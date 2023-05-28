

![Évasion Montage Blog Bannière](https://github.com/BoulahiaAhmed/Semantic-Search-and-Question-Answering/assets/45523231/823fe59c-4f6d-4cc7-a67a-3828b72963c9)



# Introduction to Semantic Search
Semantic search is a fundamental NLP task that aims to bridge the gap between user queries and the underlying meaning of textual content. It goes beyond simple keyword matching, focusing on understanding context and delivering accurate results. While LLMs have advanced NLP, semantic search remains crucial, providing a complementary approach to achieve precise and context-aware search results. In this blog, we explore the importance of semantic search and its integration with question answering models, along with creating a user-friendly web interface.

## 1. Data Preprocessing

![1](https://github.com/BoulahiaAhmed/Semantic-Search-and-Question-Answering/assets/45523231/eccc3502-acf7-478a-96bf-4ee94d50199e)

### - Understanding the Importance of Data Preprocessing
Data preprocessing plays a crucial role in semantic search as it lays the foundation for accurate and meaningful analysis. By extracting text from PDFs and employing techniques like sentence tokenization with Sentence Transformer, we enhance the quality of the data, enabling better understanding and analysis of the content during the semantic search process.

### - Extracting Text from PDFs: A Crucial First Step
Extracting text from PDFs is a crucial first step in the data preprocessing phase. To accomplish this, we employ the powerful pdfplumber Python library. By leveraging its functionality, we can efficiently extract the text content from PDF files, ensuring that we have the necessary textual data to perform subsequent semantic search and question answering tasks accurately and effectively.

### - Sentence Tokenization with Sentence Transformer: Enhancing Text Analysis
Sentence tokenization with the Sentence Transformers Python package is a pivotal step in enhancing text analysis for semantic search. By breaking down the extracted text into individual sentences, we can achieve a finer level of granularity, facilitating improved similarity measurements. Leveraging the power of Sentence Transformers, we can identify and compare relevant semantic units within the text, leading to more precise and context-aware search results.

## 2. Semantic Search

![2](https://github.com/BoulahiaAhmed/Semantic-Search-and-Question-Answering/assets/45523231/79b94708-f7a3-4f5d-95c2-cca5e0c71964)

### - Harnessing the Power of Semantic Search
Unlike traditional keyword-based search, semantic search focuses on understanding the context and meaning behind user queries, leading to more accurate and relevant results. By analyzing the semantic relationships, concepts, and entities within the text, semantic search enables a deeper level of comprehension and improves the search experience. Whether it's finding specific information within scientific papers, legal documents, or news articles, semantic search empowers us to unlock the full potential of vast knowledge repositories and retrieve "precisely" what we need.

### - Exploring Different Similarity Methods for Semantic Search (Faiss, Annoy, and TF-IDF)
In this tutorial, we explore three different similarity methods for semantic search:

- Faiss (Facebook AI Similarity Search): A library for efficient similarity search.
- Annoy (Approximate Nearest Neighbors Oh Yeah)): a package developed by Spotify.
- TF-IDF (Term Frequency-Inverse Document Frequency), a classic information retrieval technique.

By leveraging these techniques, we aim to obtain the top two most relevant results from each method, thereby improving search accuracy and effectiveness.

### - Context Injection: Unveiling the Most Relevant Content
In the context of semantic search, the BERT Question Answering (Q&A) model requires both a context and a question (used as the query) to provide accurate answers. To ensure we have the necessary context for the Q&A model, we employ context injection by concatenating all the top results obtained from the similarity methods (from the previous step). This process creates a comprehensive and informative context that can be utilized effectively by the question answering model to generate precise and contextualized responses.

### 3. Question Answering with BERT

![3](https://github.com/BoulahiaAhmed/Semantic-Search-and-Question-Answering/assets/45523231/a82404a0-578b-42d2-9c6b-2ae5cb997822)

#### - Unleashing the Potential of Question Answering with BERT

By utilizing the Huggingface transformers package and leveraging a pre-trained model called "bert-large-uncased-whole-word-masking-finetuned-squad" which was fine-tuned on the SQuAD dataset, we can achieve accurate and context-aware question answering.

![Untitled](https://github.com/BoulahiaAhmed/Semantic-Search-and-Question-Answering/assets/45523231/255dad76-3c18-4948-ad2e-24e47b75853b)

This model has the following configuration:
- 24-layer
- 1024 hidden dimension
- 16 attention heads
- 336M parameters.

This model is capable of comprehending the nuances of the context and question, allowing it to provide detailed answers based on the information present within the text.

While the release of advanced language models like ChatGPT and other LLMs has garnered significant attention, the impact on the popularity of BERT-based question answering models can be observed from the download graph. Over time, the number of downloads for BERT models has decreased significantly, reflecting the shift in focus towards broader language models. However, it's important to note that BERT still remains a valuable and effective choice for accurate and contextualized question answering tasks.

### 4. Putting It All Together - Creating a Web Interface with Gradio

#### - Enhancing User Experience

![gradio app](https://github.com/BoulahiaAhmed/Semantic-Search-and-Question-Answering/assets/45523231/911808da-10e0-41e2-a852-dcaff15b9061)

Creating a user-friendly web interface is essential for enhancing the overall user experience of our semantic search and question answering system. Gradio, a Python package, proves to be a key tool in this regard. With its intuitive and straightforward design, Gradio allows us to easily build interactive interfaces without extensive web development knowledge.

By providing a simple and elegant way to showcase our semantic search and question answering functionalities, Gradio empowers users to interact seamlessly with our system, making it accessible and user-friendly for both technical and non-technical users alike.

### 5. Conclusion

In this blog, we explored the fascinating world of semantic search and question answering. We delved into the importance of data preprocessing, highlighting the crucial steps of extracting text from PDFs and performing sentence tokenization using Sentence Transformers. We then ventured into the realm of semantic search, discovering the power of different similarity methods like Faiss, Annoy, and TF-IDF to unveil the most relevant content. Leveraging the BERT Question Answering model, we witnessed how it provides accurate and contextualized answers, fueled by its understanding of language and fine-tuning on the SQuAD dataset.

Finally, we witnessed the seamless integration of all these components through the creation of a web interface using Gradio. This interface enhanced the user experience, allowing users to effortlessly interact with our semantic search and question answering system.
