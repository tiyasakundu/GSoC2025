# GSoC2025

![ViewCount](https://views.whatilearened.today/views/github/tiyasakundu/GSoC2025.svg)
![GitHub](https://img.shields.io/github/followers/tiyasakundu?style=social)
![GitHub Stars](https://img.shields.io/github/stars/tiyasakundu/GSoC2025?style=social)

<a href = "https://summerofcode.withgoogle.com/programs/2025/projects/QJCf0exh">  ![Summer-of-code](/files/GSoC_header.png)</a>

<h2><i>Completion of the FOSSology UI using React.js and Next.js @ <a href = "https://www.fossology.org/">FOSSology </a></i></h2>

# Project Details <img src="files/projectdetails.png" width="30"/>

## What's the project about?

The FOSSology UI Completion Project aims to finalize and enhance the
React-based user interface that was previously initiated but remained incomplete
due to limited REST API support. Several pages currently lack full functionality
and proper data integration. This project focuses on completing those pages,
improving the UI/UX structure, and aligning the interface with FOSSology REST
API v2, transitioning away from the deprecated v1 implementation. The goal is
to deliver a more stable, user-friendly, and maintainable UI for the FOSSology
ecosystem.
  
# Contributions <img src="files/contributions.png" width="30"/>

## 1. Migration of FOSSology Frontend from React to Next.js

The entire FOSSology UI was migrated from an outdated **React 17 CRA setup** to a modern **Next.js (App Router) architecture**, using **pnpm** for package management.

- Set up a fresh Next.js development environment.
- Migrated all major pages: **Home, Search, Browse, Organize, Upload, Agents scheduling, User management, etc.**
- Migrated reusable components: **Header, Footer, SubHeader, Table, TreeContainer, Widgets, Modal, CommonFields, etc.**
- Unified REST API integration with FOSSology API v2, updating API variables to ensure stable responses.
- Extracted all **inline styles** into a structured **global CSS file**, improving maintainability.

📌 Pull Request: [chore(rca): migrate from react 17 to next 15](https://github.com/fossology/FOSSologyUI/pull/315) — *migrated frontend setup to Next.js*

## 2. Introduction of Modern Styling: Tailwind CSS + Shadcn UI

Replaced the legacy **Bootstrap/React-Bootstrap/Material UI** setup with a modern, lightweight styling approach:

- Configured **Tailwind CSS** in the Next.js app.
- Integrated **Shadcn UI** for reusable, accessible, and customizable components.
- Installed and implemented core components such as **Button, Input, Dropdown, Card, Modal, etc.**
- Established a global styling strategy, enabling consistent and scalable UI development.

📌 Pull Request: [feat(nextjs): implement the redesigned ui pages using Tailwind CSS](https://github.com/fossology/FOSSologyUI/pull/318) — *introduced Tailwind + Shadcn setup*

## 3. Implementation of Redesigned Pages (Figma → Next.js)

Converted the Figma mockups from the ![FOSSology UX and UI Redesign](https://github.com/fossology/fossology/discussions/2908#discussioncomment-11912320) project into a fully functional UI.

- Implemented redesigned **Header, Footer, and SubHeader** components.
- Sequentially migrated and redesigned key pages:

  - **Home Page** (entry point with a refreshed layout).
  - **Search Page** (modernized UI with clean results presentation).
  - **Schedule Agents Page** (implemented with modular CommonFields).
  - **Upload File Page** (including the Reuse Overlay).
- Introduced a **reusable Modal component** for confirmation dialogs.

📌 Pull Request: [feat(nextjs): Pages redesigned and implemented using Tailwind](https://github.com/fossology/FOSSologyUI/pull/328) — *migrated and redesigned core pages*

## 4. Codebase Stabilization and Fixes

- Removed legacy **Bootstrap and Material UI dependencies**.
- Refactored inline styles into **global CSS structure**.
- Fixed API variable handling for compatibility with REST API v2.
- Resolved **CSR bailout warnings** in Next.js by wrapping client components with `Suspense`.

📌 Pull Request: [fix: wrap client components with Suspense to resolve CSR bailout warnings (closes #320)](https://github.com/fossology/FOSSologyUI/pull/324) — *stability fixes*

## 5. Collaboration & Project Direction

- Worked with mentors to finalize core tech-stack decisions:
  - **Next.js** (App Router) for modern frontend development.
  - **Tailwind + Shadcn** (instead of Bootstrap/Material UI).
- Coordinated with the designer to review Figma files and plan the redesign implementation.
- Shared weekly progress updates with the FOSSology community.

## 6. Before vs After – UI Migration and Redesign

The FOSSology UI originally used **React with Bootstrap/React-Bootstrap**, which had several limitations:

- Heavy dependency on pre-styled Bootstrap components, making customization difficult.
- Inline CSS scattered across components, reducing maintainability.
- Lack of compatibility with modern **React Server Components**.
- Outdated design and non-uniform styling across the UI.

With the migration to **Next.js + Tailwind + Shadcn**, the UI was modernized with:

- A fully **Next.js-based codebase** with server–client separation.
- **Tailwind CSS** for atomic, customizable, and performant styling.
- **Shadcn UI components** (Button, Card, Input, Dropdown, etc.) integrated for consistency and accessibility.
- Cleaner structure with **global CSS** for shared styles and removal of inline CSS.
- Redesigned pages aligned with the shared Figma designs.

### Example 1: Header and Footer

- **Before (React Bootstrap):** Default-styled navigation bar and footer, limited customization.
  ![alt text](/files/header.png) ![alt text](/files/footer.png)
- **After (Next.js + Tailwind + Shadcn):** Fully customized, responsive, and modern UI components.
  ![alt text](/files/newheader.png) ![alt text](/files/newfooter.png)
  

### Example 2: Home Page

- **Before:** Bootstrap-based layout with inline CSS, limited flexibility.
  ![alt text](/files/homepage.png)
- **After:** Tailwind-styled modular layout, aligned with Figma redesign.
  ![alt text](/files/newhomepage.png)

### Example 3: Upload a File Page

* **Before:** Old layout with inconsistent UI elements and Bootstrap defaults.
  ![alt text](/files/uploadafilepage.png)
* **After:** Clean and modern UI with Tailwind utilities and Shadcn components for accessibility.
  ![alt text](/files/newuploadafilepage.png)

The migration modernized the entire frontend, reduced technical debt, and provided a scalable foundation for future development.

# Deliverables <img src="files/deliverables.png" width="30"/>
|                               Tasks                               | Planned |       Completed      |
| :---------------------------------------------------------------: | :-----: | :------------------: |
| Migration of Modern Stack (React 17 → 19, CRA → Vite, npm → pnpm) |   Yes   | :heavy\_check\_mark: |
|         Next.js Integration (Setup & Component Migration)         |   Yes   | :heavy\_check\_mark: |
|                 Completion of Incomplete UI Pages                 |   Yes   | In Progress |
|    UI/UX Restructuring (based on design prototypes & feedback)    |   Yes   | :heavy\_check\_mark: |
|            REST API v2 Alignment (removal of v1 usage)            |   Yes   | In Progress |
|                    Bug Fixes & Issue Resolution                   |   Yes   | :heavy\_check\_mark: |
|                    Storybook Component Library                    |   Yes   | In Progress |
|                  Developer Documentation Support                  |   Yes   | :heavy\_check\_mark: |


# Future Plans <img src="files/futureplans.png" width="30"/>

1. Implement all the redesigned pages with a modern UI using Tailwind CSS and Shadcn.
2. Complete the migration from REST API v1 to REST API v2 for all endpoints.
3. Implement and document the Storybook component library for reusable UI components.

# Things I learned from Google Summer of Code <img src="files/learnings.png" width="30"/>

- Gained in-depth understanding of migrating a large-scale React application to **Next.js** with modern conventions.
- Learned the differences between **Bootstrap** and **Tailwind CSS**, and why Tailwind with Shadcn is better suited for scalable and customizable UI design.
- Improved knowledge of **server-side rendering (SSR)**, **client components**, and React Server Components (RSC).
- Set up and managed projects with **pnpm**, exploring the advantages over npm/yarn in workspace management.
- Strengthened understanding of **REST APIs** and challenges in migrating from v1 to v2.
- Improved skills in **refactoring legacy codebases** by extracting inline CSS to a maintainable global CSS structure.
- Understood how to collaborate with **designers via Figma** and translate design systems into clean, maintainable code.
- Brushed up **Tailwind CSS** skills and explored **component-driven development** with Storybook.
- Improved ability to handle **large pull requests** and maintain good GitHub practices (draft PRs, commits, reviews).
- Learned the importance of **progressive migration strategy**—first completing functionality, then focusing on styling.
- Enhanced my **communication and collaboration skills** during regular sync meetings with mentors and contributors.
- Strengthened time management and ability to break down large tasks into achievable weekly deliverables.
