---
marp: true
paginate: true
style: |
  @import 'themes/svenskaspel_techy.css';

---

<!-- _class: lead -->

# 🎯 Promotion prerequisits 

*Understanding how we package components and systems*

**Key Topics:**
- Building and Packaging components
- Creating system(s) from components
- Best practices for component deployment and management

*Technical foundation for our deployment architecture*

---

<div class="slide-header">🚀 Component vs System</div>

<div class="content-area">

- 📦 **Component** → application in a Docker image published to a Docker registry + Helm chart that describes how the application should be run by default
- 🏗️ **System** → umbrella chart containing dependent charts that work together as a cohesive unit
- 🚀 **Delivery** → systems are the entities that we deliver through review, staging and production environments

</div>

---

<div class="slide-header">🔄 Packaging Components</div>

<div class="content-area">

- 📦 **Docker Image** → Components are packaged as Docker images containing the application code and runtime dependencies
- 📋 **Helm Chart** → How the component should be run by default is packaged as a Helm chart for the specific application
- 🏷️ **Registry Storage** → Both Docker images and Helm charts are published to registries (GHCR) for distribution
- 🔧 **Default Configuration** → Helm charts include default values, resource limits, and deployment configurations

</div>

---

<div class="slide-header">🔄 Packaging Systems</div>

<div class="content-area">

- 🏗️ **Umbrella Chart** → Systems are packaged using an umbrella chart that orchestrates multiple components
- 🎯 **System Archetypes** → Different patterns based on purpose:
  - **Microservice** → Business logic service with APIs and databases
  - **Client** → Frontend applications with web servers and assets
  - **Platform** → Shared infrastructure like monitoring or authentication
- 📦 **Component Dependencies** → References both internal components and external charts from the internet
- 🔄 **Environment Promotion** → Complete systems move through review → staging → production

</div>

---

<div class="slide-header">🔄 Helm Deployment Flow</div>

<div class="content-area">

![Helm Deployment Flow](diagrams/helm_deployment_flow.svg)

**From Code to Production:** Complete pipeline showing how applications flow from GitHub through build, packaging, and system deployment

</div>

---

<div class="slide-header">❓ Questions?</div>

<div class="content-area">

*Let's discuss how this impacts our deployment strategy!*

</div>
