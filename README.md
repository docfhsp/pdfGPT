# pdfGPT

PDF Question Answering Pipeline
Upload your PDF file and chat with it !! 
This pipeline allows users to input a URL to a PDF document, preprocess the text, and use semantic search to generate answers to user questions. The pipeline follows the following steps:

1. **Input**: User inputs a URL to a PDF document.
2. **Download** PDF: The pipeline downloads the PDF from the input URL.
3. **Load PDF**: The PDF is loaded into the pipeline.
4. **Preprocess**: The text of the PDF is preprocessed to prepare for semantic search.
5. **Text Chunks**: The text of the PDF is split into smaller text chunks for semantic search.
6. **SemanticSearch**: A semantic search model is trained on the text chunks.
7. **Query:** User inputs a question.
8. **Get Top Results**: The top semantic search results for the user's question are returned.
9. **Generate Answer**: The pipeline generates an answer based on the top semantic search results.
10. **Output**: The answer is outputted

```mermaid
flowchart LR
    A[Input] -- URL --> B[Download PDF]
    A -- PDF --> C[Load PDF]
    B --> D[Load PDF]
    C -- Preprocess --> E[Dynamic Text Chunks]
    E --Fit-->F[SemanticSearch with Deep Averaging Network Encoder]
    F -- Query --> G[Get Top Results]
    G -- Generate Prompt --> H[Generate Answer]
    H -- Output --> I[Output]

