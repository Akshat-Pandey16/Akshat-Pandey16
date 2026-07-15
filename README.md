<!--
  ┌─────────────────────────────────────────────────────────────────────┐
  │  Copy the entire contents of this file into the README.md of your    │
  │  special profile repo:  github.com/Akshat-Pandey16/Akshat-Pandey16   │
  │  (create that repo if it doesn't exist — it must match your username)│
  │  Everything below the neofetch block is standard GitHub-flavored     │
  │  Markdown and renders on your profile as-is.                         │
  └─────────────────────────────────────────────────────────────────────┘
-->

```text
-      -   --      -  --                 -   +****#*#****
         -   -                -    -+*++***##+*%%%%%%%%##*#*
-                         -  -     +**###***%%%####%#%%%#%%%#*+
 -                   -          - *##%%**###%#####%@@@%%%%%#%%**
     -           -         -       @@@@@@@@@@@@@%%%%%%%@@@@@#%%#*+
          - -                     +%@@@%##*******##%%%%%%%%@%%@@##+
                                 *#%*%# -------  ++**%%%####%%%%@#*+
                                +####%+:::-----    +++*#*****#*%@%*+
                                +*####+-::-------   ++ +++++  - %@#++
                                 *####* -----------   ----     -*%#+
                                 *##*#+-----::::---------   -- -+%#+
                                 *##* ---::-+##****+   +**####*  ***
                                 *##*::: *    +*##*+*+*####*++++-+*+
                                  %##--- **#%#%%*@#++-*%%#@%+%#* +*+
                                +# - ::--+  +*###+ +::-++*##**++ +++
                                ++: -::::: :---  -+:::--       - -++
                                   #--:::::::--+*::---   -* ------++
                                  -- --::::-- +#++#**+**#***   -- ++
                                  -:- ----- +*#*++##%#%%%#***++  ++
                                      ---- +*##%++******* %@#*++ ++      +
                                       ----  +#%@*--:-- +@@%%++  *+                              +
                                     - +   + ++  ------   ++*++ +++                          + +
                                     --*+++++  -  -+****+++ ++++*+
                                     -- *#*++ ------ ++     ++**+                            +
                                     --- *#*#+ --::-  ----  +*++             +   +    +    +
                                     :--- +#%###*+++++++***#**+  +
                                   -:----  +**#%%%@@%%%%@@#+*+                  +
                                *##------   ++*#%%%%%%%@%*+ ++                            + +
                            +*%%##%%%-----   +++*#####***+  #*                              + + +
          +              +##%#%%#%%%@%#--     +++++****++   -%##*                     +
   +                  +#%##%%%%%#%@%%%@@#     ++++++++++    -%%%%%##*                      +    +
        +           #*#%%##%@%%%##%@%%%@@@@    ++++++++     *%@%%@#%%%*#+   +     +              +
        +        **#**#%%###%@%%%#%@%%%@%@@@@%++++ ++++    +%@%@%%@%#%%%#%%*   +           +    +
            *#%#**####%#####%@%%%%%%@%%%@%%@@@@@@%*    + +%@@%%%@%#%%#%@%%%####*          +    ++
          +*#####%###%%##%%%#@%%%%%%%%%%%%%%%%@@@@@@@@@@@@@%%%@%@@%%%%##%@%%%%%%##++ +   +      +
        +*#####%%%%%%%%%%%%%#@%%%%%#%%%%%%%%%%%%%%%@@@@@%%%%@%@%%@@%%%%#%#%@%%%%%%%#+
       *####%%%%%%%%@%%%%%%%%@%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%@%%%%%##%%%@#%%%%%#++       +
     *#####%%%%%%%%@%@%%@%%%%@%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%#%@%%%%%%#+  +  +   +
   ######%%%%%%%%%%@%%@%%@@@%@@%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%#@@%@#%%#+  +   +
  *####%%%%%%%%%%%%@@@@@@@@@%@@%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%@@@%@%*+ +  +  +
++*###%%%%%%%%%%%@%@@@@@@@@@@@%%@%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%@%@@@@%#*+  + ++
 ####%%%%%%%%%@%@%@@@@@@@@@@@%@@%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%#%#%@@@@%%*+ + ++

akshat@github
─────────────────────────────────────────────
Role     Data Platform Engineer @ Intozi Tech
Uptime   2 yrs @ Intozi · coding since 2020
Focus    streaming ingest · async pipelines · MLOps
Langs    Python · SQL · Bash · TypeScript
Stack    FastAPI · Django · PostgreSQL · Redis
Async    Celery · RabbitMQ · ARQ
Stream   MediaMTX (RTSP/WebRTC) · ONVIF · WS · SSE
Data/ML  scikit-learn · scapy · NetworkX
Infra    Docker · Kubernetes · AWS · Nginx · Linux
Edu      B.Tech CS · BIT Durg · CPI 9.68
Award    KAVACH'23 — Govt. of India national winner
Base     Gurugram, IN · remote-friendly
Status   ● open to work
Contact  akshat16pandey@gmail.com
```

> **I build the data & streaming platform behind a computer-vision product.**
> Camera ingestion, async processing pipelines, and the MLOps loop that keeps
> production models fed — I keep the request path thin and push everything heavy
> off to the side. By night I write novels and cut short films.

---

### `~/` The request path

The way I think about a production backend: **keep the request path thin, push everything heavy off it.**

```mermaid
flowchart LR
    C(["Clients<br/>web · RTSP/ONVIF cameras"]) --> N["Nginx"]
    N --> API["API layer<br/>Django · FastAPI"]
    API -->|enqueue jobs| Q{{"Broker<br/>RabbitMQ · Redis"}}
    API <-->|cache · sessions| R[("Redis")]
    API <-->|read · write| PG[("PostgreSQL")]
    Q --> W["Async workers<br/>Celery · ARQ"]
    W -->|video · AI jobs| ML[["CV & video analytics"]]
    W --> PG
    W -->|artifacts| S3[("S3 object storage")]
    MTX["MediaMTX<br/>RTSP → WebRTC"] -->|live feeds| API
    API -.->|real-time| C
    classDef accent stroke:#2bd68a,stroke-width:1.5px;
    class API,W,MTX,ML accent;
```

> Live camera feeds and AI analytics surface in real time, while video-processing
> and ML jobs stay off the request path. This is the shape of the **Video
> Management System** and **Ikshana** work I own at Intozi.

---

### `~/intozi` At Intozi · Jun 2024 – present

Data platform / backend for a computer-vision & video-analytics **product** company. I own the Python services across the product line.

- **Architected the data & async layer** — `PostgreSQL` · `Redis` · `RabbitMQ` · `Celery` — so video-processing and model-inference jobs run off the request path for responsive, scalable services.
- **Built the live-video ingest** for a client-facing **Video Management System** — Django services with **MediaMTX** wired in for RTSP/WebRTC, so camera feeds and AI analytics surface in the app in real time.
- **Built an internal MLOps pipeline** (Django + React): dataset upload → auto-labeling → human verification → training/re-training, with a path to client-facing deployment.

---

### `~/projects` Selected systems

Open-source systems I designed and shipped end-to-end — deeper write-ups live in each repo.

| Project | What it is | Built with |
|---|---|---|
| **[onveef](https://github.com/Akshat-Pandey16/onveef)** | A fast, zeep-free ONVIF client library for IP cameras — discover devices, pull stream URLs, drive PTZ; sans-IO core, imports instantly | `Python` · `httpx` · `sans-IO` |
| **[Papyrus](https://github.com/Akshat-Pandey16/papyrus)** | Self-hostable, privacy-first PDF studio on an async job pipeline — merge / split / compress / OCR with a zero-retention TTL | `FastAPI` · `Celery` · `Redis` · `S3` |
| **[MeshHawk](https://github.com/Akshat-Pandey16/MeshHawk)** | Local-first 802.11 mesh detector — `.pcap` in, topology graph + SVG report out | `FastAPI` · `scapy` · `NetworkX` · `ARQ` |
| **[Hoctor](https://github.com/Akshat-Pandey16/Hoctor)** | Indoor Wi-Fi fingerprint localization — a per-venue random forest predicts the room from surrounding APs | `Django` · `DRF` · `scikit-learn` |
| **[FOSSLove](https://github.com/Akshat-Pandey16/fosslove)** | A FOSS app catalog that builds one cross-distro install script (apt / dnf / pacman / flatpak / winget) | `FastAPI` · `PostgreSQL` · `Redis` · `Next.js` |
| **[HeadTogether](https://github.com/Akshat-Pandey16/HeadTogether)** | Geo-bounded, ephemeral chat rooms discoverable only by people physically nearby | `FastAPI` · `WebSockets` · `Redis` · `Argon2id` |
| **[ShieldBuntu](https://github.com/Akshat-Pandey16/ShieldBuntu)** | One-click Ubuntu CIS hardening — 16 idempotent Ansible roles, apply / dry-run / revert, streamed live to the UI | `FastAPI` · `Ansible` · `SSE` · `PAM` |

---

### `~/toolbox` Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=python,django,fastapi,postgres,redis,docker,kubernetes,linux&theme=dark" alt="Python, Django, FastAPI, PostgreSQL, Redis, Docker, Kubernetes, Linux" />

</div>

| | |
|---|---|
| **Languages** | Python · SQL · Bash · TypeScript |
| **Frameworks** | FastAPI · Django · React |
| **Data & async** | PostgreSQL · Redis · RabbitMQ · Celery · ARQ |
| **Ingest & streaming** | MediaMTX (RTSP/WebRTC) · ONVIF · WebSockets · Server-Sent Events |
| **ML & data** | scikit-learn · scapy · NetworkX |
| **Infra** | Docker · Kubernetes/Helm · Nginx · AWS · Linux · Git |

---

### `~/recognition` Recognition & education

- 🏆 **KAVACH'23** — Winner of the inaugural **nationwide** cybersecurity hackathon organised by the **Government of India**.
- 🎓 **B.Tech, Computer Science** — Bhilai Institute of Technology, Durg · **CPI 9.68** (2020 – 2024).

### `~/offline` Beyond the terminal

A published **author** — a novelette and two novels — and I **shoot & edit short films**. Same discipline as backend work: structure, revision, pacing, and deciding what to leave out.

---

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-2bd68a?style=for-the-badge&logo=netlify&logoColor=04140c)](https://akshat16pandey.netlify.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akshat16pandey/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:akshat16pandey@gmail.com)

<sub><i>Thin request path. Heavy lifting off to the side. Same goes for the README — thanks for scrolling.</i></sub>

</div>
