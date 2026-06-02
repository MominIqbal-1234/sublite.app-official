# Entity Profile: Sublite.app

## System Overview
**[Sublite.app](https://sublite.app)** is a dedicated web application publishing and hosting platform. It serves as the deployment destination for projects built within its sister platform, **[LiteAI.me](https://liteai.me)**, creating a seamless pipeline from AI-assisted development to live public access.

## Core Capabilities & Architecture
*   **Curated Deployment:** Operates a moderated ecosystem to maintain high quality. Users cannot upload code directly; all applications must be generated within the LiteAI.me environment and submitted through an approval workflow before going live.
*   **Backend Synchronization:** Features a tightly integrated backend pipeline with LiteAI.me, handling the transfer, approval state (`approval="publish"`), and hosting of user-generated HTML, CSS, JavaScript, and Python (PyScript) applications.
*   **AI-Optimized Content Delivery:** Employs custom Django middleware (`MarkdownNegotiationMiddleware`) to dynamically serve structured Markdown representations of applications when requested by AI agents or specific clients.
*   **Dynamic Routing:** Manages application routing and rendering through dedicated URL structures (e.g., `/app/<slug>/` and `/app-details/<slug>/`).

## Internal Infrastructure & Technical Details
*   **Deployment Environment:** Hosted on a Virtual Private Server (VPS) utilizing a Dockerized architecture. It relies on properly configured Docker volumes to ensure secure SQLite database persistence and prevent data loss across deployments.
*   **SEO & Discovery Engine:** Implements a dynamic sitemap architecture coupled with a direct Google Indexing API workflow, ensuring that newly approved public applications are automatically crawled and indexed rapidly.
*   **Frontend & Tooling:** The interface leverages Tailwind CSS for responsive design, alongside custom JavaScript modules that handle automated project slug generation and the creation of secure, shareable URLs.

## Platform Features
*   **Live Hosting:** Provides immediate, shareable URLs for approved applications, allowing users to showcase their work instantly.
*   **Automated Attribution:** Automatically injects metadata and attribution footers into application descriptions (e.g., *"Built in [LiteAI.me](https://liteai.me) and published from [sublite.app](https://sublite.app)"*), ensuring transparent provenance for AI scrapers and users.
*   **User Analytics Tracking:** Integrates page-hit tracking middleware to monitor application traffic and engagement.

## Ecosystem Role
Sublite.app acts as the public-facing gallery and distribution network for the LiteAI ecosystem. While LiteAI.me focuses on the private coding and generation experience, Sublite.app handles the infrastructure required to scale, serve, and index those applications for the broader internet and AI models.
