# GH-300 Architectures

> 6 reference scenarios for GitHub Copilot at scale.

## 1. Personal developer workflow

```mermaid
flowchart LR
    Dev[VS Code]
    Dev --> CC[Copilot completions]
    Dev --> Chat[Copilot Chat]
    Dev --> CLI[gh copilot CLI]
    CC --> Proxy[GitHub Copilot proxy]
    Chat --> Proxy
    CLI --> Proxy
    Proxy --> LLM[LLM provider]
    Proxy --> Tel[Telemetry: opt-in for training]
```

## 2. Small team on Copilot Business

```mermaid
flowchart TB
    OrgAdmin[Org admin]
    OrgAdmin --> Policy[Set policies]
    Policy --> Filter[Public code filter ON]
    Policy --> Excl[Content exclusions:<br/>secrets/, *.env]
    Policy --> Audit[Audit logs enabled]
    Devs[Developer seats]
    Filter --> Devs
    Excl --> Devs
    Devs --> Proxy[Copilot proxy]
    Audit --> Log[Audit log store]
```

## 3. Enterprise with knowledge bases

```mermaid
flowchart LR
    Docs[Curated docs repos]
    Docs --> Idx[Knowledge base index]
    Idx --> KB[Knowledge base]
    Dev[IDE / web Chat]
    Dev -->|@workspace q| Chat[Copilot Chat Enterprise]
    Chat --> KB
    KB --> Chat
    Chat --> Dev
```

## 4. Custom models pipeline (Enterprise preview)

```mermaid
flowchart LR
    Repo[Private repos]
    Repo --> Train[Fine-tune pipeline<br/>GitHub-managed]
    Train --> Model[Custom Copilot model]
    Model --> Devs[Developer IDE]
    Devs --> Sugg[Suggestions match<br/>house conventions]
```

## 5. Compliance + audit topology

```mermaid
flowchart TB
    Devs[Developers] --> Proxy[Copilot proxy]
    Proxy --> LLM[LLM]
    Proxy --> Tel[Telemetry events]
    Tel --> Audit[Audit log API]
    Audit --> SIEM[SIEM / Splunk / Sentinel]
    Audit --> Compl[Compliance reports]
    OrgAdmin[Org admin] --> Audit
```

## 6. Content exclusions + IP-sensitive workflow

```mermaid
flowchart LR
    Repo[Repo with mixed content]
    Repo --> Public[Public modules]
    Repo --> Sensitive[regulated/ + secrets/]
    Public --> Copilot[Copilot active]
    Sensitive --> Block[Copilot blocked<br/>via content exclusion]
    Copilot --> Devs[IDE]
    Block --> Devs
```

---

[Master Index](00-MASTER-INDEX.md)
