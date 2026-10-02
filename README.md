<h1 align="center">Roy Carlous Christudass</h1>

<p align="center">
  <a href="https://roycarlous.com">
    <img src="https://readme-typing-svg.herokuapp.com/?font=JetBrains+Mono&size=22&duration=3500&pause=1000&color=DC2626&center=true&vCenter=true&width=720&lines=Software+Engineer;Machine+learning%2C+data+and+backend+systems" alt="Software Engineer. Machine learning, data and backend systems." />
  </a>
</p>

<p align="center">
  <a href="https://roycarlous.com"><img src="https://img.shields.io/badge/Portfolio-roycarlous.com-DC2626?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/roy-carlous-c/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:roy4edu@gmail.com"><img src="https://img.shields.io/badge/Email-roy4edu%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

---

## About

I'm a software engineer working on AI and data systems. Most of what I build ends up the same
shape: data coming in, a model or some logic over it, an API in the middle, and a front end
someone actually uses, and I like working across all of that rather than owning one layer.

Before my master's I spent January 2022 to August 2024 at HCLTech, contracted to Teradyne,
writing C++ and C#/.NET drivers for semiconductor test equipment. The software controlled physical
hardware, so bugs were expensive and I got good at tracing them. I also ended up owning customer
escalations and building the dashboards that tracked them, which is how I got into data work in
the first place.

I finished my M.S. in Computer Science at Wright State University in August 2026 and I'm looking
for a full-time software engineering role: backend, machine learning or data.

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
  <img src="https://img.shields.io/badge/Gradient_Boosting-11557C?style=flat-square" alt="Gradient boosting" />
  <img src="https://img.shields.io/badge/SHAP-4B5563?style=flat-square" alt="SHAP" />
  <img src="https://img.shields.io/badge/Embeddings-4B5563?style=flat-square" alt="Embeddings" />
  <img src="https://img.shields.io/badge/Hybrid_Retrieval-4B5563?style=flat-square" alt="Hybrid retrieval" />
  <img src="https://img.shields.io/badge/BM25-4B5563?style=flat-square" alt="BM25" />
  <img src="https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square&logo=google&logoColor=white" alt="MediaPipe" />
  <img src="https://img.shields.io/badge/Tree--sitter-6E4C13?style=flat-square" alt="Tree-sitter" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />
  <img src="https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini API" />
</p>

<p align="center"><strong>Backend, frontend and cloud</strong></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=spring,fastapi,react,vite,tailwind,aws,docker,postgres,mysql,git,githubactions,maven" alt="Spring Boot, FastAPI, React, Vite, Tailwind, AWS, Docker, PostgreSQL, MySQL, Git, GitHub Actions, Maven" />
</p>

<p align="center"><strong>Data and BI</strong></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=py,mysql,postgres" alt="Python, MySQL, PostgreSQL" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black" alt="Power BI" />
  <img src="https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square" alt="SQL Server" />
  <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="pandas" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy" />
</p>

---

## Projects

Three have browser demos and the fourth has a written case study. The code for each is public, and
every number below is reproduced by the tests or the evaluation script in its repository.

### [DiffLens](https://github.com/carlous-roy/DiffLens-Engine) · [demo](https://difflens.roycarlous.com)

A code review service that parses the code rather than pattern-matching the text. Tree-sitter
builds ASTs for Python and Java and measures cyclomatic complexity and nesting depth, with rules
that never fire inside comments or strings. A gradient-boosted model trained on ApacheJIT (106,674
commits from 15 Apache projects) scores change risk with calibrated probabilities and per-feature
attributions, held-out ROC-AUC 0.80. Findings are embedded into pgvector, so a review can say how
many times an issue has been seen before, and GitHub webhooks post inline comments on every pull
request. An optional local model through Ollama rewrites findings as review comments. 291 tests.

`Python` `FastAPI` `scikit-learn` `Tree-sitter` `PostgreSQL/pgvector` `React` `Docker` `Ollama`

### [TaskForge](https://github.com/carlous-roy/TaskForge-Engine) · [demo](https://taskforge.roycarlous.com)

Distributed report generation. Requests queue through SQS, independent workers process them, and
results land in S3 behind presigned URLs. Most of the code handles what happens when something
breaks: idempotency keys enforced with a DynamoDB transaction (a duplicate gets 409 and the existing
job), AWS full-jitter backoff through ChangeMessageVisibility, redrive to a dead-letter queue after
three deliveries with a consumer that records the last error, versioned conditional writes so a slow
worker cannot overwrite newer state, a graceful drain on SIGTERM, and correlation IDs that keep a
failed job traceable across every hop. 106 unit and 19 integration tests run against LocalStack in CI.

`Java 17` `Spring Boot` `AWS SQS/DynamoDB/S3` `Testcontainers` `LocalStack` `Docker` `React`

### [GestureControl](https://github.com/carlous-roy/GestureControl-Engine) · [demo](https://gesture.roycarlous.com)

A control loop from a webcam to a 4-channel relay module. MediaPipe hand landmarks in tracking mode,
a One Euro filter on the coordinates, and finger rules in the hand's own frame with hysteresis and a
three-frame confirmation, so rotation, scale and mirroring do not change the count. The relay path
is fail-safe on every exit, and an Arduino Firmata sketch with a host-loss watchdog releases the
relays within a second if the host disappears. A simulate command replays recorded hands through the
real pipeline, and a JavaScript port shares the rules and golden vectors with the Python tests.
Started as my final-year project in 2022. 537 tests.

`Python` `MediaPipe` `OpenCV` `pyFirmata2` `Arduino`

### [CodeAtlas](https://github.com/carlous-roy/CodeAtlas) · [case study](https://roycarlous.com/case-studies/codeatlas.html)

Semantic search over a codebase, and an evaluation harness that says how well it actually works.
The retrieval is a weekend; the measurement is the project. A corpus pinned by manifest (116 files
across four of my own projects), 36 labelled questions with a dev/test split, six retrieval
strategies by three chunkings, hit rate, recall, nDCG and MRR with 95% bootstrap intervals, and
reruns that reproduce the results byte for byte. Hybrid retrieval beats BM25 on MRR, a per-file cap
lifts recall@5 from 0.57 to 0.65, structural chunking and fixed windows are within noise of each
other, and a stock cross-encoder reranker makes ranking worse. The results that went against what I
expected are in the README with the rest.

`Python` `sentence-transformers` `Tree-sitter` `BM25` `NumPy`

---

<p align="center">
  <a href="https://roycarlous.com">roycarlous.com</a> ·
  <a href="https://www.linkedin.com/in/roy-carlous-c/">LinkedIn</a> ·
  <a href="mailto:roy4edu@gmail.com">roy4edu@gmail.com</a>
</p>
