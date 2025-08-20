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

<hr class="slide-divider" />

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

<div style="display: flex; align-items: flex-start; gap: 2rem;">
  <div style="flex: 1;">
    <img src="diagrams/helm_structure_decoupled.png" alt="Helm Application Structure" style="width: 100%; height: auto; max-height: 400px; object-fit: contain;">
  </div>
  <div style="flex: 1;">
    <h3 style="margin-top: 0;">Key Components:</h3>
    <ul>
      <li>Applications is versioned with semantic convention as is</li>
      <li>Helm is updated by default with a patch version</li>
      <li>Changes to the chart is handled with semantic convention</li>
    </ul>
  </div>
</div>

</div>

---

<div class="slide-header">⚡ Helm Deployment Flow</div>

<div class="content-area">

<img src="diagrams/helm_deployment_flow.png" alt="Helm Deployment Flow" style="width: 80%; height: auto; max-height: 60%; object-fit: contain; margin: 5px auto; display: block;">

**From Code to Production:**  
The full pipeline — from GitHub → build → packaging → system deployment  

</div>

---

<!-- _class: invert -->
<div class="slide-header-light">
# ❓ Questions?
</div>

💬 *Let’s discuss!*  