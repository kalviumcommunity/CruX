# CruX – Your Personalized AI News Curator

**CruX** is a web-based GenAI app that helps you stay ahead of the curve by curating and simplifying real-time news across various categories, tailored to your interests. With the power of generative AI, it summarizes top news, delivers bite-sized insights, and lets you interactively dive deeper using a chatbot.

---

##  Problem Statement

The internet is flooded with news from thousands of sources, most of it overwhelming, redundant, and hard to follow. People want quick, reliable, and smart ways to consume news  not a flood of links.

---

##  Our Solution

CruX gives users a personalized, clutter-free, and AI-powered news experience:

- Fetches daily news headlines across various topics
- Uses LLMs (like Gemini) to summarize and explain them
- Lets users chat with a bot to ask for more details
- Delivers clean, minimal UI with high focus on content

---

##  Core Features

- ✅ Fetches real-time news using **free APIs** or **RSS feeds**
- ✅ Auto-summarizes news articles using **LLM-based prompts**
- ✅ Built-in **Chatbot** that answers follow-up queries or explains things
- ✅ Users can **filter by category** (Tech, Finance, World, etc.)
- ✅ Clean and intuitive UI optimized for reading

---

##  Tech Stack

| Area             | Stack/Tool                     |
|------------------|-------------------------------|
| Frontend         | React + TypeScript            |
| Styling          | Tailwind CSS or Bootstrap     |
| Backend (optional) | Node.js + Express (if needed)|
| AI Integration   | Google Gemini  |
| News Source      | NewsData.io, Mediastack, NewsAPI (free tier) or RSS feeds |
| Hosting          | Vercel / Netlify              |

---

## 📌 Gen-AI Implementation Details

###  Prompting

Every news article is fed into a carefully designed prompt structure that asks the model to:

- Summarize it in 3 bullet points
- Identify the context (why it matters)
- Generate a reflection/journaling/writing prompt for deeper thinking
- Format output with labels and clarity

Prompts are engineered to be short, but rich in instruction.

###  Structured Output

Instead of plain text, the AI returns structured JSON or block sections with labeled output:

- **Summary**: TL;DR format
- **Key Takeaways**: Bullet list
- **Why it Matters**: 1-2 line explanation
- **Reflection Prompt**: For user engagement

This makes it easier to render in frontend cards and re-use elsewhere.

###  Function Calling

We'll use **function calling** (e.g., with OpenAI-compatible models) to allow the AI to trigger backend tools based on user queries like:

- `fetchTopicSummary(topic)`
- `getNewsByCategory(category)`
- `generateDailyPrompt()`

This keeps the AI's role focused and clean, while letting the app remain responsive and dynamic.

###  RAG (Retrieval-Augmented Generation)

For deeper questions users may ask (e.g., "What’s the full context behind the US inflation issue?"), we integrate a **RAG pipeline**:

- Use keywords from the user query
- Search cached or real-time content sources (news APIs, Wikipedia, etc.)
- Provide the result as `context` to the model
- Ask model to respond based on both context and prompt

This avoids hallucination and makes answers grounded in facts.

---

##  How to Contribute

1. Fork this repo
2. Clone it to your machine
3. Set up `.env` file for Google API key
4. Start building and open a PR!

---

##  Local Setup

```bash
git clone https://github.com/kalviumcommunity/CruX
cd crux
npm install
npm run dev
