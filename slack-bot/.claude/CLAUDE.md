# User Context
- Name: Iwan Mota, goes by Iwan (pronounced "Ivan" — Brazilian Portuguese)
- Role: Engineering Manager, Road Safety & Telematics team
- Org: Risk Engineering & Product, under Risk Solutions
- VP: Lin Xing — VP, Head of Risk
- Location: Toronto, Canada (Toronto Coworking, 5th Floor, 357 Bay St.)
- Timezone: America/Toronto
- GitHub: iwanmota-lyft
- GitHub repos base path: ~/src
- Slack: iwanmota (U0A3084QX5E)

# Team

## Direct Reports
- Masroor Ahmed — Senior Software Engineer
- Daniel Briones Pérez — Senior Software Engineer
- Arundhati Navada — Senior Software Engineer
- Joon Lee — Software Engineer
- Sharun Garg — Software Engineer
- Haomin Shi — Software Engineer
- Billy Su — Software Engineer
- Kyle Jang — Software Engineer
- Oleksandr Reshetar — Software Engineer
- Ryan Maksymic — Software Engineer

## Manager
- Eugene Kirvel — Senior Engineering Manager (SF office, America/Los_Angeles)

## Peers (also report to Eugene)
- Stanislav Rashevskyi (Stan) — Engineering Manager, FNOL Tech
- Yazhou Xun — Engineering Manager
- Vinyas Kedigehalli — Staff Software Engineer
- Maksim Zhuk — Staff Software Engineer (also on RST oncall rotation)
- Qi Leng — Senior Data Scientist
- Kyle Liu — Senior Data Scientist
- Spencer Christiansen — Data Scientist
- Nagadarshan Narasimhamurthy — Software Engineer, Test

## On-Call Rotation Members (Road Safety + Telematics)
- Maksim Zhuk (EE) — Server Engineer
- Arundhati Navada — Server Engineer, Telematics
- Daniel Briones — Server Engineer, Road Safety
- Joon Lee — Server Engineer, Road Safety
- Billy Su — Server Engineer, Telematics

Ping *familybot* slack app with "oncall Road Safety + Telematics" for current on-call.
Each member has a 24/7 shift. High urgency: 9 AM–5 PM PST ("office hours").
Outside that, most incidents are low urgency (can wait until next day).

# Key Repos

## Road Safety
- lyft/roadsafetyinfo — road safety services repo + cron jobs
- lyft/roadsafetydata — feature flags & config (Dynamex-based), consumed by roadsafetyinfo
- lyft/drivermonitor — monitors driver behavior events, owns auto-offboarding
- lyft/featurebuilderdata — dsfeatures definitions; RS owns `data/conf/fs2/road_safety/`
- lyft/ridexppredictor — interventions service; smooth cruiser alerts/reminders live in `app/actions/proactive_intervention/road_safety/`
- lyft/dashboards — grafana dashboards config

## Telematics
- lyft/telematicsingest — telematics data ingestion service
- lyft/telematicsairflow — airflow DAGs for telematics pipelines
- lyft/Telematics-lyftlearn-tasks — data processing tasks on LyftLearn (invoked from Airflow)
- lyft/python-lyft-telematics-data — interfaces for consuming raw telematics data (pypi: lyft-telematics-data)
- lyft/python-lyft-telematics-algorithms — algorithms for processing high-frequency telematics data (pypi: lyft-telematics-algorithms)
- lyft/telematicsmodels — analysis notebooks

## Mobile (shared ownership with mobile teams)
- lyft/instant-android — Android app; RST owns: `smooth-cruiser`, `road-safety-offboard`, `handheld-phone-use` modules
- lyft/Lyft-iOS — iOS app; RST owns: `SmoothCruiser*`, `RoadSafetyOffboarding`, `HandheldPhoneUseAlerting`, and code tagged `road_safety_and_telematics`

## IDL
- lyft/idl — TelematicsReport proto definition at `protos/pb/api/models/v1/telematics/telematics_report.proto`

# PagerDuty

Team: Risk Solutions Tech (ID: PBTAWMH)
Primary escalation policy: PCNNDW1

Key services owned by Road Safety + Telematics:
- roadsafetyinfo, roadsafetydata
- road-safety-reminders — in-app road safety reminders via DSFeatures
- road-safety-smooth-cruiser — smooth cruiser driver feedback via DSFeatures
- safety-offboarding — safety offboarding alarms (part of drivermonitor)
- dispatch-safety — integrations between insurance and dispatch/matching
- glm-score / glm-score-high-urgency — GLM model failures (ICAD)
- telematicsingest, telematicsairflow, telematicslyftlearntasks
- telematicsviztool — Telematics Visualization Tool (TVT)
- telematics-airflow-jobs, telematics-sox-data-quality
- riskdocs
- accidentlabels
- client-telematics-android, client-telematics-ios

# Active Projects
Always look up dynamically — do not hardcode.
- Risk Tech Project Tracker (source of truth):
  https://docs.google.com/spreadsheets/d/1Ys6VEobOONitWTIZaHG8baX_Va_IOuVzTYJPiCXvoC8/edit

# JIRA
- Telematics board: https://jira.lyft.net/secure/RapidBoard.jspa?rapidView=2010&projectKey=TELEMATICS
- Road Safety board: https://jira.lyft.net/secure/RapidBoard.jspa?rapidView=2009

# Slack Channels

## Core Team Channels
- #road-safety-telematics-team (C0A90DB2SFM) — main team channel (Iwan's reports + Eugene's Toronto reports)
- #road-safety-telematics-leads (C0A4LNPQB70) — leads channel
- #rst-oncall (C02H0EA1H5L) — oncall rotation alerts

## Engineering Channels
- #road-safety-eng (G015DD6E41W) — road safety engineering
- #telematics-eng (G014GD7HG69) — telematics engineering (private)
- #core-telematics-eng (GK4NNGWHY) — core telematics engineering
- #telematics-all (C016Y7FKR2Q) — broader telematics stakeholders
- #telematics-bots (C019KAR41C5) — telematics bot alerts
- #risk-knowledge-sharing (C0407MNN69W) — cross-team knowledge sharing

## Project Channels
- #smooth-cruiser-v3-m1 (C0AN4JDUH47) — Smooth Cruiser v3 milestone 1 (active)
- #acpriv-smooth-cruiser-core (C028X8KHSAE) — Smooth Cruiser core
- #smooth-cruiser-uxr (C0A1WEXS4KH) — Smooth Cruiser UX research
- #speed-limits-smooth-cruiser-integration (C0A79Q38LJ1) — speed limits integration
- #road-safety-feedback-campaign (C07TEVBP85V) — feedback campaign project
- #road-safety-offboarding (GQUSAF9QX) — offboarding discussions

## Bug Channels
- #android-road-safety-and-telematics-bugs (C086SU00T50)
- #ios-road-safety-and-telematics-bugs (C086VEKCJ5A)

# How We Work
- Road Safety Standup notes: https://docs.google.com/document/d/1W5l5pzwbYtmkbHUYjjXzaCzYNH6llxft3GS-3lV6Nz8/edit
- Telematics Weekly Meeting Notes: https://docs.google.com/document/d/17hyKxHuE25GIEdmsX3zW-uxywaXVZHQXDBC5_a2ybzI/edit

Core principles:
- Own problems end-to-end & full-stack
- Champion your own projects
- Think in impact, not output — measure what changes in the business
- Prioritize ruthlessly for highest ROI
- Predictability earns trust for ambitious work

# Preferences
- Ask clarifying questions before diving in — understand context, constraints, goals first
- Make changes incrementally, one logical step at a time
- Explain what you're doing and why at each step before showing code
- Prefer clear, maintainable solutions over clever ones
- When multiple approaches exist, briefly outline tradeoffs before proceeding
- Brief, direct communication style
- Evidence-based analysis over high-level estimates
- Prefers grounded, codebase-level analysis
- Interested in learning more about architecture and internal tech stack
- Cares that team works on highest-impact (best ROI) projects, supported by data-driven metrics
- Defines impact and opportunities with data; uses data to identify problems
- Full-stack experience, EM role

# Reference Documents

## Onboarding & Team Guides
- Telematics Tech Onboarding Guide:
  https://docs.google.com/document/d/13FmS6F1fh9UblM2nPg9AqxvoS4HDT5OeJVhXZsi3Sy8/edit
- Road Safety Tech Onboarding Guide:
  https://docs.google.com/document/d/1buUJNcB6829NtZrJ1kl07X20CGet9S-5njo6geHM41Q/edit
- Risk Tech Team Onboarding:
  https://docs.google.com/document/d/1ku82KMu_PzuAbm95Mr1xjyHBeEGE7jb7U9mZslM1s58/edit
- Telematics References (master doc with ~100 links):
  https://docs.google.com/document/d/1W-Cd7qWd3xX-mkdnIQ_eie1bQbuWpUWAhF4IMxJ7Obk/edit

## Domain Knowledge
- Lyft Insurance Dictionary:
  https://lyft.atlassian.net/wiki/spaces/INS/pages/315785264/Lyft+Insurance+Dictionary
- Lyft-tionary:
  https://lyft.atlassian.net/wiki/spaces/ENG/pages/84247020/Lyft-tionary
- An Engineer's Crash Course to Insurance & Risk:
  https://docs.google.com/document/d/16ueQoKNvYd4g5D8ccJXCs4m8rz1g_gatA2rxzlM2SGQ

## Key Technical Docs
- Telematics End-to-End (eng doc):
  https://docs.google.com/document/d/1Cug8owKPJ6f26MKxQBYcR8WBpdmabgjpMj349tb0_Cc/edit
- Lyft Telematics User Guide (Model Tables):
  https://docs.google.com/document/d/1Q8aNukt91YHhHY1zJhMf33pUfKl0TJ9gI17DbT8tE84/edit
- Telematics Overview:
  https://docs.google.com/document/d/12joWY5Tqlh7m5hezfLI96IE24YbsKrIdx_PdH3GBf8I/edit

## Tools
- Sourcegraph: https://sourcegraph.lyft.net/search (code search)
- LyftLearn: https://ml.lyft.net/ (ML platform)
- Mode: go/mode (queries & visualizations)
- Spellbook: go/sql (ad-hoc SQL/Spark)
- TCS: go/tcs (experimentation)
- Grafana dashboards:
  - Telematicsingest: https://grafana.lyft.net/d/H25ayeEWz/telematicsingest
  - Telematics Pipeline: https://grafana.lyft.net/d/HjUnUeEWk/telematics-pipeline

# Workflows

## Daily Slack Digest

Review unread Slack messages across key channels and DMs for the relevant lookback window:
- **Tuesday–Friday:** last 24 hours
- **Monday:** since end of Friday (i.e. cover Saturday + Sunday + Monday so no weekend activity
  is missed)

Produce a bullet-point summary of action items prioritized by:
1. Was Iwan tagged directly (`<@U0A3084QX5E>`)?
2. Is it an action item attributable to Iwan?
3. Is it something that should interest Iwan?
4. Was it sent by someone in his immediate circle (directs, manager, peers) AND/OR is it
   relevant to one of his active projects?

For each item include a citation link to the original Slack message so Iwan can drill down.

### Channels to check (in addition to DMs and group DMs)
- #road-safety-telematics-team (C0A90DB2SFM)
- #road-safety-telematics-leads (C0A4LNPQB70)
- #rst-oncall (C02H0EA1H5L)
- #road-safety-eng (G015DD6E41W)
- #telematics-eng (G014GD7HG69)
- #smooth-cruiser-v3-m1 (C0AN4JDUH47)
- #road-safety-feedback-campaign (C07TEVBP85V)
- #telematics-all (C016Y7FKR2Q)
- #android-road-safety-and-telematics-bugs (C086SU00T50)
- #ios-road-safety-and-telematics-bugs (C086VEKCJ5A)

### Searching for messages
- Use `after:YYYY-MM-DD` in search queries. Note: this modifier is **exclusive** — to include
  messages *on* a given date, use the day before (e.g. to include Apr 1, use `after:2026-03-31`).
- Use `oldest` (Unix timestamp) when reading channels directly to bound the time window.

### Generating citation links — CRITICAL RULE
Slack permalink format: `https://lyft.slack.com/archives/{channel_id}/p{message_ts_no_dot}`

The `message_ts` value (e.g. `1775059522.084149`) becomes `p1775059522084149` — remove the
decimal point, **do not pad with zeros**.

**Always obtain `message_ts` from actual tool results** (e.g. `slack_read_channel` with
`response_format: detailed`, or from search result `Message_ts` fields). Never compute or
approximate a timestamp from a wall-clock time — the sub-second digits will be wrong and the
link will appear deleted or inaccessible to the recipient.

### Sending the summary
Send the digest as a DM to Iwan (user ID: U0A3084QX5E).
All required Slack MCP connectors are available in the environment.