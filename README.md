## GPT-4 Jenks

👉🏼 Fork [https://github.com/mayooear/gpt4-pdf-chatbot-langchain](https://github.com/mayooear/gpt4-pdf-chatbot-langchain)  
👉🏼 Frontend inspired by [langchain-chat-nextjs](https://github.com/zahidkhawaja/langchain-chat-nextjs)

### Built With

OpenAI GPT-4 LangChain, Pinecone, Typescript, and Next.js. 

LangChain is a framework that makes it easier to build scalable AI/LLM apps and chatbots. 

Pinecone is a vectorstore for storing embeddings and your PDF in text to later retrieve similar docs.

### Run

1. Install Modules
```
yarn install
```

2. Configure Environment
- Copy `.env.example` into `.env`

```
OPENAI_API_KEY=
PINECONE_API_KEY=
PINECONE_ENVIRONMENT=
PINECONE_INDEX_NAME=
```
3. config/pinecone.tx ~ replace the `PINECONE_NAME_SPACE` with a `namespace` where you'd like to store your embeddings. Dimensions to 1536 and metric as cosine. 
 
4. utils/makechain.ts change the `QA_PROMPT` for your own usecase. Change `modelName` in `new OpenAI` to `gpt-4`, if you have access to `gpt-4` api.

5. Convert PDF to embeddings

```
npm run ingest
```
6. Localhost 
```
npm run dev
npm run build
npm run start
```