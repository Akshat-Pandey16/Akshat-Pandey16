<!-- ============================ HEADER ============================ -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rounded&color=0:0d1117,100:00451f&height=160&section=header&text=Akshat%20Pandey&fontSize=46&fontColor=00d668&animation=fadeIn&fontAlignY=40&desc=Backend%20Lead%20%E2%80%A2%20Python%20%E2%80%A2%20Async%20%26%20Real-time%20Systems&descAlignY=62&descSize=16&descColor=c9d1d9" alt="Akshat Pandey — Backend Lead, Python, Async & Real-time Systems" width="100%" />

[![Lead Backend @ Intozi](https://img.shields.io/badge/Lead_Backend-Intozi_Tech-00d668?style=flat-square&labelColor=0d1117)](https://github.com/Akshat-Pandey16)
[![KAVACH'23 National Winner](https://img.shields.io/badge/KAVACH'23-National_Winner_·_Govt._of_India-00d668?style=flat-square&labelColor=0d1117)](#recognition-and-education)
![BTech CS · CPI 9.68](https://img.shields.io/badge/BTech_CS-CPI_9.68-00d668?style=flat-square&labelColor=0d1117)
![Based in Gurugram, IN](https://img.shields.io/badge/Based_in-Gurugram,_IN-58a6ff?style=flat-square&labelColor=0d1117)

</div>

> **I lead the Python backend at a computer-vision product company** — designing the async, streaming, and data layers that production AI workloads run on. By night, I write novels and cut short films.

---

## The request path

The way I think about a production backend: **keep the request path thin, push everything heavy off it.**

```mermaid
flowchart LR
    C(["Clients<br/>web and RTSP cameras"]) --> N["Nginx"]
    N --> API["API layer<br/>Django and FastAPI"]
    API -->|enqueue jobs| Q{{"Broker<br/>RabbitMQ and Redis"}}
    API <-->|cache and sessions| R[("Redis")]
    API <-->|read and write| PG[("PostgreSQL")]
    Q --> W["Async workers<br/>Celery and ARQ"]
    W -->|video and AI jobs| ML[["CV and video analytics"]]
    W --> PG
    W -->|artifacts| S3[("S3 object storage")]
    MTX["MediaMTX<br/>RTSP to WebRTC"] -->|live feeds| API
    API -.->|real-time| C
    classDef accent stroke:#00d668,stroke-width:1.5px;
    class API,W,MTX,ML accent;
```

> Live camera feeds and AI analytics surface in real time, while video-processing and ML jobs stay off the request path. This is the shape of the **Video Management System** and **Ikshana** work I own at Intozi.

---

## By the numbers

<div align="center">

<table>
<tr>
<td align="center" width="20%">

### `4`
**backends**<br/><sub>shipped · open-source</sub>

</td>
<td align="center" width="20%">

### `73`
**REST routes**<br/><sub>HeadTogether</sub>

</td>
<td align="center" width="20%">

### `20`
**ORM tables**<br/><sub>layered repos</sub>

</td>
<td align="center" width="20%">

### `16`
**Ansible roles**<br/><sub>idempotent · CIS</sub>

</td>
<td align="center" width="20%">

### `🏆`
**KAVACH'23**<br/><sub>Govt. of India</sub>

</td>
</tr>
</table>

</div>

---

## At Intozi  ·  Jun 2024 – present

Lead backend at a computer-vision & video-analytics **product** company. I own the Python services across the products and coordinate delivery within a small team.

> [!NOTE]
> **Currently building** the backend for a client-facing **Video Management System** — Django services with **MediaMTX** wired in for RTSP/WebRTC, so live camera feeds and AI analytics surface in the app in real time.

- **Own the Python services** across the company's products, including **Ikshana**, its core video-analytics product.
- **Architected the data & async layers** — `PostgreSQL` · `Redis` · `RabbitMQ` · `Celery` — to run video-processing jobs and AI workloads off the request path for responsive, scalable services.
- **Built an internal MLOps pipeline** (Django + React): dataset upload → auto-labeling → human verification → training/retraining, with a path to client-facing deployment.

---

## Selected systems

Four backends I designed and shipped end-to-end — deeper write-ups live in each repo.

| Project | What it is | Built with |
|---|---|---|
| **[Papyrus](https://github.com/Akshat-Pandey16/papyrus)** | Self-hostable, privacy-first PDF studio — merge / split / compress / OCR with a zero-retention TTL | `FastAPI` · `Celery` · `S3` · `Compose + Helm` |
| **[HeadTogether](https://github.com/Akshat-Pandey16/HeadTogether)** | Geo-bounded, ephemeral chat rooms discoverable only by people physically nearby | `FastAPI` · `WebSockets` · `Redis pub/sub` · `Argon2id` |
| **[ShieldBuntu](https://github.com/Akshat-Pandey16/ShieldBuntu)** | One-click Ubuntu CIS hardening — apply / dry-run / revert, streamed live to the UI | `FastAPI` · `Ansible` · `SSE` · `PAM` |
| **[MeshHawk](https://github.com/Akshat-Pandey16/MeshHawk)** | Local-first 802.11 mesh detector — `.pcap` in, topology graph + SVG report out | `FastAPI` · `scapy` · `NetworkX` · `ARQ` |

---

## Toolbox

<div align="center">

<img src="https://skillicons.dev/icons?i=python,django,fastapi,postgres,redis,docker,linux&theme=dark" alt="Python, Django, FastAPI, PostgreSQL, Redis, Docker, Linux" />

</div>

| | |
|---|---|
| **Languages** | Python · Bash |
| **Frameworks** | Django · FastAPI |
| **Data & async** | PostgreSQL · Redis · RabbitMQ · Celery · ARQ |
| **Streaming & real-time** | MediaMTX (RTSP/WebRTC) · WebSockets · Server-Sent Events |
| **Infra** | Docker · Kubernetes/Helm · Nginx · AWS · Linux · Git |

---

## Beyond the terminal

Engineering isn't the only thing I ship. I'm a published **author** — a novelette and **two novels** — and I **shoot and edit short films**. Both are the same discipline as backend work: structure, revision, pacing, and deciding what to leave out.

### Recognition and education

- 🏆 **KAVACH'23** — Winner of the inaugural **nationwide** cybersecurity hackathon organised by the **Government of India**.
- 🎓 **B.Tech, Computer Science** — Bhilai Institute of Technology, Durg · **CPI 9.68** (2020 – 2024).

---

## GitHub activity

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=Akshat-Pandey16&show_icons=true&hide_rank=true&hide=issues&include_all_commits=true&count_private=true&hide_border=true&bg_color=0d1117&title_color=00d668&icon_color=00d668&text_color=c9d1d9" alt="GitHub stats" />
<img height="170" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Akshat-Pandey16&theme=github_dark" alt="Most-used languages by commits" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Akshat-Pandey16&bg_color=0d1117&color=00d668&line=00d668&point=ffffff&area=true&hide_border=true&height=300" alt="Contribution activity graph" width="100%" />

</div>

---

## Connect

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/akshat-pandey-001a53147)
[![Portfolio](https://img.shields.io/badge/Portfolio-00d668?style=for-the-badge&logo=netlify&logoColor=white)](https://akshat16pandey.netlify.app/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:akshat16pandey@gmail.com)
[![X](https://img.shields.io/badge/X_(Twitter)-000000?style=for-the-badge&logo=x&logoColor=white&labelColor=00d668)](https://twitter.com/akshatpandey160)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/c/akshatpandey)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/akshat._.pandey)

<br/>

<sub><i>Thin request path. Heavy lifting off to the side. Same goes for the README — thanks for scrolling.</i></sub>

</div>
