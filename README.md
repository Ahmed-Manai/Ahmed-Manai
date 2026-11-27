<h1 align="center">Hi, I'm Ahmed Manai 👋</h1>

<p align="center">
  <b>Full-Stack &amp; AI Engineer · Microsoft Certified Azure Solutions Architect Expert</b><br/>
  LLM apps · RAG · AI agents · .NET · Angular · Spring Boot · Azure
</p>

<p align="center">
  <a href="mailto:manai.ahmed.tn@gmail.com"><img src="https://img.shields.io/badge/Email-manai.ahmed.tn%40gmail.com-D14836?style=flat&logo=gmail&logoColor=white" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Location-Tunis%2C%20Tunisia-0A66C2?style=flat&logo=googlemaps&logoColor=white" alt="Location"/>
  <a href="https://github.com/Ahmed-Manai?tab=repositories"><img src="https://img.shields.io/badge/Repositories-browse-181717?style=flat&logo=github&logoColor=white" alt="Repositories"/></a>
</p>

---

## About me

I build cloud-native applications end to end, from Angular front ends to .NET and Spring Boot services on Azure, and more and more the AI features inside them: LLM integrations, retrieval-augmented generation (RAG) and semantic search. I have 3+ years of professional experience and hold the **Microsoft Certified: Azure Solutions Architect Expert** certification.

- 🤖 I build LLM features with Azure OpenAI and the OpenAI API: embeddings, vector search and RAG
- 🧩 I contribute to [Quarkus LangChain4j](https://github.com/quarkiverse/quarkus-langchain4j), the Java framework for LLM apps and agents: I work on its Azure OpenAI extension, where my [v1 endpoints support](https://github.com/quarkiverse/quarkus-langchain4j/pull/3100) and [streaming chat model fix](https://github.com/quarkiverse/quarkus-langchain4j/pull/3299) are merged, and I track what is still missing in [#3293](https://github.com/quarkiverse/quarkus-langchain4j/issues/3293)
- 🧠 I build tools for AI agents with the Model Context Protocol (MCP): my [docs-rag-mcp](https://github.com/Ahmed-Manai/docs-rag-mcp) server is on NuGet and in the official MCP Registry, and I fix bugs in the [MCP C# SDK](https://github.com/modelcontextprotocol/csharp-sdk/pull/2041) it is built on
- 🔗 I contribute fixes to [LangChain4j](https://github.com/langchain4j/langchain4j/pulls?q=is%3Apr+author%3AAhmed-Manai) (tool calling, chat memory) and [Keycloak](https://github.com/keycloak/keycloak/pulls?q=is%3Apr+author%3AAhmed-Manai) (admin console)
- 🏗️ I design cloud systems on Azure (Functions, AKS, Service Bus, Cosmos DB) with a focus on performance and cost
- ⚡ I work on real-time data processing with gRPC, SignalR, MQTT and ZeroMQ
- ✍️ I write about LLMs, RAG and search: [I built a local RAG server for Claude and Copilot in C#. Here is what I learned about search.](https://dev.to/ahmed_manai/i-built-a-local-rag-server-for-claude-and-copilot-in-c-here-is-what-i-learned-about-search-2h3) on DEV, and [llm-articles](https://github.com/Ahmed-Manai/llm-articles)

## 🤖 AI & LLM work

| Project | What it is | Stack |
|---------|-----------|-------|
| [**docs-rag-mcp**](https://github.com/Ahmed-Manai/docs-rag-mcp) | An MCP server that lets Claude, GitHub Copilot and Cursor search your own Markdown, text, HTML, Word and PDF files with RAG. Hybrid search (vectors + keywords), watched folders that stay in sync, and fully local with Ollama, or OpenAI or Azure OpenAI. Published on [NuGet](https://www.nuget.org/packages/DocsRagMcp) and in the official MCP Registry | C# · .NET 10 · MCP · SQLite |
| [**llm-articles**](https://github.com/Ahmed-Manai/llm-articles) | A practical guide to embeddings, cosine similarity, dense vector search and RAG, with runnable notebooks | Python · OpenAI |
| [**Azure OpenAI v1 endpoints for Quarkus LangChain4j**](https://github.com/quarkiverse/quarkus-langchain4j/pull/3100) | Adds support for the new Azure OpenAI `v1` API to the chat and embedding models. Merged | Java · Quarkus · LangChain4j |
| [**E-Learn-Transformers**](https://github.com/Ahmed-Manai/E-Learn-Transformers) | An Angular app that sends prompts to a GPT model and shows the generated text | Angular · TypeScript · OpenAI |

## 🚀 Latest releases

### [docs-rag-mcp](https://github.com/Ahmed-Manai/docs-rag-mcp)

<a href="https://www.nuget.org/packages/DocsRagMcp"><img src="https://img.shields.io/nuget/v/DocsRagMcp?logo=nuget&label=NuGet" alt="NuGet version"/></a>
<a href="https://github.com/Ahmed-Manai/docs-rag-mcp/actions/workflows/ci.yml"><img src="https://github.com/Ahmed-Manai/docs-rag-mcp/actions/workflows/ci.yml/badge.svg" alt="CI"/></a>
<a href="https://github.com/Ahmed-Manai/docs-rag-mcp/stargazers"><img src="https://img.shields.io/github/stars/Ahmed-Manai/docs-rag-mcp?style=flat&logo=github" alt="GitHub stars"/></a>

An MCP server that gives AI assistants retrieval-augmented generation over your own documents. Point it at a folder of notes, docs or PDFs and ask Claude, Copilot or Cursor questions about them: it answers from the most relevant passages and cites the file and section. Documents can stay on your machine with Ollama, and the index is a single SQLite file.

- **Hybrid search**: vector similarity blended with SQLite FTS5 keyword ranking, tuned on an evaluation set
- **Watch mode**: indexed folders stay in sync on their own, including changes made while the server was stopped
- **Incremental**: content hashes mean only changed files are embedded again
- **MCP resources**: indexed files are exposed as MCP resources, so the assistant can open the whole file behind an answer (0.7.0)

```bash
claude mcp add docs-rag -- dnx DocsRagMcp --yes
```

Listed in [Awesome-LLM-RAG](https://github.com/jxzhangjhu/Awesome-LLM-RAG) and in the [TensorBlock](https://github.com/TensorBlock/awesome-mcp-servers) and [Sagargupta16](https://github.com/Sagargupta16/awesome-mcp-servers) awesome MCP servers lists.

[NuGet](https://www.nuget.org/packages/DocsRagMcp) · [Source](https://github.com/Ahmed-Manai/docs-rag-mcp) · [How it works (article)](https://dev.to/ahmed_manai/i-built-a-local-rag-server-for-claude-and-copilot-in-c-here-is-what-i-learned-about-search-2h3) · [Good first issues](https://github.com/Ahmed-Manai/docs-rag-mcp/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)

### [Company Highlighter](https://github.com/Ahmed-Manai/company-highlighter-browser-extension)

A browser extension (Chrome, Edge, Firefox) that highlights the companies from your own list on any web page, which makes job boards, LinkedIn and news much faster to scan. Your list stays in your browser. Open to contributions: two features in the latest version were built by contributors.

<a href="https://github.com/Ahmed-Manai/company-highlighter-browser-extension">
  <img src="https://raw.githubusercontent.com/Ahmed-Manai/company-highlighter-browser-extension/main/docs/screenshot-highlights.png" alt="Company Highlighter highlighting company names on a job board" width="720"/>
</a>

[Download the latest release](https://github.com/Ahmed-Manai/company-highlighter-browser-extension/releases/latest) · [Source](https://github.com/Ahmed-Manai/company-highlighter-browser-extension) · [Good first issues](https://github.com/Ahmed-Manai/company-highlighter-browser-extension/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)

## 🤝 Open-source contributions

| Project | Contribution | Status |
|---------|--------------|--------|
| [dotnet/maui](https://github.com/dotnet/maui) | [Fix misleading MA002 warning text about implicit package references (#39858)](https://github.com/dotnet/maui/pull/39858) | ✅ Merged |
| [microsoft/mcp](https://github.com/microsoft/mcp) | [Return the tool list for an unknown tool in single mode (#4236)](https://github.com/microsoft/mcp/pull/4236), a bug I found and reported in [#4235](https://github.com/microsoft/mcp/issues/4235) | 👍 Approved |
| [quarkiverse/quarkus-langchain4j](https://github.com/quarkiverse/quarkus-langchain4j) | [Apply the chat-model credentials and API version to the Azure OpenAI streaming chat model (#3299)](https://github.com/quarkiverse/quarkus-langchain4j/pull/3299), which also made streaming calls send the Azure AD token | ✅ Merged |
| [quarkiverse/quarkus-langchain4j](https://github.com/quarkiverse/quarkus-langchain4j) | [Add Responses API support to the Azure OpenAI chat models (#3292)](https://github.com/quarkiverse/quarkus-langchain4j/pull/3292) | 🔄 In review |
| [quarkiverse/quarkus-langchain4j](https://github.com/quarkiverse/quarkus-langchain4j) | [Add max-completion-tokens and stop to the Azure OpenAI chat models (#3300)](https://github.com/quarkiverse/quarkus-langchain4j/pull/3300), needed by the o-series reasoning models | 🔄 In review |
| [modelcontextprotocol/csharp-sdk](https://github.com/modelcontextprotocol/csharp-sdk) | [Bind true and false prompt arguments to bool parameters (#2041)](https://github.com/modelcontextprotocol/csharp-sdk/pull/2041), a bug I found and reported in [#2040](https://github.com/modelcontextprotocol/csharp-sdk/issues/2040) | 🔄 In review |
| [langchain4j/langchain4j](https://github.com/langchain4j/langchain4j) | [Count only responses with tool calls against maxToolCallingRoundTrips (#7273)](https://github.com/langchain4j/langchain4j/pull/7273) | 🔄 In review |
| [langchain4j/langchain4j](https://github.com/langchain4j/langchain4j) | [Compare the memory id with the default id by value in ChatMemoryService (#7272)](https://github.com/langchain4j/langchain4j/pull/7272) | 🔄 In review |
| [keycloak/keycloak](https://github.com/keycloak/keycloak) | [Set the admin console html lang attribute from the user locale (#55491)](https://github.com/keycloak/keycloak/pull/55491), a bug I found and reported in [#55490](https://github.com/keycloak/keycloak/issues/55490) | 🔄 In review |
| [keycloak/keycloak](https://github.com/keycloak/keycloak) | [Show an error when an uploaded JSON file is not valid (#55498)](https://github.com/keycloak/keycloak/pull/55498) | 🔄 In review |
| [quarkiverse/quarkus-langchain4j](https://github.com/quarkiverse/quarkus-langchain4j) | [Support Azure OpenAI v1 endpoints for chat and embedding models (#3100)](https://github.com/quarkiverse/quarkus-langchain4j/pull/3100) | ✅ Merged |

## Tech stack

<p>
  <img src="https://skillicons.dev/icons?i=cs,dotnet,java,spring,python,ts,js,angular,react,azure,docker,kubernetes,mysql,mongodb,postgres,git,githubactions&perline=9" alt="Tech stack"/>
</p>

| Area | Technologies |
|------|--------------|
| **AI & LLM** | Azure OpenAI, OpenAI API, Ollama, Model Context Protocol (MCP), Microsoft.Extensions.AI, LangChain4j, RAG, embeddings, vector search, prompt engineering |
| **Languages** | C#, Java, Python, TypeScript, SQL |
| **Back end** | .NET 6 to 10, ASP.NET Core, Blazor, Spring Boot, Quarkus, FastAPI |
| **Front end** | Angular 14+, React |
| **Cloud & DevOps** | Azure (Functions, AKS, Service Bus, Cosmos DB), Azure DevOps, Docker, Kubernetes, Jenkins, GitHub Actions |
| **Data** | MySQL, PostgreSQL, MongoDB, Apache Spark |
| **Messaging & protocols** | gRPC, SignalR, MQTT, ZeroMQ, REST |
| **Practices** | Clean Architecture, Agile/Scrum, TDD, CI/CD, UML/BPMN modelling, rule engines (Drools, Activiti) |

## Featured projects

| Project | What it is | Stack |
|---------|-----------|-------|
| [**company-highlighter-browser-extension**](https://github.com/Ahmed-Manai/company-highlighter-browser-extension) | Highlights the companies from your own list on any web page, with excluded sites, a popup and a match badge | JavaScript · Manifest V3 |
| [**nexadash**](https://github.com/Ahmed-Manai/nexadash) | An admin dashboard starter with SVG charts, data tables, dark mode, tests and CI. [Live demo](https://ahmed-manai.github.io/nexadash/) | Angular 21 · Material · Tailwind |
| [**User-Management-MS**](https://github.com/Ahmed-Manai/User-Management-MS) | A user management REST microservice with Swagger UI and CI | Java · Spring Boot · MongoDB |
| [**IdentityServer4Pro**](https://github.com/Ahmed-Manai/IdentityServer4Pro) | An OAuth 2.0 / OpenID Connect identity provider built on IdentityServer4 | C# · ASP.NET Core |
| [**React-go-containerized-env**](https://github.com/Ahmed-Manai/React-go-containerized-env) | A three-tier app (React, Node and Go APIs, PostgreSQL) fully containerised with Docker | Docker · Go · Node · React |
| [**ManaiBay**](https://github.com/Ahmed-Manai/ManaiBay) | A client management app with a JWT-secured REST API | React · FastAPI · Cassandra |
| [**Algorithms-Computational**](https://github.com/Ahmed-Manai/Algorithms-Computational) | Classic sorting algorithms in C#, one console project each, built and run in CI | C# · .NET |

## GitHub activity

<p>
  <img src="https://streak-stats.demolab.com/?user=Ahmed-Manai&hide_border=true&theme=tokyonight" alt="GitHub streak"/>
</p>

## Let's connect

I'm open to collaborating on AI and LLM projects, open source, cloud architecture and full-stack work. Reach me by [email](mailto:manai.ahmed.tn@gmail.com), or open an issue or discussion on any of my repositories.
