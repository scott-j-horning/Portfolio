# Finsights Grey — 10-K Retrieval-Augmented Generation
Retrieval-Augmented Generation (RAG) over five 2023 Form 10-K reports for a fictional fintech.  
Target: answer analyst questions from the filings, not from model memory.

## Approach
- Load and split five PDFs (Google, Amazon, Microsoft, IBM, Meta)
- Embed with Sentence Transformers; store in Chroma
- Filter retrieval by company, then generate with OpenAI
- Gradio interface and Hugging Face Space for inference
- Log responses as a Hugging Face dataset

## Key pieces
- Company filter on document source
- Persistent Chroma index
- Gradio radio selector plus question box

## Result
Capstone scored 40/40. Space is public at https://huggingface.co/spaces/scott-j-horning/finsights-10k-rag

PDFs omitted from this repository.