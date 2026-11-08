# Awesome-User-Polling-Quick-Decision-Making

# Awesome User Polling & Quick Decision Making

> A curated list of top User Polling and Quick Decision Making platforms — both SaaS/Hosted commercial solutions and open-source alternatives for live audience polling, scheduling polls, and rapid group decisions.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Poll Everywhere](#poll-everywhere)
  - [Slido](#slido)
  - [Mentimeter](#mentimeter)
  - [Kahoot!](#kahoot)
  - [Doodle](#doodle)
  - [StrawPoll](#strawpoll)
  - [Polly for Teams](#polly-for-teams)
  - [Typeform Opinion Scale](#typeform-opinion-scale)
- [Open-Source Software](#-open-source-software)
  - [Rallly](#rallly)
  - [Claper](#claper)
  - [Bitpoll](#bitpoll)
  - [Framadate](#framadate)
  - [Librepolls](#librepolls)
  - [QikPoll](#qikpoll)
  - [Prashna](#prashna)
  - [Polly (manfredsteger)](#polly-manfredsteger)
  - [open.mentimeter](#openmentimeter)
  - [CEDIS Deck Manager](#cedis-deck-manager)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted User Polling and Quick Decision Making platforms. These are not open-source but are included as reference points for feature comparison.

### Poll Everywhere
**Type:** Live audience polling and engagement  
Poll Everywhere is a long-standing platform for live polling during presentations, meetings, and classes. Supports multiple choice, open-ended, word clouds, Q&A, and surveys. Participants respond via web, SMS, or app. It is a direct commercial reference point for open-source alternatives like CEDIS Deck Manager [citation:9].

### Slido
**Type:** Q&A and live polling for meetings  
Slido (Cisco) focuses on live Q&A, polls, and quizzes integrated into video conferencing tools. Widely used for meetings and events to collect questions and gauge audience sentiment in real time. Open-source alternatives explicitly position themselves against Slido, including Claper [citation:1].

### Mentimeter
**Type:** Interactive presentations and live polling  
Mentimeter enables presenters to create interactive slides with polls, word clouds, quizzes, and Q&A. Participants respond from their phones. A frequent reference point for open-source alternatives like Claper and open.mentimeter [citation:1][citation:14].

### Kahoot!
**Type:** Gamified quizzes and live competitions  
Kahoot! is the dominant gamified quiz platform for classrooms and training. Participants compete on leaderboards in real time. Open-source alternatives exist for education-focused use cases, including CEDIS Deck Manager and Prashna [citation:9][citation:13].

### Doodle
**Type:** Scheduling polls for group availability  
Doodle is the most recognized tool for finding a meeting time across a group. Participants vote on proposed dates without needing accounts. Rallly is the most direct open-source alternative to Doodle [citation:2][citation:3].

### StrawPoll
**Type:** Quick anonymous polls  
StrawPoll provides instant, no-signup polls for quick decisions. Librepolls is explicitly inspired by the now-defunct StrawPoll.me, and QikPoll is described as a "StrawPoll-style" app [citation:5][citation:11].

### Polly for Teams
**Type:** Polling within Microsoft Teams  
Polly integrates directly into Microsoft Teams for quick polls, surveys, and scheduling within the chat interface. Microsoft provides sample code for building custom Teams polling apps, though these are samples rather than production alternatives [citation:6][citation:12].

### Typeform Opinion Scale
**Type:** Survey-based opinion collection  
Typeform's Opinion Scale is a survey question type for collecting rated feedback rather than live polling. It is included here as a reference point for the broader "quick decision" category, though it is not a live polling tool.

---

## 🟩 Open-Source Software

Self-hosted, community-driven User Polling and Quick Decision Making tools. The open-source ecosystem splits into **scheduling polls** (Rallly, Bitpoll, Framadate) and **live audience interaction** (Claper, Prashna, open.mentimeter).

### Rallly
**Stack:** Next.js / TypeScript / Prisma / PostgreSQL | **License:** AGPLv3 [citation:3]  
Rallly is the leading open-source alternative to Doodle, focused on **scheduling polls**. Create a poll with proposed dates, share the link, and participants vote without creating accounts [citation:2][citation:3]. Features include an availability grid, comments on the poll, notifications, finalizing a date with calendar invites, and support for 10+ languages [citation:3]. Self-hosting is supported via Docker with PostgreSQL and optional MinIO for storage [citation:2].  
**Best for:** Teams and organizers needing a self-hosted Doodle replacement for meeting scheduling without participant accounts.

### Claper
**Stack:** (Check repository) | **License:** (Check repository)  
Claper is explicitly described as an open-source alternative to Slido, AhaSlides, and Mentimeter [citation:1]. It targets live audience interaction during presentations and events. Available for self-hosting.  
**Best for:** Presenters wanting a self-hosted Slido/Mentimeter alternative for live polls and audience engagement.

### Bitpoll
**Stack:** Python / Docker | **License:** GPL-3.0 [citation:1]  
Bitpoll is a self-hosted tool for conducting polls about dates, times, or general questions. It sits in the same category as Rallly and Framadate for scheduling and decision-making polls. Deployable via Docker [citation:1].  
**Best for:** Teams wanting a straightforward self-hosted scheduling poll tool with a GPL license.

### Framadate
**Stack:** PHP | **License:** (Check repository)  
Framadate is a long-standing open-source online service for planning appointments or making decisions quickly. Users create a poll, define dates or subjects, share the link, and participants discuss and decide [citation:1]. It is a simpler, established alternative in the scheduling poll space.  
**Best for:** Organizations wanting a proven, lightweight scheduling poll tool without modern JavaScript dependencies.

### Librepolls
**Stack:** Laravel / PHP / Docker | **License:** AGPLv3 [citation:5]  
Librepolls allows creating and voting on polls without registering accounts, inspired by the defunct StrawPoll.me [citation:5]. Supports single or multiple choices per poll, with vote restriction options based on IP or browser. Deployable via Docker Compose. Configuration variables control poll limits (max choices, title length, slug length) [citation:5].  
**Best for:** Teams wanting a simple, anonymous StrawPoll-style polling tool that can be self-hosted.

### QikPoll
**Stack:** Bun / TypeScript / React / Redis | **License:** (Check repository)  
QikPoll is a StrawPoll-style app for fast, no-signup polling with **live vote updates via WebSockets** [citation:11]. Create polls with 2–8 options, choose public or private visibility, and watch results update in real time. Uses Redis for storage with TTL expiration and includes anti-repeat guardrails. Exposes an MCP endpoint (`/api/mcp`) with tools like `create_poll` and `list_public_polls` for AI agent integration [citation:11].  
**Best for:** Developers wanting a modern, real-time anonymous polling tool with MCP/AI agent accessibility.

### Prashna
**Stack:** Python (local executable) | **License:** MIT [citation:13]  
Prashna is a local-first live Q&A and quiz tool for sessions with an audience (training, lectures, workshops, town halls). Two core features: **anonymous Q&A** with participant upvoting, and **moderator-run quizzes** with single/multiple choice and versioned results [citation:13]. Runs on your own laptop with no server or subscription — one command installs it. Supports Cloudflare/ngrok tunnels so audiences can reach it over the internet. Includes a projector view with join code and QR code.  
**Best for:** Educators and presenters wanting a zero-infrastructure, privacy-respecting Q&A and quiz tool that runs entirely on their own machine.

### Polly (manfredsteger)
**Stack:** React / Express / PostgreSQL / Docker | **License:** (Check repository)  
Polly is a modern self-hosted polling and scheduling app for teams. Supports schedule polls, surveys, and booking lists with email-based voting, real-time results via WebSockets, PDF export, and QR code sharing [citation:8]. Includes an API with OpenAPI specification, ICS calendar export, and a roadmap that includes AI voice/agentic poll creation and Keycloak SSO [citation:8]. Deploys via Docker with no cloud dependencies. Currently in beta.  
**Best for:** Teams wanting a feature-rich self-hosted polling platform with scheduling, surveys, and real-time results in one tool.

### open.mentimeter
**Stack:** React / Node.js / Socket.io | **License:** MIT [citation:14]  
open.mentimeter is a local-first Mentimeter alternative designed to run entirely over **local networks with zero cloud dependencies** [citation:14]. The presenter's laptop acts as the server; participants connect via browser. Features include live multiple-choice quizzes with speed bonuses, word clouds, Q&A with upvoting, a presenter remote view, and Excel export. Works offline over local Wi-Fi or mobile hotspot.  
**Best for:** Trainers and educators in offline or privacy-sensitive environments needing live interactive quizzes without internet access.

### CEDIS Deck Manager
**Stack:** Docker / Linux VPS | **License:** MIT [citation:9]  
CEDIS Deck Manager is an open-source alternative to Kahoot, Mentimeter, Slido, and Poll Everywhere, built for educational use [citation:9]. Publishes interactive HTML presentations with activity control policies (always open, class window, presenter only, scheduled), privacy-by-design anonymization (no tracking cookies, IP truncation, DNT respect), and learning analytics dashboards. Includes an AI-assisted presentation-generation skill for Claude/ChatGPT. Self-hosted on any Linux VPS with Docker.  
**Best for:** Educational institutions wanting a self-hostable, privacy-compliant alternative to commercial classroom polling platforms.

---

## 📊 Comparison at a Glance

| Software | License | Poll Type | No-Account Voting | Real-Time Results | Self-Hosted | Best For |
|----------|---------|-----------|-------------------|-------------------|-------------|----------|
| **Poll Everywhere** | Proprietary | Live audience | ✅ | ✅ | ❌ | Live presentations |
| **Slido** | Proprietary | Q&A + polls | ✅ | ✅ | ❌ | Meeting engagement |
| **Mentimeter** | Proprietary | Interactive slides | ✅ | ✅ | ❌ | Presentations |
| **Kahoot!** | Proprietary | Gamified quizzes | ✅ | ✅ | ❌ | Classroom competition |
| **Doodle** | Proprietary | Scheduling | ✅ | (Async) | ❌ | Meeting scheduling |
| **StrawPoll** | Proprietary | Quick polls | ✅ | (Async) | ❌ | Instant decisions |
| **Rallly** | AGPLv3 | Scheduling | ✅ | (Async) | ✅ | Doodle replacement |
| **Claper** | (Check) | Live audience | (Check) | ✅ | ✅ | Slido/Menti alternative |
| **Bitpoll** | GPL-3.0 | Scheduling/general | (Check) | (Async) | ✅ | Self-hosted scheduling |
| **Framadate** | (Check) | Scheduling | ✅ | (Async) | ✅ | Simple proven scheduling |
| **Librepolls** | AGPLv3 | Quick polls | ✅ | (Async) | ✅ | StrawPoll replacement |
| **QikPoll** | (Check) | Quick polls | ✅ | ✅ (WebSocket) | ✅ | Real-time anonymous polls |
| **Prashna** | MIT | Q&A + quizzes | ✅ | ✅ | ✅ (local) | Local Q&A/quiz tool |
| **Polly (manfred)** | (Check) | Scheduling/surveys | ✅ (email) | ✅ | ✅ | All-in-one team polling |
| **open.mentimeter** | MIT | Quizzes/word clouds | ✅ | ✅ | ✅ (LAN) | Offline live polling |
| **CEDIS Deck Manager** | MIT | Educational polling | ✅ | ✅ | ✅ | Education + privacy |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source User Polling or Quick Decision Making tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
