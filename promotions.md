---
marp: true
paginate: true
style: |
  @import 'themes/svenskaspel_techy.css';
---

<!-- _class: lead -->

# 🎯 Components, Systems and Promotions

> Packaging is **more than containerizing apps** —  
> it’s about **reusable components**,  
> **system orchestration with umbrella charts**, and  
> **seamless deployment pipelines**.

*The technical foundation of our deployment architecture*

---

<div class="slide-header">🚀 Component vs. System</div>

<div class="content-area">

> - 📦 **Component** → Application packaged as a Docker image in a registry  
> - 📋 **Helm Chart** → Default deployment definition for 
a component  

<hr />

> - 🏗️ **System** → Umbrella chart combining multiple components into one cohesive unit  
> - 🚀 **Delivery** → We promote systems (not individual components) through review → staging → production

</div>

---

<div class="slide-header">📦 Packaging Components</div>

<div class="content-area">

- 🐳 **Docker Image** → Bundles application code + runtime dependencies  
- 📋 **Helm Chart** → Defines how the component is deployed by default  
- 🏷️ **Registry** → Images and charts are published to GHCR for distribution  
- ⚙️ **Default Config** → Includes sensible defaults for resources, limits, and deployment settings  

</div>

---

<div class="slide-header">🏗️ Packaging Systems</div>

<div class="content-area">

- 🛠️ **Umbrella Chart** → Orchestrates multiple components into one system  
- 🎯 **Example System Archetypes**:
  - **Microservice** → API + business logic + database  
  - **Client** → Frontend apps with assets + web servers  
  - **Managed Service** → Shared infra like monitoring or authentication  
- 🔗 **Dependencies** → Includes internal charts + external charts  for components
- 🔄 **Promotion** → Entire systems move through environments: review → staging → production  

</div>

---


<div class="slide-header">⚡ Helm Application Structure</div>

<div class="content-area">

<img src="diagrams/helm_structure_decoupled.png" alt="Helm Deployment Flow" style="width: 80%; height: auto; max-height: 60%; object-fit: contain; margin: 5px auto; display: block;">

**Application Structure:**  
How components are organized within Helm charts and umbrella systems  

</div>

---

<div class="slide-header">⚡ Helm Deployment Flow</div>

<div class="content-area">

<img src="diagrams/helm_deployment_flow.png" alt="Helm Deployment Flow" style="width: 80%; height: auto; max-height: 60%; object-fit: contain; margin: 5px auto; display: block;">

**From Code to Production:**  
The full pipeline — from GitHub → build → packaging → system deployment  

</div>

---

<div class="slide-header">❓ Questions</div>

<div class="content-area">

💬 *How does this shape our deployment strategy?*  

</div>