<h1 align="center">Roy Carlous Christudass</h1>

<p align="center">
  <a href="https://roycarlous.com">
    <img src="https://readme-typing-svg.herokuapp.com/?font=JetBrains+Mono&size=22&duration=3500&pause=1000&color=DC2626&center=true&vCenter=true&width=720&lines=Software+Engineer;Data+analysis%2C+machine+learning+and+backend+systems" alt="Software Engineer. Data analysis, machine learning and backend systems." />
  </a>
</p>

<p align="center">
  <a href="https://roycarlous.com"><img src="https://img.shields.io/badge/Portfolio-roycarlous.com-DC2626?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/roy-carlous-c/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:roy4edu@gmail.com"><img src="https://img.shields.io/badge/Email-roy4edu%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

---

## About

I'm a software engineer working on data analysis, machine learning and the systems around them.
Most of what I build ends up the same shape: data coming in, a model or some logic over it, a
measurement of how well that works, and an API and a front end someone actually uses. In the
projects below that means a change-risk model scored on held-out commits, a retrieval evaluation
with a bootstrap interval on every metric, and SQL reports whose summaries are tested against their
rows. I like working across all of it rather than owning one layer.

Before my master's I spent January 2022 to August 2024 at HCLTech, contracted to Teradyne, and was
promoted twice in two years. I got into data work there: I built the team's first Power BI
dashboard on a SQL Server mirror of Jira, tracking defect velocity and backlog age, and later ran
the defect dashboards in client-facing calls, where mean time to resolution and defect clusters by
platform, module and instrument set code-review and staffing priorities. I also wrote the Python
tooling that pulled call stacks out of crash dumps and compared profiler reports across nightly
builds to flag memory and execution-time regressions. The codebase was the C++ and C#/.NET
instrument drivers behind Teradyne's IG-XL test platform. That software controlled physical
hardware, so bugs were expensive and I got good at tracing them, and I ended up owning the customer
escalations the dashboards tracked.

I finished my M.S. in Computer Science at Wright State University in August 2026 and I'm looking
for a full-time role in data analysis, data science or software engineering.

Open to relocation anywhere in the US. Reach me at **roy4edu@gmail.com**.

---

## Tech stack

<p align="center"><strong>Languages</strong></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=python,java,cpp,cs,js,html,css" alt="Python, Java, C++, C#, JavaScript, HTML, CSS" />
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

---

## Projects

Three have browser demos and one, CodeAtlas, has a written case study. The code for each is public,
and every number below is reproduced by the tests or the evaluation script in its repository.

### [DiffLens](https://github.com/carlous-roy/DiffLens-Engine) · [demo](https://difflens.roycarlous.com)

A code review service built around a gradient-boosted change-risk model trained on ApacheJIT
(106,674 commits from 15 Apache projects) with a per-project temporal split and isotonic
calibration. Held-out ROC-AUC 0.80, PR-AUC 0.468 and Brier 0.134 against 0.160 for a constant
prediction, with per-feature attributions and a generated model card. Tree-sitter builds ASTs for
Python and Java and measures cyclomatic complexity and nesting depth, with rules that never fire
inside comments or strings. Findings are embedded into pgvector to count repeats, GitHub webhooks
post inline pull-request comments, and an optional local model through Ollama adds review comments.
291 tests.

`Python` `scikit-learn` `pandas` `PostgreSQL/pgvector` `FastAPI` `Tree-sitter` `React` `Docker` `Ollama`

### [CodeAtlas](https://github.com/carlous-roy/CodeAtlas) · [case study](https://roycarlous.com/case-studies/codeatlas.html)

A retrieval evaluation harness and the semantic code search it measures. The retrieval part is
small; the measurement is the project. A corpus pinned by manifest (116 files across four of my own
projects), 36 labelled questions with a dev/test split, six retrieval strategies by three
chunkings, and hit rate, recall, nDCG and MRR with a 95% bootstrap interval on every metric. Reruns
reproduce the results byte for byte, and CI fails if the published tables and the results files
disagree. Hybrid retrieval beats BM25 on MRR, a per-file cap lifts recall@5 from 0.57 to 0.65,
structural chunking and fixed windows are within noise of each other, and a stock cross-encoder
reranker makes ranking worse.

`Python` `NumPy` `sentence-transformers` `BM25` `Tree-sitter`

### [TaskForge](https://github.com/carlous-roy/TaskForge-Engine) · [demo](https://taskforge.roycarlous.com)

Distributed report generation. Three reports (sales by product and region, inventory value with a
low-stock flag, per-user and hourly activity) run in SQL over a seeded sample dataset; requests
queue through SQS to independent workers, and the CSV lands in S3 behind presigned URLs. Most of
the code handles what happens when something breaks: idempotency keys enforced with a DynamoDB
transaction (a duplicate gets 409 and the existing job), full-jitter backoff, redrive to a
dead-letter queue after three deliveries, versioned conditional writes, a graceful drain on
SIGTERM, and correlation IDs across every hop. 106 unit tests and 19 integration tests against
LocalStack in CI.

`Java 17` `SQL (H2)` `Spring Boot` `AWS SQS/DynamoDB/S3` `Testcontainers` `LocalStack` `Docker` `React`

### [GestureControl](https://github.com/carlous-roy/GestureControl-Engine) · [demo](https://gesture.roycarlous.com)

A control loop from a webcam to a 4-channel relay module. MediaPipe hand landmarks, a One Euro
filter on the coordinates, and finger rules in the hand's own frame with hysteresis and three-frame
confirmation, so rotation, scale and mirroring do not change the count. A bench command reports
median and 95th-percentile latency by stage, a simulate command replays recorded hands, and a
JavaScript port shares the rules and golden vectors with the Python tests. The relay path is
fail-safe on every exit, and an Arduino Firmata watchdog releases the relays within a second if the
host disappears. Started as my final-year project in 2022. 537 tests.

`Python` `MediaPipe` `OpenCV` `pyFirmata2` `Arduino`

---

<p align="center">
  <a href="https://roycarlous.com">roycarlous.com</a> ·
  <a href="https://www.linkedin.com/in/roy-carlous-c/">LinkedIn</a> ·
  <a href="mailto:roy4edu@gmail.com">roy4edu@gmail.com</a>
</p>
