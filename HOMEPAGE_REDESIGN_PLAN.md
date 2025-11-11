# Homepage Redesign Plan

This document outlines the strategy and steps for redesigning the homepage of the Sign Language Tech website.

## 1. Objective

To create a new homepage that is visually impactful, simple, and human. It will immediately communicate the agency's unique identity, showcase its technical credibility, and guide potential clients toward making contact.

## 2. Guiding Principle

The redesign will be based on the **"Human-First Narrative"** concept. We will lead with the most powerful and unique aspect of the brand: the story of its Deaf-engineer founders. The goal is to build an immediate connection with the visitor, grounding the agency's technical services in a powerful mission.

## 3. New Homepage Structure

The new homepage will be composed of several distinct, reusable components. This will create a clean, modular, and maintainable structure.

The planned component flow is:

1.  Hero Section
2.  Mission Snippet
3.  Learning & Community
4.  Featured Project
5.  Blog Highlights
6.  Final Call-to-Action (CTA)

## 4. Component Breakdown & Content Strategy

Here are the components to be built and the content they will feature:

### a. `Hero.astro`

*   **Purpose:** To make a strong first impression.
*   **Visual:** A high-quality background image or silent video of the founders.
*   **Headline (H1):** "We are Deaf engineers. We build accessible technology for everyone."
*   **Sub-headline:** "Bridging worlds through code and sign."
*   **CTAs:**
    *   Primary Button: "Our Story" (links to `/about`)
    *   Secondary Button: "See Our Work" (links to `/projects`)

### b. `MissionSnippet.astro`

*   **Purpose:** To concisely state the core mission, balancing business solutions with community empowerment.
*   **Headline:** "Our Mission: Building Bridges Through Technology"
*   **Content:** This will pull directly from the `about` page, emphasizing both aspects: "Our mission is simple: to create exceptional software solutions that empower users. We specialize in cloud-native software services and web application development, driven by an unwavering commitment to quality, innovation, and universal digital accessibility. We are dedicated to **Empowering the Deaf Community through Technology and Innovation**, ensuring our work benefits both our clients and the wider community."

### c. `LearningAndCommunity.astro`

*   **Purpose:** To highlight educational and community-focused offerings.
*   **Headline:** "Learn & Grow with Sign Language Tech"
*   **Content:** "Master coding with interactive tutorials, insightful interviews, and workshops delivered in International or American Sign Language."
*   **CTA:** "Explore Learning Resources" (links to a dedicated learning/community page, or filtered blog posts/videos)

### d. `ProjectHighlight.astro`

*   **Purpose:** To provide a concrete example of your work and impact.
*   **Content:** This component will feature the **"Sign Tours Hungary"** project, as it has a powerful story and an excellent client testimonial.
    *   **Image:** `sth-location-detail-chain-bridge.webp`
    *   **Title:** Sign Tours Hungary
    *   **Impact Statement:** "Enabled thousands of Deaf travelers to experience Hungarian culture through a fully accessible, visual-first web platform."
    *   **Testimonial Snippet:** The powerful quote from the JOF Foundation CEO.
    *   **CTA:** "View Case Study" (links to `/projects`)

### e. `BlogHighlight.astro`

*   **Purpose:** To showcase thought leadership and community involvement.
*   **Headline:** "Community and Insights"
*   **Content:** This will display the **three most recent blog posts**.
    *   For each post, it will show the featured image, title, and a short description.
    *   This will dynamically pull from the `blog` content collection. This section highlights our engagement with the broader tech ecosystem and our commitment to sharing knowledge.

### f. `FinalCTA.astro`

*   **Purpose:** To provide a clear, final prompt for user action.
*   **Headline:** "Have a project in mind?"
*   **Sub-headline:** "Let's build something better, together."
*   **CTA:** "Book a Free Consultation" (links to the `cal.com` page)

## 5. Implementation Steps

I will proceed in the following order:

1.  **Clear the existing `src/pages/index.astro`** to create a blank canvas.
2.  **Create each new component** one by one in the `src/components/` directory (`Hero.astro`, `MissionSnippet.astro`, etc.).
3.  **Populate each component** with the specified static and dynamic content.
4.  **Assemble the components** within `src/pages/index.astro` in the correct order.
5.  **Apply styling** to ensure the final page is polished, responsive, and visually aligned with the brand.
