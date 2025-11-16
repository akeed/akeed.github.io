# AI Augmented: Your Creativity Is the Limit Now

*Published: November 16, 2025*


As you’ve  probably seen, all over the web, people do amazing things with the latest AI technology. Tons of posts showing what is possible, even if not always useful (especially not for enterprises). 

New companies are launched like rockets to the sky, and many still are made void by new releases by the very frameworks they built their business on. 

The complaints about yet another bubble, and reports about poor ROI are stacking up. Hype, doomers, people playing the bubble market. Yes, worrying times. Prices have decreased a lot, but we’ve seen that pattern earlier when fighting about market shares.

Business as usual, just accelerated.

Those worries aside, let’s look at what you can do for your own needs. Not to publish or sell, just create solutions to problems you have, and see what happens. 

And, to avoid being too naive, I focused on what I can do on my own laptop. In my dreams I would have my environment air gapped, but for now it’s ok as long as I get my local models and open source frameworks.

**Problem: How to keep up with new technologies, ideally using the same tech?**


I’m hoarding information on the web, articles and posts, that I intend to read more carefully ‘one of these days’. Some are really good, and they drown in the flood. I’m selective, still I have 500+ articles to grasp. 

Disclaimer: Yes, I know there are plenty of services that do this already. I've tested a few, and they are great, and I use them now-and-then, but I wanted to build it myself, to learn, and to be in control of my own data. And never underestimate *the joy of rediscovery.*

**Solution: Formulate, carefully and detailed, what you want, and serve your AI assistant with that context. Then start iterate**

Write a description of what I want, in a context.md. I want a solution that can take a link, go out and get the information the link is pointing to (post, pdf, …), summarize it, tag it, get some grading of comments (if a post), let me grade it, let me add notes to it, make it searchable. And more.

Using VS Code, agent mode, pointing at the context.md, and start iterate. 

The more I worked with this, local-never-to-release-to-anyone-else, I started to wake up, thinking wider, feeling more and more free. Ideas didn’t take months to take shape. Hours, less.

All good, I got a service that, to my surprise, I actually used (still use) daily, that really helped in my collections of information.

But. Collection is the first step, ensuring that I don’t lose any gems I’ve found. Yes, I could search the material, but still.

**Not efficient enough**

I kept mailing myself links, and they stacked up. I manually dropped these into my web solution (that crawled the linked content), but it still felt like a really dumb way of working. Yes, I created a way to take in batches of links, but still. We’re in the so called agent time now, manual isn’t the way to work. 

So I got help again (from my AI assistant, some googling, and ChatGPT) to download and extract Google mails, instead of the manual ingestion step.
*BTW, if you ever think about doing this: create a separate gmail, do all the OATH 2+.*

**Efficient, doing what I asked for, but I need even more**

Ok. Good. I got a way to collect and use my hoarded information. But still, that didn’t  help that much. 

And here’s one observation: *You’re a very demanding customer (not in a bad sense). As the solution expands, the more ideas you get.*
And that’s a key finding: your creativity is not hindered. Period. It takes a moment to grasp that it is you that is the limiting factor. *That it is you who need to get up to speed, not the technology that is slow.*

**Next step: Add analysis, insights, trends**

So, what did I do next? 

I, obviously, wanted more. I wanted real insights, analysis, and trends, not just collecting my findings. So, I ‘talked’ to various AI (good practice, ‘play’ the AI:s against each other), proposing the idea of wrapping it all up into a Knowledge Hub: collect, curate, analyse. Where ‘analyse’ should be, beside earlier search:  ‘this week’, ‘trends’, ‘chat with the information’ (RAG solution). 

*Note: After initial iterations, I created a new project, with above as initial collector and curator step. And, yes, I created a new context.md file to get a good start.*

Some hours later it was all in place. Collecting and curating new findings into the 'platform' is now really smooth, even if the embeddings of the data takes longer (running local, all on my Mac).

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; align-items: flex-start;">
<img src="images/knowledge-hub.png" alt="Landing page" style="max-width: 45%; height: auto;">
<img src="images/chat-example.png" alt="Chat example" style="max-width: 45%; height: auto;">
</div>


**Now, what? What's next?**

Tune above. Use validation techniques (Arize Phoenix and more) to get it as good a possible. Deepen the analysis angles, maybe add graphs to get deeper insights. Or something (for sure something) more.
But also, start thinking about what else I can do. 

That's when I started my next project, 'AI Architecture Lab', using **AI to accelerate my job as architect.**. That one is also completed (ok, nothing ever get completed, but you get the idea), and I’ll write about that next.

*Your creativity is the only limit now.*


**The Knowledge Hub, under the hood (will evolve, for sure)**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         KNOWLEDGE HUB SYSTEM                                │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│  PHASE 1: COLLECTION                                                        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌─────────────────┐    ┌─────────────────┐    ┌──────────────────┐         │
│  │ Knowledge       │    │ Gmail           │    │ Custom           │         │
│  │ Crawler         │───▶│ Crawler         │───▶│ Collectors       │         │
│  │ (Web/LinkedIn)  │    │ (Email)         │    │ (Slack, etc)     │         │
│  └─────────────────┘    └─────────────────┘    └──────────────────┘         │
│           │                      │                       │                  │
│           └──────────────────────┴───────────────────────┘                  │
│                                  │                                          │
│                                  ▼                                          │
│                        ┌──────────────────┐                                 │
│                        │   MinIO S3       │                                 │
│                        │  Object Storage  │                                 │
│                        │  data/raw/*.json │                                 │
│                        └──────────────────┘                                 │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│  PHASE 2: CURATION                                                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                        ┌──────────────────┐                                 │
│                        │   Curator        │                                 │
│                        │  normalize.py    │                                 │
│                        └────────┬─────────┘                                 │
│                                 │                                           │
│  • Parse & clean raw JSON       │                                           │
│  • Extract metadata             │                                           │
│  • Generate content hash (ID)   │                                           │
│  • Create Evidence objects      │                                           │
│                                 ▼                                           │
│                        ┌──────────────────┐                                 │
│                        │  PostgreSQL DB   │                                 │
│                        │    (Metadata)    │                                 │
│                        └──────────────────┘                                 │
│                                 │                                           │
│                                 ▼                                           │
│                        ┌──────────────────┐                                 │
│                        │  data/curated/   │                                 │
│                        │  Evidence files  │                                 │
│                        │  {id}.json       │                                 │
│                        └──────────────────┘                                 │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│  PHASE 3: ENRICHMENT                                                        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                        ┌──────────────────┐                                 │
│                        │   Enricher       │                                 │
│                        │   enrich.py      │                                 │
│                        └────────┬─────────┘                                 │
│                                 │                                           │
│  ┌──────────────────────────────┼──────────────────────────────┐            │
│  │                              │                              │            │
│  ▼                              ▼                              ▼            │
│ ┌──────────────┐      ┌──────────────────┐        ┌─────────────────┐       │
│ │ Ollama LLM   │      │ spaCy NLP        │        │ Nomic Embedder  │       │
│ │ (llama3.1:8b)│      │ (en_core_web_sm) │        │ (768-dim)       │       │
│ └──────┬───────┘      └────────┬─────────┘        └────────┬────────┘       │
│        │                       │                           │                │
│        │  • Short summary      │  • Named entities         │  • Text        │
│        │  • Executive summary  │  • Organizations          │    vectors     │
│        │  • Technical summary  │  • Technologies           │  • Summary     │
│        │  • Key points         │  • Concepts               │    vectors     │
│        │  • Taxonomy           │                           │                │
│        └───────────────────────┴───────────────────────────┘                │
│                                 │                                           │
│                                 ▼                                           │
│                        ┌──────────────────┐                                 │
│                        │  data/enriched/  │                                 │
│                        │  Evidence files +│                                 │
│                        │  metadata        │                                 │
│                        └──────────────────┘                                 │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│  PHASE 4: ANALYSIS & API                                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌───────────────────────────────────────────────────────────────┐          │
│  │                  FastAPI Server (port 8000)                   │          │
│  ├───────────────────────────────────────────────────────────────┤          │
│  │                                                               │          │
│  │  ┌──────────────┐  ┌──────────────┐  ┌────────────────────┐   │          │
│  │  │  Search      │  │  Chat/RAG    │  │  Digest & Analysis │   │          │
│  │  │  Router      │  │  Router      │  │  Router            │   │          │
│  │  └──────┬───────┘  └──────┬───────┘  └──────────┬─────────┘   │          │
│  │         │                 │                     │             │          │
│  │         ▼                 ▼                     ▼             │          │
│  │  ┌──────────────────────────────────────────────────────┐     │          │
│  │  │       Analyzer Engine (analyze.py)                   │     │          │
│  │  ├──────────────────────────────────────────────────────┤     │          │
│  │  │  • SemanticSearch     (vector similarity)            │     │          │
│  │  │  • SimilarityDetector (duplicates, clusters)         │     │          │
│  │  │  • DigestGenerator    (daily, weekly, trending)      │     │          │
│  │  └──────────────────────────────────────────────────────┘     │          │
│  │                                                               │          │
│  │  ┌────────────────────────────────────────────────────────┐   │          │
│  │  │            Web UI (index.html)                         │   │          │
│  │  ├────────────────────────────────────────────────────────┤   │          │
│  │  │  📊 Search Tab    💬 Chat Tab    📈 Digest Tab          │   │          │
│  │  └────────────────────────────────────────────────────────┘   │          │
│  └───────────────────────────────────────────────────────────────┘          │
│                                                                             │
│  Access Points:                                                             │
│  • Web UI:    http://localhost:8000                                         │
│  • API Docs:  http://localhost:8000/docs                                    │
│  • CLI:       python analyzer/analyze.py search "query"                     │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│  INFRASTRUCTURE                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌───────────────┐  ┌────────────────┐  ┌─────────────────┐                 │
│  │   Colima      │  │  PostgreSQL    │  │  MinIO S3       │                 │
│  │  (Docker)     │  │  (Metadata)    │  │  (Raw Files)    │                 │
│  │  port 2375    │  │  port 5432     │  │  port 9000/9001 │                 │
│  └───────────────┘  └────────────────┘  └─────────────────┘                 │
│                                                                             │
│  ┌───────────────┐  ┌────────────────┐                                      │
│  │   Ollama      │  │  Python venv   │                                      │
│  │  (Local LLM)  │  │  Dependencies  │                                      │
│  │  port 11434   │  │  3.11+         │                                      │
│  └───────────────┘  └────────────────┘                                      │
└─────────────────────────────────────────────────────────────────────────────┘
```





