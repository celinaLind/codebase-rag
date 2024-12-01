# Raggity

This project involves creating an AI expert over a codebase using Retrieval-Augmented Generation (RAG). Implementing the ability to chat with a codebase so the user can understand how they work and what can be improved.

Given the user's query, the most relevant code is retrieved from the codebase and used to generate a response using an LLM.

This is done from a web app where users can chat with a codebase. Where the contents of a codebase are embedded, inserted into a vector database called Pinecone, and then get answers to the user's queries based on the contents of the codebase using LLMs.

## Table of Contents
- [Tools Used](#tools-and-skills-used)
- [Notes](#notes)
- [Development Issues](#development-issues)
- [Resources](#resources)
- [Coming Soon](#coming-soon)

## Tools and Skills Used
- Python
- Streamlit
- Google Colab
- Pinecone
- Model Inference
- GitHub API
- Agents
- Groq

## Notes
...

## Development Issues

##### Currently Working on:
- While developing a Streamlit app in Colab I ran into an issue where the session_state feature for streamlit wasn't updating the UI. But I did find a [discussion](https://discuss.streamlit.io/t/updating-state-variable-doesnt-rerun-the-app/47470) about using a callback widget that can trigger a UI rerun.
- Ran into a styling issue where the input fields were being held right below the initial bot messages instead of at the bottom of the screen. Also, new messages would appear beneath the input fields and only properly display after a manual rerun was done.

## Resources
- [Streamlit Web App](https://docs.streamlit.io/develop/tutorials/llms/build-conversational-apps) - Python Chatbot
- [Vercel Chatbot](https://vercel.com/templates/next.js/nextjs-ai-chatbot) - React and Next.js
- [RAG Workdshop](https://app.headstarter.co/content/accelerator/recordings/rag-workshop)
- [Example Codebase RAG Web App](https://sage.storia.ai/)
- [RAG on Codebases](https://blog.lancedb.com/rag-codebase-1/)
- [Getting started with Embeddings](https://huggingface.co/blog/getting-started-with-embeddings)
- [Embedding Model Leaderboard](https://huggingface.co/spaces/mteb/leaderboard)
- [How Greptile does Codebase RAG](https://news.ycombinator.com/item?id=39604961)
- [RAG Codebase with 10k Repos](https://www.qodo.ai/blog/rag-for-large-scale-code-repos/)
- [How embeddings are Generated](https://arxiv.org/abs/1301.3781)
- [Headstarter Project](https://github.com/team-headstart/CodebaseRAG/tree/main)
- [5 levels of text-splitting retrieval](https://www.youtube.com/watch?v=8OJC21T2SL4)

## Coming Soon
- Add support for image uploads when chatting with the codebase - this is called Multimodal RAG.
- Add a way to select different codebases to chat with.
- Add a way to update the Pinecone index when you push any new commits to your repo. This would be done through a webhook that's triggered on each commit, where the codebase is re-embedded and added to Pinecone.
- Add a way to chat with multiple codebases at the same time.
