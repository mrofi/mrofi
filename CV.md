# Mokhamad Rofiudin

Senior Software Engineer · DevOps Engineer · Platform Engineer
Tulungagung, East Java, Indonesia

mokh.rofiudin@gmail.com · [linkedin.com/in/mokhamadrofiudin](https://www.linkedin.com/in/mokhamadrofiudin) · [github.com/mrofi](https://github.com/mrofi) · [mokh.rofiudin.my.id](https://mokh.rofiudin.my.id)

---

## Summary

I'm a software engineer who's happiest when something ships. I care less about how elegant a design doc is than whether the thing actually runs in production, in front of real users — and I've had the chance to deliver products used by millions of customers: ride-sharing, job-matching, and e-commerce platforms serving real customers in Jakarta, and telco billing and chatbot services at Kata.ai reaching a subscriber base in the tens of millions.

My career didn't follow a straight line. I started as an IT generalist at a hospital in my home town — writing small apps in Visual Basic 6, fixing hardware, teaching users to solve their own problems. No CS degree, just curiosity and whatever needed to get done. From there I moved into software consulting, then spent 7.5 years in Jakarta as a PHP backend developer, building real products for real users: a ride-sharing platform, a job-matching app with a custom matching algorithm, an e-commerce platform with cart, payments, vouchers, and referrals.

In 2023 I made a deliberate pivot into DevOps and platform engineering — not away from shipping, but closer to it: owning the whole path from code to production, on-call included. Now I spend my days on Kubernetes, GKE, Helm, ArgoCD, Kafka, and observability tooling, alongside writing and deploying the Go services that run on it.

14 years of figuring things out in production, across hospitals, agencies, and platform teams. Still learning, still enjoying it.

---

## Experience

### Kata.ai — DevOps Engineer
*May 2023 – Present · Jakarta, Indonesia*

Own site reliability engineering (SRE), platform operations, and backend development for a multi-tenant conversational AI platform running on GKE — on-call, postmortems, and infrastructure hardening, alongside building and maintaining the Go services that run on it.

- Diagnosed a production chatbot response-delay incident traced to a large-scale broadcast overwhelming reactive autoscaling; designed and shipped a KEDA-based pre-scaling strategy (combined CPU + scheduled triggers) that scaled the affected worker to 90 replicas ahead of each broadcast window with zero pending pods. While validating the fix, found and resolved a second, unrelated crash-loop incident on a neighboring service caused by a blocking health-check pattern — fixed by redesigning the liveness/readiness probe split, then safely cycled ~140 deployments cluster-wide to clear the resulting connection storm.
- Led a 5 Whys root-cause investigation into a P1 cluster-wide worker node outage, uncovering three independently compounding failures — a silently broken CNI plugin caused by a deprecated upstream image registry, CPU starvation from a security agent lacking container-aware exclusions, and unbounded log growth on end-of-life Kubernetes/Docker versions — and delivered both immediate fixes and a long-term upgrade roadmap.
- Designed and personally verified an end-to-end security hardening reference implementation (encrypted/private-only Cloud SQL, functional account lockout tested via real login attempts, immutable/locked backups verified via real deletion attempts, hardened bastion access via IAP + OS Login + least-privilege service accounts) to prove a client's regulatory compliance controls were technically achievable ahead of a production-wide rollout.
- Authored the migration plan and led execution of a production Kafka cluster migration from ZooKeeper-based coordination to KRaft consensus mode.
- Created and scaffolded new services from the ground up — git setup, Helm chart, CI/CD pipeline, and ArgoCD GitOps registration — and served as an individual contributor across 25+ service repositories on the platform.
- Personally designed and built several Go backend services now running in production, including payment gateway middleware connecting the chatbot platform to telco billing systems across multiple client accounts (push-to-pay, top-ups, refunds, WhatsApp payment reminders), and a CRM conversation adapter integrating the chat channel with a third-party live-chat API.
- Operate Kubernetes workloads spanning Airflow, Spark, and cert-manager; write and maintain CI/CD pipelines (Azure Pipelines) and GitOps deployments (ArgoCD, Helm).
- Regularly produce RCA documentation and postmortems for production incidents across databases (PostgreSQL, MongoDB, MySQL), messaging (Kafka, RabbitMQ), and orchestration tooling (Dkron).

### Suitmedia — Software Engineer
*December 2015 – May 2023 (7.5 years) · Jakarta Selatan, Indonesia*

- Built and maintained PHP-based web products for clients, translating requirements into working software under real deadlines.
- Delivered a ride-sharing platform, a job-matching application with a custom matching algorithm, and an e-commerce platform with cart, payment, vouchers, and referral systems.
- Advised on technical solutions across other projects beyond direct ownership.

### Jaya Institute Indonesia — IT Consultant
*January 2011 – October 2015 · Pekalongan, Central Java, Indonesia*

- Advised on software, websites, design, promotion, and general computer literacy for local clients.

### RS QIM — IT Staff
*August 2011 – February 2014 · Pekalongan, Central Java, Indonesia*

- Built internal applications in Visual Basic 6; handled hardware and software troubleshooting.
- Trained end users to independently resolve recurring issues.

---

## Skills

**Platform & Orchestration:** Kubernetes, GKE, Helm, ArgoCD (GitOps), KEDA, Docker
**Observability:** Prometheus, Grafana, Loki, Alertmanager
**Data & Messaging:** Apache Kafka (incl. ZooKeeper → KRaft migration), RabbitMQ, Cassandra
**Databases:** PostgreSQL, MySQL, MariaDB, Cloud SQL
**Cloud & Security:** Google Cloud Platform (Compute, Cloud SQL, IAM, Artifact Registry), bastion/IAP access hardening, security compliance hardening
**Workflow & Data Tooling:** Apache Airflow, Apache Spark
**Languages:** Go, TypeScript, PHP, JavaScript
**CI/CD:** Azure Pipelines, GitOps
**Frontend (prior experience):** React.js, Vue/Nuxt, TailwindCSS

---

## Selected Personal Projects

- **[edge-proxy](https://github.com/mrofi/edge-proxy)** (TypeScript) — lightweight edge proxy service.
- **[simple-golang-kv](https://github.com/mrofi/simple-golang-kv)** (Go) — a simple key-value store built with the Echo framework and etcd.
- **[bashscript-server](https://github.com/mrofi/bashscript-server)** (Go) — a lightweight HTTP server for serving and running bash scripts remotely, designed as a base Docker image.
- **[windmill-dashboard-nextjs-typescript](https://github.com/roketid/windmill-dashboard-nextjs-typescript)** (Next.js/TypeScript, 263 ★) — a Next.js admin dashboard UI.
- **[caddy-html-server-dockerfile](https://github.com/mrofi/caddy-html-server-dockerfile)** — a minimal Caddy-based static HTML server Docker base image.

More at [github.com/mrofi](https://github.com/mrofi) (100+ public repos).

---

## Education

**STMIK Widya Pratama Pekalongan** — Management Information Systems and Services *(2010 – 2015, not completed)*
**SMA Negeri 1 Pekalongan** *(2004 – 2006)*

---

## Languages

Indonesian (native/bilingual) · English (limited working proficiency)
