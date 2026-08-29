<h1 align="center">Roy Carlous Christudass</h1>

<p align="center">
  <a href="https://roycarlous.com">
    <img src="https://readme-typing-svg.herokuapp.com/?font=JetBrains+Mono&size=22&duration=3500&pause=1000&color=DC2626&center=true&vCenter=true&width=720&lines=AI+Software+Engineer;Machine+learning%2C+data+and+backend+systems" alt="AI Software Engineer. Machine learning, data and backend systems, built end to end." />
  </a>
</p>

<p align="center">
  <a href="https://roycarlous.com"><img src="https://img.shields.io/badge/Portfolio-roycarlous.com-DC2626?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/roy-carlous-c/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:roy4edu@gmail.com"><img src="https://img.shields.io/badge/Email-roy4edu%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://komarev.com/ghpvc/?username=carlous-roy&style=for-the-badge&color=DC2626&label=Profile+views" alt="Profile views" />
</p>

---

## About

I'm a software engineer working on AI and data systems. Most of what I build ends up the same
shape: data coming in, a model or some logic over it, an API in the middle, and a front end
someone actually uses, and I like working across all of that rather than owning one layer.

Before my master's I spent nearly three years at HCLTech, contracted to Teradyne, writing C++ and
C#/.NET drivers for semiconductor test equipment. The software controlled physical hardware, so
bugs were expensive and I got good at tracing them. I also ended up owning customer escalations
and building the dashboards that tracked them, which is how I got into data work in the first
place.

I'm currently actively looking for Internship or Full-Time roles where I can bring real
engineering rigor to high-impact problems.

Based in Dayton, OH, open to relocation. Reach me at **roy4edu@gmail.com**.

---

## Tech stack

<p align="center"><strong>Languages</strong></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=python,java,cpp,cs,js,html,css" alt="Python, Java, C++, C#, JavaScript, HTML, CSS" />
</p>

<p align="center"><strong>AI and ML</strong></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=sklearn,opencv,py" alt="scikit-learn, OpenCV, Python" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Gradient_Boosting-11557C?style=flat-square" alt="Gradient Boosting" />
  <img src="https://img.shields.io/badge/Embeddings-4B5563?style=flat-square" alt="Embeddings" />
  <img src="https://img.shields.io/badge/Hybrid_Retrieval-4B5563?style=flat-square" alt="Hybrid retrieval" />
  <img src="https://img.shields.io/badge/BM25-4B5563?style=flat-square" alt="BM25" />
  <img src="https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square&logo=google&logoColor=white" alt="MediaPipe" />
  <img src="https://img.shields.io/badge/Tree--sitter-6E4C13?style=flat-square" alt="Tree-sitter" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />
  <img src="https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini API" />
  <img src="https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white" alt="Claude" />
</p>

<p align="center"><strong>Backend, frontend and cloud</strong></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=spring,fastapi,react,vite,tailwind,aws,docker,postgres,mysql,git,maven" alt="Spring Boot, FastAPI, React, Vite, Tailwind, AWS, Docker, PostgreSQL, MySQL, Git, Maven" />
</p>

<p align="center"><strong>Data and BI</strong></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=py,mysql,postgres" alt="Python, MySQL, PostgreSQL" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black" alt="Power BI" />
  <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="pandas" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/ETL_Pipelines-4B5563?style=flat-square" alt="ETL pipelines" />
</p>

---

## Projects

Three are deployed and the fourth has a written case study. The code for each is public.

### [DiffLens](https://github.com/carlous-roy/DiffLens-Engine) · [demo](https://difflens.roycarlous.com)

A code review engine that parses the code rather than pattern-matching the text. Tree-sitter builds
ASTs for Python and Java and measures cyclomatic complexity and nesting depth, a gradient-boosting
model scores change risk, TF-IDF sorts findings into five classes, and embedding search surfaces
issues the codebase has seen before. An optional local CodeLlama pass rewrites findings as review
comments, and GitHub webhooks run the whole thing on every pull request.

`Python` `FastAPI` `scikit-learn` `Tree-sitter` `PostgreSQL` `React` `Docker` `Ollama`

### [TaskForge](https://github.com/carlous-roy/TaskForge-Engine) · [demo](https://taskforge.roycarlous.com)

Distributed report generation. Requests queue through SQS, independent workers process them, and
results land in S3 behind presigned URLs. Most of the code handles what happens when something
breaks: exponential backoff with jitter, a dead-letter queue after three attempts, idempotency keys
that return 409 rather than doing the work twice, a 60-second graceful drain on SIGTERM, and
correlation IDs that keep a failed job traceable across every hop.

`Java 17` `Spring Boot` `AWS SQS/S3/DynamoDB` `Docker` `LocalStack` `React`

### [GestureControl](https://github.com/carlous-roy/GestureControl-Engine) · [demo](https://gesture.roycarlous.com)

A 30 FPS control loop from a webcam to a relay module. MediaPipe runs two models per frame, an SSD
palm detector then direct regression of 21 3D hand landmarks, and a geometric classifier reads
finger state from that geometry. The thumb needs its own rule because it folds laterally rather than
vertically. Jitter and stabilization filtering sit between the classifier and the relays, and a
simulation mode runs the whole loop with no board attached.

Started as my final-year project in 2022 and rebuilt in 2026 with a modular package, unit tests, a
CLI and the simulation mode.

`Python` `OpenCV` `MediaPipe` `PyFirmata` `Arduino UNO`

### [CodeAtlas](https://github.com/carlous-roy/CodeAtlas) · [case study](https://roycarlous.com/case-studies/codeatlas.html)

Semantic search over a codebase, and an evaluation harness that says how well it actually works.
The retrieval is a weekend; the measurement is the project. 36 questions with labelled answers,
scored across four retrieval strategies and three chunking strategies, every number regenerated by
the eval script.

Best configuration reaches recall@5 0.86 and MRR 0.591. Two findings went against what I expected.
Tree-sitter chunking on declaration boundaries first *lost* to a naive fixed-window baseline, and
the reason was that my experiment moved chunk size and chunk boundaries at once; with sizes matched
it wins on ranking, recall@1 0.42 against 0.31. And a standard MS MARCO cross-encoder reranker made
things worse, because it is trained on web passages and code is out of distribution for it.

`Python` `sentence-transformers` `Tree-sitter` `BM25` `NumPy`

---

<p align="center">
  <a href="https://roycarlous.com">roycarlous.com</a> ·
  <a href="https://www.linkedin.com/in/roy-carlous-c/">LinkedIn</a> ·
  <a href="mailto:roy4edu@gmail.com">roy4edu@gmail.com</a>
</p>
