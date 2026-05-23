# Kaio here 👋

📍 Fortaleza, Brazil | 🔧 Senior Platform Engineer · Istio upstream contributor · Go & K8s operators

![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)
![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Istio](https://img.shields.io/badge/-Istio-466BB0?style=flat&logo=istio&logoColor=white)
![Terraform](https://img.shields.io/badge/-Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![Crossplane](https://img.shields.io/badge/-Crossplane-EF3A43?style=flat&logo=crossplane&logoColor=white)
![ArgoCD](https://img.shields.io/badge/-ArgoCD-EF7B4D?style=flat&logo=argo&logoColor=white)
![Helm](https://img.shields.io/badge/-Helm-0F1689?style=flat&logo=helm&logoColor=white)
![Prometheus](https://img.shields.io/badge/-Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/-Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/-OpenTelemetry-F5A800?style=flat&logo=opentelemetry&logoColor=black)

> Computadores fazem arte<br>
> artistas fazem dinheiro<br>
> Computadores avançam<br>
> artistas levam a fama

---

## 🌐 Upstream — Istio

Active contributor to [istio/istio](https://github.com/istio/istio). Filed [**#59567**](https://github.com/istio/istio/issues/59567) (multi-port metrics merging in `enablePrometheusMerge`); design discussion with maintainers ([@howardjohn](https://github.com/howardjohn), [@keithmattix](https://github.com/keithmattix)) led to acceptance of the additive `prometheus.istio.io/scrape-targets` annotation over deprecation. **2 of 3 PRs from the implementation series are merged**:

- [**#59924**](https://github.com/istio/istio/pull/59924) *(merged)* — annotation parsing + data model with backward-compat guarantees
- [**#59925**](https://github.com/istio/istio/pull/59925) *(merged)* — concurrent fan-out in `handleStats` with OpenMetrics EOF handling
- [**#59926**](https://github.com/istio/istio/pull/59926) *(in review)* — integration tests for STRICT mTLS multi-container pods

Solves a real production failure mode previously without an upstream fix.

→ [Why Istio's Metrics Merging Breaks in Multi-Container Pods — and How to Fix It](https://dev.to/kaiohenricunha/why-istios-metrics-merging-breaks-in-multi-container-pods-and-how-to-fix-it-3l6f)

---

## What I'm Thinking About

- **Multi-cluster Istio at production scale** — service mesh as platform primitive, not just sidecar config
- **Crossplane vs Terraform for tenant-facing platform APIs** — when each wins, where the seams should be
- **Agentic CLI governance** — what dotbabel solves and what still doesn't have a good answer
- **Observability cost vs cardinality tradeoffs in Thanos at scale** — retention strategies, downsampling, the FinOps angle

---

## Featured Projects

🔩 **[metrics-aggregator](https://github.com/kaiohenricunha/metrics-aggregator)** — Go sidecar for aggregating Prometheus metrics from multiple containers in a K8s Pod. The public artifact of the Istio #59567 contribution; production alerting and native OTel tracing (OTLP, W3C traceparent, Jaeger).

🧹 **[kube-janitor](https://github.com/kaiohenricunha/kube-janitor)** — Kubernetes controller that automatically classifies and garbage-collects stale resources using TTL annotations, expiry timestamps, owner references, and a resolver reference graph. Operator chops in Go.

⚙️ **[dotbabel](https://github.com/kaiohenricunha/dotbabel)** — Model-agnostic governance toolkit for agentic CLIs (Claude Code, Codex, Gemini, Copilot) plus the `@dotbabel/dotbabel` npm package. CLI validators for skills-manifest checksums, spec schemas, PR spec-coverage gates, and instruction drift across `CLAUDE.md` / `README.md` / `copilot-instructions.md`.

🏆 **[SquadRanks](https://squadranks.com/)** *(private)* — Production football intelligence platform. Composite squad rankings from heterogeneous stats and prediction-market sources (Sofascore × Kalshi), engineered around data variety and veracity. Multiplayer prediction pools (bolão), multilingual (EN/PT/FR/ES). TypeScript + React + Vite + Go + PostgreSQL on Vercel + Fly.io + Neon.

<details>
<summary><b>Other Projects</b></summary>

<br>

🧠 **[kortex](https://github.com/kaiohenricunha/kortex)** — CLI that compiles raw source material into a structured, interlinked Obsidian knowledge base. Go + Cobra.

⚔️ **[lamport](https://github.com/kaiohenricunha/lamport)** — Go + Temporal cloud infrastructure pentesting tool orchestrating a 13-agent Claude AI pipeline across AWS/GCP/Azure/K8s targets.

📊 **[aws-scalable-metabase-deployment](https://github.com/kaiohenricunha/aws-scalable-metabase-deployment)** — Production-grade Metabase on EKS with Fargate, Karpenter, and KEDA. Real-world case study.

⚡ **[ami-update-automation](https://github.com/kaiohenricunha/ami-update-automation)** — AWS Lambda detecting new EKS AMI versions and opening PRs across Terraform/Terragrunt/Pulumi/Crossplane repos.

🛡️ **[pentest-dashboard](https://github.com/kaiohenricunha/pentest-dashboard)** — Go web dashboard ingesting Shannon pentest reports, tracking security posture with REST API + Prometheus metrics.

🔗 **[shannon-reporter](https://github.com/kaiohenricunha/shannon-reporter)** — CLI tool and GitHub Action bridging Shannon pentest reports into GitHub workflows.

🎯 **[pentest-lab](https://github.com/kaiohenricunha/pentest-lab)** — Deliberately vulnerable Go REST API for white-box + black-box exploit validation.

🎬 **[showreel](https://github.com/kaiohenricunha/showreel)** — Script-driven demo video generator built on Remotion.

🩺 **Cori** *(private)* — Holistic health monitoring app. React Native + Go API + Python AI service.

⚽ **Moneyballer** *(private)* — Stats-based football scouting system. Python ELT + Go API + TypeScript/React.

</details>

---

## Writing

📝 [Why Istio's Metrics Merging Breaks in Multi-Container Pods — and How to Fix It](https://dev.to/kaiohenricunha/why-istios-metrics-merging-breaks-in-multi-container-pods-and-how-to-fix-it-3l6f)

📝 [Istio's Metrics Merging Was Built for a Simpler World. What Should Replace It?](https://medium.com/@kaiohsdc/istios-metrics-merging-was-built-for-a-simpler-world-what-should-replace-it-585b285fbc32?postPublishedType=repub)

📝 [Scaling Workloads with the Big Savings Quartet: EKS, Fargate, Karpenter, and KEDA](https://medium.com/@kaiohsdc/scaling-workloads-with-the-big-savings-quartet-eks-fargate-karpenter-and-keda-1d43d2bb5f72)

📝 [dotbabel: The Open Source Governance Layer for AI-Assisted Development](https://medium.com/@methodMan/dotclaude-the-open-source-governance-layer-for-ai-assisted-development-b57880968ce9)

📝 [dotbabel handoff: Portable Context across Claude Code, Codex, Copilot CLI, and Gemini CLI](https://medium.com/@methodMan/dotclaude-handoff-portable-context-across-claude-code-codex-copilot-cli-and-gemini-cli-746ea788d03a)

---

<details>
<summary><b>Random Facts</b></summary>

<br>

- Taught English for 8 years — still the best debugging skill I have
- Will argue about football (the real one ⚽) with anyone
- Thinks about wormholes and quantum gravity more than is professionally useful
- Has kicked off Claude Code remote sessions from the gym more than once

</details>

---

## Connect

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/kaiohenricunha)
[![GitHub](https://img.shields.io/badge/-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/kaiohenricunha)
[![Twitter](https://img.shields.io/badge/-Twitter-1DA1F2?style=flat&logo=x&logoColor=white)](https://twitter.com/kaiohenricunha)
[![Medium](https://img.shields.io/badge/-Medium-12100E?style=flat&logo=medium&logoColor=white)](https://medium.com/@kaiohsdc)
[![dev.to](https://img.shields.io/badge/-dev.to-0A0A0A?style=flat&logo=devdotto&logoColor=white)](https://dev.to/kaiohenricunha)
![Timezone](https://img.shields.io/badge/-UTC--3_(Fortaleza)-gray?style=flat&logo=clock&logoColor=white)
