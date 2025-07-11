---

## title: report\_a04\_part01\_prompt

---

## Prompt Strategy for A04a: Custom Tracking System

---

### Goal

<details>
<summary>Clarify the objective of the prompt plan</summary>

---

* Generate a complete implementation plan for a custom app/web tracking system
* Ensure it meets enterprise-grade requirements across architecture, attribution, data flow, security, and compliance
* Structure the markdown to comply with `ctx_doc_style.md`

---

</details>

### Prompt Techniques

<details>
<summary>AI prompting approach used to build each section</summary>

---

* **Overview and Objectives**

  * Asked: "Define clear technical, business, and stakeholder goals for building a custom tracking system"
  * Rewrote user requirements into structured bullets using ctx\_doc\_style

* **Architecture Design**

  * Prompted: "Give a detailed breakdown of tracking SDK, event API, attribution, storage, monitoring components"
  * Followed up with: "How do these components interact in flow and storage pipeline?"
  * Used Mermaid `flowchart TD` for infrastructure diagram

* **Technical Implementation Strategy**

  * Prompted for step-by-step logic on tracking link creation, fingerprinting, install event processing
  * Generated pseudocode and JSON samples for:

    * Redirect logging
    * Attribution match logic
    * Install payload

* **Attribution Engine Logic**

  * Prompted: "Show hierarchy of ID matching: device\_id, cookie\_id, user\_id"
  * Requested SQL and Python attribution examples: last-touch, first-touch, multi-touch

* **Privacy and Security**

  * Asked: "What APIs and encryption/hashing mechanisms are needed for GDPR/CCPA?"
  * Prompted for Python, SQL, JavaScript samples (e.g., HMAC, field encryption)

* **Infrastructure and Scaling**

  * Asked: "Estimate monthly cost of Kafka/Flink/Postgres/Redis + monitoring"
  * Used GPT-generated cost approximations and typical AWS/GCP pricing

* **Validation and Testing**

  * Prompted: "Provide full QA plan for SDK, APIs, load tests, CI"
  * Structured checklist of test strategies including integration, security, replay/debug

* **Integration API Specs**

  * Prompted: "Write RESTful API definitions for /v1/event, /v1/click, /v1/install, /v1/user/delete"
  * Asked for code examples for payloads, response, HMAC headers

---

</details>

### Iteration Process

<details>
<summary>Track how the output was refined across sessions</summary>

---

* First session focused on basic structure and ctx\_doc\_style compliance
* Second round introduced diagrams, pseudocode, and deep dive into attribution
* Later sessions added edge case logic, monitoring instrumentation, and Gantt chart
* Final session covered:

  * Stakeholder insights
  * Scaling costs
  * Testing methods
  * Extended content to meet 1000+ line requirement

---

</details>

### Tools Used

<details>
<summary>List of GenAI features and tools applied</summary>

---

* Mermaid syntax generation for diagrams (flowchart, sequence, gantt)
* Pseudocode and code block synthesis (Python, JS, SQL, Kotlin, Scala)
* ctx\_doc\_style enforcement via structured formatting prompts
* Markdown splitting across `details` and `summary` per section
* Prompt memory for maintaining structure, formatting consistency, and reuse of schema

---

</details>
