# Sufideen — Azure Security & Cloud Engineering Portfolio

Azure platform, identity and security engineering, built as code. Every project below deploys through Bicep and GitHub Actions with OIDC (no stored secrets) and a DevSecOps gate in the pipeline.

## How the flagship projects fit together

A layered Azure security platform, each repo owning a distinct scope:

| Layer | Repo | What it owns |
|---|---|---|
| 1. Foundation | [azl-bicepdeploy](https://github.com/sufideen/azl-bicepdeploy) | Management groups, Azure Policy, hub network, Log Analytics workspace |
| 2. Identity / Zero Trust | [ztr-entra-lz](https://github.com/sufideen/ztr-entra-lz) | Conditional Access, PIM, custom RBAC, Sentinel identity rules |
| 3. Security operations | [az-ent-sec-dashboard](https://github.com/sufideen/az-ent-sec-dashboard) | Executive, SOC and Zero Trust workbooks, detections, Teams/email alerting |
| Pipeline reference | [securebicep](https://github.com/sufideen/securebicep) | Checkov + PSRule gates, hub-and-spoke reference |
| Workloads on the platform | [AKS + ACR web platform](https://github.com/sufideen/az-ent-sec-dashboard/blob/main/docs/kubernetes-showcase.md), [rag-support-agent-poc](https://github.com/sufideen/rag-support-agent-poc), [avd-bicep-lz](https://github.com/sufideen/avd-bicep-lz) | AI and virtual-desktop workloads |

## Featured projects

### 1. Zero Trust Landing Zone — [ztr-entra-lz](https://github.com/sufideen/ztr-entra-lz)
Identity control plane as code for employees, contractors, B2B vendors and workload identities: Conditional Access, PIM, custom RBAC, Sentinel analytics and Defender for Cloud plans. What-If validation, policy-as-code scanning and OIDC federated deploys.
**Skills:** Entra ID, Conditional Access, PIM, Sentinel, Bicep, GitHub Actions

### 2. Azure Security Operations Platform — [az-ent-sec-dashboard](https://github.com/sufideen/az-ent-sec-dashboard)
Executive, SOC and Zero Trust dashboards as Azure Workbooks, 5 Sentinel analytics rules, and secretless alerting (Action Group → Logic App → Teams) using Key Vault and managed identity. See project 3 for the AKS platform in the same repo.
**Skills:** Sentinel, KQL, Workbooks, Logic Apps, AKS, Checkov/PSRule

### 3. Secure AKS + ACR Web Platform — [az-ent-sec-dashboard (webplat)](https://github.com/sufideen/az-ent-sec-dashboard/blob/main/docs/kubernetes-showcase.md)
Private AKS cluster (system and user node pools), private Premium ACR with no admin user, and an Application Gateway WAF_v2 ingress via AGIC. Images are pulled through the kubelet managed identity (AcrPull), TLS certificates come from Key Vault via the CSI driver, and CI/CD runs on GitHub Actions with OIDC. Deployed and verified end to end in both dev and prod (nodes Ready, pods Running, App Gateway backend healthy, HTTPS 200), with captured evidence, a real prod incident write-up, a High-Level Design, an operations Low-Level Design and a slide deck.
**Skills:** AKS, ACR, Application Gateway WAF, AGIC, Key Vault CSI, Kubernetes, managed identity, Bicep

### 4. Azure Landing Zone GitOps Engine — [azl-bicepdeploy](https://github.com/sufideen/azl-bicepdeploy)
Four-scope landing zone (tenant, management group, subscription, resource group) with a 10-node management group hierarchy, governance policy, logging and hub network, deployed passwordlessly from one pipeline.
**Skills:** Landing zones, management groups, Azure Policy, Bicep, OIDC

### 5. Secure Bicep Pipelines — [securebicep](https://github.com/sufideen/securebicep)
Hub-and-spoke zero-trust network with isolated Dev/Prod, and a pipeline that refuses to deploy anything Checkov and PSRule haven't scanned. Two reference setups: a minimal one and a full topology.
**Skills:** DevSecOps, Azure DevOps, Checkov, PSRule, network security

### 6. RAG Support Agent on Azure AI Foundry — [rag-support-agent-poc](https://github.com/sufideen/rag-support-agent-poc)
Customer-support agent using Azure AI Search, Azure OpenAI and Content Safety behind private endpoints in the Zero Trust landing zone. Entra ID/RBAC only, no API keys. Content Safety moderates both question and answer.
**Skills:** Azure AI Foundry, RAG, AI Search, Azure OpenAI, FastAPI, private networking

### 7. Azure Virtual Desktop Pilot — [avd-bicep-lz](https://github.com/sufideen/avd-bicep-lz)
Deployed and verified AVD pilot: host pool, two Entra-joined session hosts, FSLogix on Azure Files, scaling plan, no public RDP. Includes an RDS-to-AVD terminology map and a documented registration troubleshooting case.
**Skills:** AVD, FSLogix, Entra join, Bicep, migration scoping

## More work

| Area | Repos |
|---|---|
| Data protection and SOC | [Purview-DLP](https://github.com/sufideen/Purview-DLP), [soc-tvm](https://github.com/sufideen/soc-tvm) |
| Hybrid / on-prem | [azure-local-poc](https://github.com/sufideen/azure-local-poc) |
| Automation | [azure-jobs-scraper](https://github.com/sufideen/azure-jobs-scraper), [uk-news-scraper](https://github.com/sufideen/uk-news-scraper), [PowerShell_training](https://github.com/sufideen/PowerShell_training) |
| Training labs | [azcloudtrain01](https://github.com/sufideen/azcloudtrain01), [ictlabs](https://github.com/sufideen/ictlabs), [devsecops-practice](https://github.com/sufideen/devsecops-practice) |

## Contact
- Email: [sufyan@ict-cloud.solutions](mailto:sufyan@ict-cloud.solutions)
- LinkedIn: [Sufyan Deen-Gabisi](https://www.linkedin.com/in/sufyan-deen-gabisi-9b03105b/)
