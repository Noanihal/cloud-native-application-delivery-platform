# User Stories  
**Cloud-Native Application Delivery Platform**

---

## 📌 Document Information

| Field | Details |
|------|--------|
| Document Name | User Stories |
| Project | Cloud-Native Application Delivery Platform |
| Version | v1.0 |
| Owner Role | Product Owner / Project Manager |
| Created On | 02-APR-2026 |
| Last Updated | 02-APR-2026 |

---

## 📜 Version History

| Version | Date | Updated By | Changes |
|--------|------|-----------|--------|
| v1.0 | 02-APR-2026 | Product Owner | Initial version |

---

## 🧭 PRIORITY LEGEND

| Code | Meaning |
|------|--------|
| M | Must Have |
| S | Should Have |
| C | Could Have |
| W | Won’t Have |

---

# 🟦 EPIC E1: Application Setup

| ID | Title | Role | User Story | Priority | Acceptance Criteria / Reason |
|----|------|------|------------|----------|------------------------------|
| E1.1 | Frontend Service Setup | Developer | As a developer, I want a frontend service so that users can interact with the application | M | Frontend runs locally; UI accessible |
| E1.2 | Backend Service Setup | Developer | As a developer, I want a backend API so that business logic is handled | M | API runs locally; Endpoint responds |
| E1.3 | Database Setup | Developer | As a developer, I want a database so that data is stored persistently | M | DB initialized; Backend connects |
| E1.4 | Service Configuration via Environment Variables | Developer | As a developer, I want environment-based configs so that services are configurable across environments | M | No hardcoded configs; Env variables used |
| E1.5 | Standardized Project Structure | Developer | As a developer, I want structured codebases so that services are maintainable | M | Clean folder structure; Separation of concerns |
| E1.6 | API Integration (Frontend ↔ Backend) | Developer | As a developer, I want frontend to call backend APIs so that data flows through system | M | API calls succeed; Data displayed |
| E1.7 | Backend ↔ Database Integration | Developer | As a developer, I want backend connected to DB so that data operations work | M | Queries execute successfully |
| E1.8 | Health Check Endpoint | Developer | As a developer, I want health endpoints so that services can be monitored | M | `/health` endpoint returns status |
| E1.9 | Application Logging | Developer | As a developer, I want logging so that system behavior can be tracked | M | Logs generated for requests/errors |
| E1.10 | Local Multi-Service Execution | Developer | As a developer, I want all services to run together locally so that integration is validated | M | Frontend, backend, DB run together |
| E1.11 | Docker-Ready Codebase | DevOps Engineer | As a DevOps Engineer, I want services structured for containerization so that Dockerization is seamless | M | No OS-specific dependencies; Services container-ready |
| E1.12 | Dependency Management | Developer | As a developer, I want proper dependency management so that builds are reproducible | M | Dependencies locked; Build succeeds |
| E1.13 | Centralized Configuration File | Developer | As a developer, I want centralized config so that environment management is easier | S | Config file exists; Supports multiple environments |
| E1.14 | API Response Standardization | Developer | As a developer, I want consistent API responses so that system behavior is predictable | S | Standard success/error format |
| E1.15 | Error Handling Mechanism | Developer | As a developer, I want structured error handling so that failures are managed | S | Errors handled gracefully |
| E1.16 | Seed/Test Data Setup | Developer | As a developer, I want initial data so that system can be tested easily | S | Sample data available |
| E1.17 | Basic Input Validation | Developer | As a developer, I want input validation so that invalid requests are prevented | S | Invalid inputs rejected |
| E1.18 | Port Configuration | Developer | As a developer, I want configurable ports so that services are flexible | S | Ports defined via env |
| E1.19 | Local Orchestration (docker-compose) | DevOps Engineer | As a DevOps Engineer, I want docker-compose so that local multi-service setup is easier | C | Services run via single command |
| E1.20 | API Documentation (Basic) | Developer | As a developer, I want API docs so that endpoints are clear | C | API endpoints documented |
| E1.21 | Structured Logging Format | Developer | As a developer, I want structured logs so that logs are machine-readable | C | JSON/log format consistent |
| E1.22 | Config Profiles (dev/test) | Developer | As a developer, I want config profiles so that environments are separated | C | Profiles defined |
| E1.23 | Advanced Authentication System | Developer | As a developer, I want authentication so that system is secure | W | Not required for DevOps focus; adds product complexity instead of platform value |
| E1.24 | UI/UX Optimization | Developer | As a developer, I want improved UI/UX so that user experience is enhanced | W | UI is not core to DevOps learning; minimal UI sufficient |
| E1.25 | Complex Business Logic | Developer | As a developer, I want advanced business logic so that application is feature-rich | W | Focus is platform engineering, not application complexity |

---

# 🟦 EPIC E2: Containerization

| ID | Title | Role | User Story | Priority | Acceptance Criteria / Reason |
|----|------|------|------------|----------|------------------------------|
| E2.1 | Frontend Dockerfile Creation | Developer | As a developer, I want a Dockerfile for frontend so that it can be containerized | M | Dockerfile created; Image builds successfully |
| E2.2 | Backend Dockerfile Creation | Developer | As a developer, I want a Dockerfile for backend so that it can be containerized | M | Dockerfile created; API works inside container |
| E2.3 | Database Container Setup | Developer | As a developer, I want database to run as a container so that setup is consistent | M | DB container runs; Backend connects |
| E2.4 | Multi-Container Local Setup | Developer | As a developer, I want all services to run in containers locally so that integration is tested | M | Frontend, backend, DB containers run together |
| E2.5 | Docker Networking Configuration | Developer | As a developer, I want containers to communicate so that services interact correctly | M | Services communicate via container network |
| E2.6 | Environment Variables Injection | Developer | As a developer, I want environment variables in containers so that configs are dynamic | M | Env variables passed at runtime |
| E2.7 | Docker Compose Setup | Developer | As a developer, I want docker-compose so that multi-service setup is simplified | M | All services run using single command |
| E2.8 | Image Build Optimization | DevOps Engineer | As a DevOps Engineer, I want optimized Docker images so that builds are efficient | M | Multi-stage build used; Image size reduced |
| E2.9 | Image Tagging Strategy | DevOps Engineer | As a DevOps Engineer, I want tagging strategy so that versions are traceable | M | Tags follow versioning (latest + commit-based) |
| E2.10 | Image Validation | DevOps Engineer | As a DevOps Engineer, I want to validate images so that deployments are reliable | M | Containers run without errors |
| E2.11 | Container Logging Validation | SRE | As an SRE, I want to verify container logs so that issues can be debugged | S | Logs accessible via container runtime |
| E2.12 | Container Health Check Integration | Developer | As a developer, I want health checks in containers so that service status is known | S | Health endpoint integrated in container |
| E2.13 | Restart Policy Configuration | Platform Engineer | As a Platform Engineer, I want restart policies so that failed containers recover | S | Containers restart on failure |
| E2.14 | .dockerignore Configuration | Developer | As a developer, I want to exclude unnecessary files so that images are efficient | S | Unused files excluded from build |
| E2.15 | Port Exposure Standardization | Developer | As a developer, I want consistent port configuration so that services are accessible | S | Ports defined and exposed properly |
| E2.16 | Base Image Standardization | DevOps Engineer | As a DevOps Engineer, I want standardized base images so that builds are secure and consistent | C | Official/minimal base images used |
| E2.17 | Container Security Best Practices | DevSecOps Engineer | As a DevSecOps Engineer, I want secure container configs so that vulnerabilities are minimized | C | Non-root user; Minimal packages |
| E2.18 | Resource Limits Definition | Platform Engineer | As a Platform Engineer, I want resource limits defined so that containers use resources efficiently | C | CPU/memory limits defined (future Kubernetes readiness) |
| E2.19 | Multi-Arch Image Support | DevOps Engineer | As a DevOps Engineer, I want multi-architecture images so that system supports different environments | W | Not required for current scope; adds unnecessary complexity |
| E2.20 | Advanced Image Caching Strategy | DevOps Engineer | As a DevOps Engineer, I want advanced caching so that builds are faster | W | Can be handled later in CI/CD phase |
| E2.21 | Private Registry Setup (Local) | DevOps Engineer | As a DevOps Engineer, I want a private registry so that images are stored locally | W | AWS ECR will be used later; local registry unnecessary |

---

# 🟦 EPIC E3: CI/CD Pipeline

| ID | Title | Role | User Story | Priority | Acceptance Criteria / Reason |
|----|------|------|------------|----------|------------------------------|
| E3.1 | CI Pipeline Setup (GitHub Actions) | DevOps Engineer | As a DevOps Engineer, I want to set up CI pipeline so that builds are automated on code push | M | Pipeline triggers on push; Workflow executes successfully |
| E3.2 | Code Checkout & Environment Setup | DevOps Engineer | As a DevOps Engineer, I want pipeline to fetch code and set environment so that build can run | M | Code checkout works; Environment prepared |
| E3.3 | Dependency Installation in CI | DevOps Engineer | As a DevOps Engineer, I want dependencies installed in pipeline so that builds are reproducible | M | Dependencies installed successfully |
| E3.4 | Build Application in CI | DevOps Engineer | As a DevOps Engineer, I want application build step so that artifacts are generated | M | Build step completes without failure |
| E3.5 | Docker Image Build in CI | DevOps Engineer | As a DevOps Engineer, I want to build Docker images in CI so that applications are containerized automatically | M | Images built successfully |
| E3.6 | Docker Image Tagging | DevOps Engineer | As a DevOps Engineer, I want proper tagging so that images are versioned | M | Tags include latest + commit-based tag |
| E3.7 | Authenticate with AWS ECR | DevOps Engineer | As a DevOps Engineer, I want pipeline to authenticate with ECR so that images can be pushed | M | Authentication succeeds securely |
| E3.8 | Push Docker Image to ECR | DevOps Engineer | As a DevOps Engineer, I want to push images to ECR so that they are available for deployment | M | Images available in ECR repository |
| E3.9 | CI Pipeline Logging | DevOps Engineer | As a DevOps Engineer, I want logs for pipeline execution so that issues can be debugged | M | Logs visible for each stage |
| E3.10 | Pipeline Failure Handling | DevOps Engineer | As a DevOps Engineer, I want pipeline to fail correctly so that issues are caught early | M | Pipeline fails on errors; No silent failures |
| E3.11 | Secrets Management in CI | DevSecOps Engineer | As a DevSecOps Engineer, I want secrets handled securely so that credentials are protected | M | Secrets stored securely; No hardcoding |
| E3.12 | Basic Pipeline Validation | DevOps Engineer | As a DevOps Engineer, I want validation checks so that pipeline ensures correctness | M | Pipeline completes end-to-end successfully |
| E3.13 | Code Quality Scan (SonarQube) | DevSecOps Engineer | As a DevSecOps Engineer, I want code scanning so that quality issues are detected | S | Scan runs; Issues reported |
| E3.14 | Image Vulnerability Scan (Trivy) | DevSecOps Engineer | As a DevSecOps Engineer, I want image scanning so that vulnerabilities are detected | S | Scan runs; Vulnerabilities reported |
| E3.15 | Pipeline Stage Separation | DevOps Engineer | As a DevOps Engineer, I want clear pipeline stages so that workflow is structured | S | Build, test, push stages separated |
| E3.16 | Branch-Based Pipeline Execution | DevOps Engineer | As a DevOps Engineer, I want branch-based triggers so that environments can be controlled | S | Pipeline behavior differs by branch |
| E3.17 | Artifact Retention | DevOps Engineer | As a DevOps Engineer, I want artifacts stored so that builds are traceable | S | Artifacts stored and accessible |
| E3.18 | Parallel Job Execution | DevOps Engineer | As a DevOps Engineer, I want parallel jobs so that pipeline is faster | C | Jobs run in parallel |
| E3.19 | Notification Integration | DevOps Engineer | As a DevOps Engineer, I want notifications so that failures are communicated | C | Notifications sent on failure |
| E3.20 | Reusable Pipeline Templates | DevOps Engineer | As a DevOps Engineer, I want reusable workflows so that pipelines are maintainable | C | Templates created and reused |
| E3.21 | Multi-Environment CD (Full Deployment) | DevOps Engineer | As a DevOps Engineer, I want full CD pipeline so that deployments are automated across environments | W | Will be handled in GitOps (E4/E5); not part of initial CI |
| E3.22 | Advanced Pipeline Orchestration (Jenkins) | DevOps Engineer | As a DevOps Engineer, I want Jenkins pipelines so that complex workflows can be managed | W | Will be introduced later phase |
| E3.23 | Canary / Blue-Green Deployment | Platform Engineer | As a Platform Engineer, I want advanced deployment strategies so that releases are safer | W | Out of scope for initial CI/CD setup |

---

# 🟦 EPIC E4: Kubernetes Deployment

| ID | Title | Role | User Story | Priority | Acceptance Criteria / Reason |
|----|------|------|------------|----------|------------------------------|
| E4.1 | Kubernetes Cluster Setup (EKS) | Cloud Engineer | As a Cloud Engineer, I want to provision a Kubernetes cluster so that applications can be deployed | M | EKS cluster created; Nodes available |
| E4.2 | kubectl Access Configuration | DevOps Engineer | As a DevOps Engineer, I want access to the cluster so that I can manage deployments | M | kubectl configured; Cluster accessible |
| E4.3 | Namespace Setup | Platform Engineer | As a Platform Engineer, I want namespaces so that workloads are logically separated | M | Namespace created and used |
| E4.4 | Backend Deployment | Platform Engineer | As a Platform Engineer, I want backend deployed so that API runs in cluster | M | Pods running; Backend accessible internally |
| E4.5 | Frontend Deployment | Platform Engineer | As a Platform Engineer, I want frontend deployed so that UI is available | M | Pods running; UI accessible |
| E4.6 | Database Deployment | Platform Engineer | As a Platform Engineer, I want database deployed so that persistence is available | M | DB pod running; Persistent storage configured |
| E4.7 | Service Configuration (ClusterIP) | Platform Engineer | As a Platform Engineer, I want services so that pods can communicate | M | Services created; Internal communication works |
| E4.8 | External Access (LoadBalancer/Ingress) | Platform Engineer | As a Platform Engineer, I want external access so that users can access application | M | App accessible via external endpoint |
| E4.9 | Environment Variables in Kubernetes | Platform Engineer | As a Platform Engineer, I want environment variables injected so that configs are dynamic | M | Env variables configured via manifests |
| E4.10 | Secrets Management (Kubernetes) | DevSecOps Engineer | As a DevSecOps Engineer, I want secrets managed so that sensitive data is secure | M | Secrets created; No hardcoded credentials |
| E4.11 | Health Probes (Liveness/Readiness) | Platform Engineer | As a Platform Engineer, I want health checks so that Kubernetes manages pod health | M | Liveness & readiness probes configured |
| E4.12 | Resource Requests & Limits | Platform Engineer | As a Platform Engineer, I want resource limits so that workloads are controlled | M | CPU/memory limits defined |
| E4.13 | Logging Visibility | SRE | As an SRE, I want logs from pods so that issues can be debugged | M | Logs accessible via kubectl logs |
| E4.14 | Basic Deployment Validation | DevOps Engineer | As a DevOps Engineer, I want to validate deployment so that system is working end-to-end | M | Frontend → Backend → DB works in cluster |
| E4.15 | Horizontal Pod Autoscaler (HPA) | Platform Engineer | As a Platform Engineer, I want auto-scaling so that system handles load | S | HPA configured; Pods scale under load |
| E4.16 | ConfigMaps for Configuration | Platform Engineer | As a Platform Engineer, I want config maps so that configs are externalized | S | ConfigMaps used for non-sensitive configs |
| E4.17 | Rolling Update Strategy | Platform Engineer | As a Platform Engineer, I want rolling updates so that deployments are smooth | S | No downtime during updates |
| E4.18 | Pod Restart Policies | Platform Engineer | As a Platform Engineer, I want restart policies so that failures are handled | S | Pods restart automatically on failure |
| E4.19 | Ingress Controller Setup | Platform Engineer | As a Platform Engineer, I want ingress so that routing is managed efficiently | C | Ingress controller configured |
| E4.20 | Multi-Namespace Strategy | Platform Engineer | As a Platform Engineer, I want multiple namespaces so that environments are separated | C | Dev/staging namespaces defined |
| E4.21 | Service Mesh Integration | Platform Engineer | As a Platform Engineer, I want service mesh so that traffic control is enhanced | C | Service mesh integrated (future) |
| E4.22 | Multi-Cluster Deployment | Cloud Engineer | As a Cloud Engineer, I want multi-cluster setup so that system is globally distributed | W | Not required for current scale; adds complexity |
| E4.23 | Advanced Traffic Routing (Canary/Blue-Green) | Platform Engineer | As a Platform Engineer, I want advanced routing so that releases are safer | W | Will be handled later if needed |
| E4.24 | Chaos Engineering Setup | SRE | As an SRE, I want chaos testing so that resilience is validated | W | Out of scope for initial deployment phase |

---

# 🟦 EPIC E5: GitOps Deployment

| ID | Title | Role | User Story | Priority | Acceptance Criteria / Reason |
|----|------|------|------------|----------|------------------------------|
| E5.1 | GitOps Repository Setup | DevOps Engineer | As a DevOps Engineer, I want a dedicated Git repository so that deployment configurations are version controlled | M | Repo created; Structure defined for manifests/Helm |
| E5.2 | Helm Chart Creation (Frontend) | Platform Engineer | As a Platform Engineer, I want Helm charts for frontend so that deployments are standardized | M | Helm chart created; Deployable via Helm |
| E5.3 | Helm Chart Creation (Backend) | Platform Engineer | As a Platform Engineer, I want Helm charts for backend so that deployments are standardized | M | Helm chart created; Backend deploys successfully |
| E5.4 | Helm Chart Creation (Database) | Platform Engineer | As a Platform Engineer, I want Helm charts for database so that deployment is consistent | M | DB Helm chart works; Persistent storage configured |
| E5.5 | Values Configuration (Environment-based) | Platform Engineer | As a Platform Engineer, I want values files so that configurations differ per environment | M | values.yaml supports env configs |
| E5.6 | ArgoCD Installation | Platform Engineer | As a Platform Engineer, I want ArgoCD installed so that GitOps deployment is enabled | M | ArgoCD running in cluster |
| E5.7 | ArgoCD Application Setup | Platform Engineer | As a Platform Engineer, I want ArgoCD apps configured so that deployments are automated | M | Application created; Sync works |
| E5.8 | GitOps Sync (Auto Deployment) | DevOps Engineer | As a DevOps Engineer, I want ArgoCD to sync automatically so that deployments happen on Git changes | M | Changes in repo trigger deployment |
| E5.9 | Deployment State Visibility | SRE | As an SRE, I want deployment status visibility so that system state is monitored | M | ArgoCD UI shows sync status |
| E5.10 | Separation of GitOps and App Repos | DevOps Engineer | As a DevOps Engineer, I want separate repos so that concerns are isolated | M | App code and deployment configs separated |
| E5.11 | Rollback Capability via Git | Platform Engineer | As a Platform Engineer, I want rollback using Git so that deployments can be reverted | M | Reverting Git commit rolls back deployment |
| E5.12 | Secrets Handling in GitOps | DevSecOps Engineer | As a DevSecOps Engineer, I want secrets managed securely so that sensitive data is protected | M | Secrets not stored in plain text; External or encrypted |
| E5.13 | App-of-Apps Pattern | Platform Engineer | As a Platform Engineer, I want app-of-apps so that multiple services are managed centrally | S | Parent app manages child apps |
| E5.14 | Sync Policies (Auto/Manual) | Platform Engineer | As a Platform Engineer, I want control over sync so that deployments are flexible | S | Sync modes configurable |
| E5.15 | Drift Detection | SRE | As an SRE, I want drift detection so that config mismatches are identified | S | ArgoCD detects out-of-sync state |
| E5.16 | Environment Separation (dev/staging) | DevOps Engineer | As a DevOps Engineer, I want env separation so that deployments are isolated | S | Separate configs per env |
| E5.17 | Multi-Cluster GitOps | Platform Engineer | As a Platform Engineer, I want multi-cluster support so that system scales | C | Multiple clusters managed |
| E5.18 | Helm Chart Reusability | Platform Engineer | As a Platform Engineer, I want reusable charts so that services scale easily | C | Charts parameterized |
| E5.19 | GitOps Access Control | DevSecOps Engineer | As a DevSecOps Engineer, I want RBAC so that deployments are secure | C | Role-based access enforced |
| E5.20 | Multi-Tenant GitOps Setup | Platform Engineer | As a Platform Engineer, I want multi-tenant GitOps so that multiple teams can deploy independently | W | Not required for single-project scope |
| E5.21 | Advanced Deployment Strategies (Canary/Blue-Green via GitOps) | Platform Engineer | As a Platform Engineer, I want advanced strategies so that releases are safer | W | Will be considered after baseline GitOps |
| E5.22 | Policy Enforcement (OPA/Gatekeeper) | DevSecOps Engineer | As a DevSecOps Engineer, I want policy enforcement so that configs are validated | W | Out of scope for initial implementation |

---
# 🟦 EPIC E6: Observability

| ID | Title | Role | User Story | Priority | Acceptance Criteria / Reason |
|----|------|------|------------|----------|------------------------------|
| E6.1 | Metrics Collection Setup (Prometheus) | SRE | As an SRE, I want to collect metrics so that system performance can be monitored | M | Prometheus deployed; Metrics scraped successfully |
| E6.2 | Application Metrics Exposure | Developer | As a developer, I want application metrics exposed so that they can be monitored | M | Metrics endpoint available (e.g., /metrics) |
| E6.3 | Grafana Deployment | SRE | As an SRE, I want Grafana so that metrics can be visualized | M | Grafana deployed; Accessible via UI |
| E6.4 | Dashboard Creation | SRE | As an SRE, I want dashboards so that system health is visible | M | Dashboards show CPU, memory, request metrics |
| E6.5 | Kubernetes Metrics Monitoring | SRE | As an SRE, I want cluster-level metrics so that infrastructure health is tracked | M | Node/pod metrics visible |
| E6.6 | Container Logs Access | SRE | As an SRE, I want logs from containers so that issues can be debugged | M | Logs accessible via kubectl logs |
| E6.7 | Centralized Logging Setup | SRE | As an SRE, I want centralized logging so that logs are aggregated | M | Logs collected in single system (CloudWatch/Loki) |
| E6.8 | Log Integration with Application | Developer | As a developer, I want structured logs so that logs are meaningful | M | Logs include request/response/error data |
| E6.9 | Observability Validation | SRE | As an SRE, I want to validate observability so that system is monitorable end-to-end | M | Metrics + logs visible for all services |
| E6.10 | Alerting Setup (Prometheus Alertmanager) | SRE | As an SRE, I want alerts so that failures are detected proactively | S | Alerts triggered on threshold breach |
| E6.11 | Log Query & Search | SRE | As an SRE, I want log search capability so that debugging is faster | S | Logs searchable via query |
| E6.12 | Dashboard Standardization | SRE | As an SRE, I want standardized dashboards so that monitoring is consistent | S | Common dashboards reused |
| E6.13 | Application-Level Metrics (Custom) | Developer | As a developer, I want custom metrics so that business-level insights are available | S | Custom metrics exposed |
| E6.14 | Distributed Tracing | SRE | As an SRE, I want tracing so that request flow is visible | C | Traces captured (Jaeger/Tempo) |
| E6.15 | External Monitoring Integration (Datadog) | SRE | As an SRE, I want external monitoring so that advanced insights are available | C | Datadog integrated |
| E6.16 | Log Correlation with Metrics | SRE | As an SRE, I want logs and metrics correlated so that debugging is easier | C | Logs linked with metrics |
| E6.17 | Full Observability Stack (Tracing + APM + Profiling) | SRE | As an SRE, I want complete observability so that system is fully instrumented | W | Overkill for initial setup; incremental approach preferred |
| E6.18 | AI-Based Anomaly Detection | SRE | As an SRE, I want automated anomaly detection so that issues are predicted | W | Not required for baseline observability |
| E6.19 | Enterprise SLA Monitoring System | SRE | As an SRE, I want SLA tracking so that uptime is formally measured | W | Can be added after system maturity |

---

# 🟦 EPIC E7: Security

| ID | Title | Role | User Story | Priority | Acceptance Criteria / Reason |
|----|------|------|------------|----------|------------------------------|
| E7.1 | IAM Role Configuration (AWS) | Cloud Engineer | As a Cloud Engineer, I want IAM roles configured so that access to AWS resources is secure | M | Least-privilege roles created; Access controlled |
| E7.2 | Kubernetes RBAC Setup | Platform Engineer | As a Platform Engineer, I want RBAC so that cluster access is restricted | M | Roles and role bindings configured |
| E7.3 | Secrets Management (AWS Secrets Manager / K8s Secrets) | DevSecOps Engineer | As a DevSecOps Engineer, I want secrets managed securely so that credentials are protected | M | Secrets stored securely; No hardcoding |
| E7.4 | Secure Environment Variable Handling | Developer | As a developer, I want secure env handling so that sensitive data is not exposed | M | Sensitive values not stored in code |
| E7.5 | CI/CD Secrets Management | DevSecOps Engineer | As a DevSecOps Engineer, I want secrets in pipeline secured so that credentials are protected | M | Secrets stored in GitHub Secrets; No plaintext exposure |
| E7.6 | Secure Docker Image Practices | DevSecOps Engineer | As a DevSecOps Engineer, I want secure images so that vulnerabilities are minimized | M | Minimal base image; No unnecessary packages |
| E7.7 | Container Vulnerability Scanning (Trivy) | DevSecOps Engineer | As a DevSecOps Engineer, I want image scanning so that vulnerabilities are detected | M | Scan runs; Issues reported |
| E7.8 | Code Quality & Security Scan (SonarQube) | DevSecOps Engineer | As a DevSecOps Engineer, I want code scanning so that vulnerabilities are identified | M | Scan integrated in pipeline |
| E7.9 | Network Access Control (Security Groups / K8s) | Cloud Engineer | As a Cloud Engineer, I want network controls so that services are protected | M | Only required ports exposed |
| E7.10 | HTTPS / Secure Access Setup | Platform Engineer | As a Platform Engineer, I want secure communication so that data is encrypted | M | HTTPS enabled (basic setup) |
| E7.11 | Sensitive Data Masking in Logs | Developer | As a developer, I want sensitive data masked so that logs are safe | M | No secrets in logs |
| E7.12 | Security Validation in Pipeline | DevSecOps Engineer | As a DevSecOps Engineer, I want security checks in CI so that insecure builds fail | M | Pipeline fails on critical vulnerabilities |
| E7.13 | Kubernetes Network Policies | Platform Engineer | As a Platform Engineer, I want network policies so that pod communication is controlled | S | Traffic restricted between services |
| E7.14 | Image Signing / Verification | DevSecOps Engineer | As a DevSecOps Engineer, I want image verification so that trusted images are used | S | Image validation enabled |
| E7.15 | Role-Based Access in CI/CD | DevSecOps Engineer | As a DevSecOps Engineer, I want role-based pipeline access so that permissions are controlled | S | Access restricted by roles |
| E7.16 | Secrets Rotation Strategy | DevSecOps Engineer | As a DevSecOps Engineer, I want secret rotation so that credentials remain secure | S | Rotation mechanism defined |
| E7.17 | Web Application Firewall (WAF) | Cloud Engineer | As a Cloud Engineer, I want WAF so that application is protected from attacks | C | WAF configured |
| E7.18 | Security Monitoring Dashboard | SRE | As an SRE, I want security metrics so that threats are visible | C | Security metrics dashboard |
| E7.19 | Policy Enforcement (OPA/Gatekeeper) | DevSecOps Engineer | As a DevSecOps Engineer, I want policy enforcement so that configs follow rules | C | Policies applied to cluster |
| E7.20 | Zero Trust Architecture | Security Architect | As a Security Architect, I want zero trust so that all access is verified | W | Too complex for initial project scope |
| E7.21 | Advanced Threat Detection (SIEM) | SRE | As an SRE, I want SIEM so that threats are analyzed centrally | W | Not required for baseline system |
| E7.22 | Full Compliance Framework (SOC2/GDPR) | Compliance Engineer | As a Compliance Engineer, I want compliance so that system meets regulations | W | Out of scope for portfolio project |

---

# 🟦 EPIC E8: Infrastructure (Future Phase)


| ID | Title | Role | User Story | Priority | Acceptance Criteria / Reason |
|----|------|------|------------|----------|------------------------------|
| E8.1 | Terraform Project Setup | Cloud Engineer | As a Cloud Engineer, I want a Terraform project so that infrastructure can be managed as code | M | Terraform repo created; Structure defined |
| E8.2 | VPC Provisioning via Terraform | Cloud Engineer | As a Cloud Engineer, I want VPC created via IaC so that network is reproducible | M | VPC, subnets, routing configured |
| E8.3 | EKS Cluster Provisioning via Terraform | Cloud Engineer | As a Cloud Engineer, I want EKS created via Terraform so that cluster setup is automated | M | EKS cluster provisioned successfully |
| E8.4 | IAM Roles via Terraform | Cloud Engineer | As a Cloud Engineer, I want IAM roles defined so that access is controlled | M | Roles created with least privilege |
| E8.5 | ECR Repository via Terraform | Cloud Engineer | As a Cloud Engineer, I want ECR repos created so that images can be stored | M | ECR repos available |
| E8.6 | Terraform State Management (Remote Backend) | DevOps Engineer | As a DevOps Engineer, I want remote state so that infrastructure is managed safely | M | State stored in S3; Locking enabled |
| E8.7 | Terraform Execution Workflow | DevOps Engineer | As a DevOps Engineer, I want standardized workflow so that infra changes are controlled | M | Plan → Apply workflow defined |
| E8.8 | Environment-Based Infrastructure (dev/prod) | Cloud Engineer | As a Cloud Engineer, I want environment separation so that deployments are isolated | M | Separate configs per environment |
| E8.9 | Infrastructure Validation | DevOps Engineer | As a DevOps Engineer, I want validation so that infra changes are safe | M | Terraform validate/plan executed |
| E8.10 | Modular Terraform Design | Cloud Engineer | As a Cloud Engineer, I want modules so that infra is reusable | S | Modules created for VPC, EKS, IAM |
| E8.11 | CI/CD for Terraform | DevOps Engineer | As a DevOps Engineer, I want pipeline for infra so that changes are automated | S | Terraform integrated with CI pipeline |
| E8.12 | Ansible Setup | DevOps Engineer | As a DevOps Engineer, I want Ansible so that system configs are automated | S | Playbooks created |
| E8.13 | Node Configuration via Ansible | DevOps Engineer | As a DevOps Engineer, I want node setup automated so that consistency is maintained | S | Nodes configured via playbooks |
| E8.14 | Secrets Handling in Terraform | DevSecOps Engineer | As a DevSecOps Engineer, I want secrets handled securely so that sensitive data is protected | S | No secrets in code; Secure storage used |
| E8.15 | Multi-Region Infrastructure | Cloud Engineer | As a Cloud Engineer, I want multi-region setup so that system is resilient | C | Infra deployed in multiple regions |
| E8.16 | Cost Optimization Setup | Cloud Engineer | As a Cloud Engineer, I want cost tracking so that resources are optimized | C | Cost monitoring enabled |
| E8.17 | Infrastructure Monitoring Integration | SRE | As an SRE, I want infra monitoring so that resource health is tracked | C | Infra metrics visible |
| E8.18 | Fully Automated Infra Provisioning Pipeline | DevOps Engineer | As a DevOps Engineer, I want fully automated infra provisioning so that no manual steps are needed | W | Will introduce after stable manual workflow |
| E8.19 | Multi-Cloud Infrastructure | Cloud Engineer | As a Cloud Engineer, I want multi-cloud setup so that vendor lock-in is avoided | W | Out of scope; AWS-only focus |
| E8.20 | Advanced Networking (PrivateLink, Transit Gateway) | Cloud Engineer | As a Cloud Engineer, I want advanced networking so that enterprise connectivity is achieved | W | Not required for current project scale |

---
