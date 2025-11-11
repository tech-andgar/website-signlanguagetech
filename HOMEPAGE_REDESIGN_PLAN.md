# Homepage Redesign Plan

## 1. Vision & Objective

Create a powerful, human-centered homepage that immediately communicates Sign Language Tech's unique identity: **founded by Deaf engineers who build accessible technology from lived experience, not afterthought**.

**Core Message:** "Code with Purpose, Communication without Barriers"

**Goals:**
- Instant emotional connection through founder story
- Establish technical credibility for CNCF/cloud-native audience
- Drive conversions: consultations, project inquiries, community engagement
- Differentiate from competitors through authentic accessibility expertise

---

## 2. Design Principles

### Visual Identity
- **Color Palette** (current styles maintained):
  - Primary: `--accent: #2337ff` (bright blue)
  - Dark variant: `--accent-dark: #000d8a`
  - Text: `rgb(var(--black))` / `rgb(var(--gray-dark))`
  - Backgrounds: Light mode gray gradient, dark mode black gradient
  - Interactive states: existing hover/selection colors

### Typography
- **Font Family:** Atkinson (current)
- **Hierarchy:**
  - H1: 3.052em - Hero headlines only
  - H2: 2.441em - Section titles
  - H3: 1.953em - Subsections
  - Body: 20px base (16px mobile)

### Layout
- **Max Width:** 960px centered
- **Spacing:** 120px vertical between sections (consistent)
- **Grid:** Flexible, responsive (mobile-first)
- **Images:** High-quality, meaningful (not decorative)

---

## 3. Homepage Structure

### Component Flow
1. **HeroSection** - Immediate impact & identity
2. **MissionStatement** - Our unique advantage
3. **ValueProposition** - Why choose us (3 pillars)
4. **ImpactShowcase** - Real results (featured project)
5. **CommunityHighlight** - Thought leadership
6. **CTASection** - Clear next steps

**Total Sections:** 6 (streamlined from previous plan)

---

## 4. Component Specifications

### 4.1 HeroSection.astro

**Purpose:** Create immediate emotional connection through authentic founder story

**Design:**
```
┌─────────────────────────────────────────────────┐
│                                                 │
│  [High-quality image: founder(s) coding/signing]│
│                                                 │
│  H1: "We are Deaf engineers.                   │
│       We build accessible technology            │
│       for everyone."                            │
│                                                 │
│  Subheading: "Bridging worlds through code      │
│              and sign language."                │
│                                                 │
│  [Primary CTA] [Secondary CTA]                  │
│                                                 │
└─────────────────────────────────────────────────┘
```

**Content:**
- **Headline (H1):** "We are Deaf engineers. We build accessible technology for everyone."
- **Subheading:** "Bridging worlds through code and sign language."
- **Visual:** Professional photo of founders (coding, presenting, or signing) - conveys both technical expertise and Deaf identity
- **CTAs:**
  - Primary: "Our Story" → `/about`
  - Secondary: "View Our Work" → `/projects`

**Styling:**
- Full-width background image with overlay
- Text centered or left-aligned over image
- High contrast for readability
- Mobile: stack elements vertically

**Assets Needed:**
- Founder photo (professional, aspirational)
- Alternative: `slt-my-profile-dark.webp` / `slt-my-profile-light.webp`

---

### 4.2 MissionStatement.astro

**Purpose:** Articulate unique value proposition - accessibility as competitive advantage

**Design:**
```
┌─────────────────────────────────────────────────┐
│  H2: "Your Advantage: Accessible by Design"    │
│                                                 │
│  "Our identity isn't just a feature; it's our  │
│   greatest strength. As members of the Deaf    │
│   community, we live and breathe accessibility.│
│   We understand firsthand the barriers that    │
│   non-inclusive design creates—and the         │
│   opportunities it unlocks."                    │
│                                                 │
│  "We specialize in cloud-native software and   │
│   web development, building accessibility from │
│   the core, not as an afterthought."           │
│                                                 │
└─────────────────────────────────────────────────┘
```

**Content:**
- **Headline (H2):** "Your Advantage: Accessible by Design"
- **Body:** Condensed mission from propusal.md (English version)
  - Emphasize lived experience → better products
  - Bridge to business value: cloud-native, web apps
  - NO generic mission statements

**Styling:**
- Centered text block, max-width 800px
- Padding: 60px vertical
- Background: subtle gradient or solid
- Typography: H2 + body copy (1.1em)

**Key Differentiator:**
Unlike competitors who "add" accessibility, we build it from lived experience.

---

### 4.3 ValueProposition.astro

**Purpose:** Showcase three core pillars that make SLT unique

**Design:**
```
┌──────────────────────────────────────────────────┐
│  H2: "Built on Three Pillars"                   │
│                                                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐      │
│  │ [Icon 1] │  │ [Icon 2] │  │ [Icon 3] │      │
│  │          │  │          │  │          │      │
│  │ Empathy- │  │ Quality  │  │Seamless  │      │
│  │  Driven  │  │    by    │  │Collabora-│      │
│  │Innovation│  │  Design  │  │   tion   │      │
│  │          │  │          │  │          │      │
│  │ [Short   │  │ [Short   │  │ [Short   │      │
│  │  desc]   │  │  desc]   │  │  desc]   │      │
│  └──────────┘  └──────────┘  └──────────┘      │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Content:**
Based on propusal.md "Our Values" section:

1. **Empathy-Driven Innovation**
   - Icon: Heart/Lightbulb combination
   - Text: "We solve complex problems with elegant solutions that put the end-user first."

2. **Quality by Design**
   - Icon: Shield/Checkmark
   - Text: "Accessible software is inherently better—more robust, usable, and scalable."

3. **Seamless Collaboration**
   - Icon: Connected nodes/Communication
   - Text: "Direct, frictionless communication ensuring your vision translates perfectly."

**Styling:**
- Three-column grid (stack on mobile)
- Icons: simple SVG, branded color
- Card-style with subtle borders
- Hover: lift effect (transform: translateY(-5px))

**Color Usage:**
- Icons: `var(--accent)`
- Borders: `rgb(var(--gray-light))`
- Hover: `box-shadow: var(--box-shadow)`

---

### 4.4 ImpactShowcase.astro

**Purpose:** Demonstrate real-world impact through featured project (Sign Tours Hungary)

**Design:**
```
┌──────────────────────────────────────────────────┐
│  H2: "Real Impact, Real Results"                │
│                                                  │
│  ┌────────────────┬─────────────────────────┐   │
│  │                │  Sign Tours Hungary     │   │
│  │  [Project      │                         │   │
│  │   Image]       │  "Enabled thousands of  │   │
│  │                │   Deaf travelers to     │   │
│  │                │   experience Hungarian  │   │
│  │                │   culture through a     │   │
│  │                │   fully accessible      │   │
│  │                │   platform."            │   │
│  │                │                         │   │
│  │                │  The Challenge:         │   │
│  │                │  [Brief description]    │   │
│  │                │                         │   │
│  │                │  Our Solution:          │   │
│  │                │  [Key points]           │   │
│  │                │                         │   │
│  │                │  "The entire process—  │   │
│  │                │   from technical        │   │
│  │                │   meetings to code      │   │
│  │                │   reviews—was conducted │   │
│  │                │   entirely in sign      │   │
│  │                │   language."            │   │
│  │                │   — JOF Foundation CEO  │   │
│  │                │                         │   │
│  │                │  [View Full Case Study] │   │
│  └────────────────┴─────────────────────────┘   │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Content:**
- **Featured Project:** Sign Tours Hungary (from propusal.md)
- **Image:** `sth-location-detail-chain-bridge.webp`
- **Impact Statement:** "Enabled thousands of Deaf travelers to experience Hungarian culture through a fully accessible, visual-first platform."
- **The Challenge:** Brief (2-3 sentences) from propusal
- **Our Solution:**
  - Visual-first UX/UI
  - Interactive map + video player
  - Full i18n support
  - Native sign language collaboration
- **Testimonial:** Elevated quote from JOF Foundation
- **CTA:** "View Full Case Study" → `/projects#sign-tours-hungary`

**Styling:**
- Two-column layout (image left, content right)
- Image: full-height, object-fit: cover
- Testimonial: distinct styling (italic, larger font, border-left accent)
- Mobile: stack vertically

**Metrics to Include:**
- "250+ minutes of sign language content"
- "30 cultural landmarks"
- "Conducted entirely in sign language"

**Why This Project:**
- Shows technical capability (i18n, video, maps)
- Demonstrates accessibility expertise
- Client testimonial adds credibility
- Relevant to CNCF (web tech, UX)

---

### 4.5 CommunityHighlight.astro

**Purpose:** Position as thought leaders, showcase community engagement

**Design:**
```
┌──────────────────────────────────────────────────┐
│  H2: "Insights & Community"                     │
│                                                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐      │
│  │ [Image]  │  │ [Image]  │  │ [Image]  │      │
│  │          │  │          │  │          │      │
│  │ KubeCon  │  │ JSConf   │  │ Sign to  │      │
│  │ London   │  │ Budapest │  │ Text AI  │      │
│  │ 2025     │  │ 2024     │  │          │      │
│  │          │  │          │  │          │      │
│  │ [Read]   │  │ [Read]   │  │ [Read]   │      │
│  └──────────┘  └──────────┘  └──────────┘      │
│                                                  │
│  [Explore All Insights →]                       │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Content:**
- **Headline (H2):** "Insights & Community"
- **Featured Posts:** 3 curated (NOT most recent, most impactful)
  1. **KubeCon London 2025** - Shows CNCF involvement
  2. **JSConf Budapest 2024** - Community presence
  3. **Sign to Text AI Revolution** - Technical innovation

**Each Card:**
- Featured image
- Title (clickable)
- 1-sentence excerpt (optional)
- "Read More →" link

**CTA:** "Explore All Insights" → `/blog`

**Styling:**
- Three-column grid (2-col tablet, 1-col mobile)
- Cards: image (16:9 ratio), title, minimal text
- Hover: scale image slightly, lift card
- Images: `border-radius: 8px`

**Dynamic Logic:**
```astro
---
import { getCollection } from 'astro:content';
const featuredSlugs = [
  'kubecon-london-2025',
  'jsconf-budapest-2024',
  'sign-to-text-ai-revolution'
];
const allPosts = await getCollection('blog');
const featuredPosts = featuredSlugs.map(slug =>
  allPosts.find(post => post.slug === slug)
);
---
```

**Why These Posts:**
- KubeCon: CNCF credibility
- JSConf: Broader tech community
- AI: Innovation leadership
- NO overlap with existing blog page (which shows chronological)

---

### 4.6 CTASection.astro

**Purpose:** Clear, compelling final call-to-action

**Design:**
```
┌──────────────────────────────────────────────────┐
│                                                  │
│          Have a project in mind?                │
│                                                  │
│     Let's build something better, together.     │
│                                                  │
│       [Book a Free Consultation →]              │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Content:**
- **Headline (H2):** "Have a project in mind?"
- **Subheading:** "Let's build something better, together."
- **CTA Button:** "Book a Free Consultation"
  - Link: Uses existing `BookAppointmentButton.astro` component
  - Opens: Cal.com booking (existing functionality)

**Styling:**
- Centered content
- Large padding (100px vertical)
- Background: subtle gradient or accent color (5% opacity)
- Button: Primary style, prominent size

**Psychological Triggers:**
- "Free" removes barrier
- "Consultation" less intimidating than "sales call"
- "Together" collaborative tone

---

## 5. Typography & Spacing Standards

### Heading Scales
```css
H1 (Hero only):     3.052em (61px @ 20px base)
H2 (Sections):      2.441em (49px @ 20px base)
H3 (Subsections):   1.953em (39px @ 20px base)
Body:               1em (20px, 16px mobile)
Large Body:         1.1em (22px)
```

### Vertical Rhythm
```css
Section margin-bottom:  120px
Component padding:      60px vertical
Paragraph spacing:      1em (20px)
Heading margin-bottom:  0.5em
```

### Responsive Breakpoint
```css
@media (max-width: 720px) {
  /* Mobile adjustments */
}
```

---

## 6. Color Application Guide

### Light Mode
- **Background:** `linear-gradient(var(--gray-gradient))`
- **Text Primary:** `rgb(var(--gray-dark))` - #22293
- **Text Secondary:** `rgb(var(--gray))` - #60739F
- **Headings:** `rgb(var(--black))` - #0F1219
- **Accent:** `#2337ff`
- **Borders:** `rgb(var(--gray-light))` - #E5E9F0

### Dark Mode
- **Background:** `linear-gradient(var(--black-gradient))`
- **Text Primary:** `rgba(var(--white), 0.5)`
- **Text Bright:** `rgba(var(--white), 0.8)`
- **Headings:** `rgb(var(--white), 0.8)`
- **Accent:** `#2337ff` (same)

### Interactive States
- **Selection:** `background: #352e7e`, `color: #fff`
- **Link Hover:** `rgb(var(--gray))` or `rgb(var(--white), 0.8)`
- **Button Hover:** Transform or opacity change

---

## 7. Image Assets

### Required Images
1. **Hero Background:**
   - Option A: New founder photo (professional)
   - Option B: Existing `slt-my-profile-dark.webp`
   - Dimensions: 1920x1080 minimum
   - Format: WebP optimized

2. **Value Proposition Icons:**
   - Custom SVG icons (3 total)
   - Style: Simple, line-based
   - Color: Match accent brand color

3. **Impact Showcase:**
   - `sth-location-detail-chain-bridge.webp` (existing)

4. **Community Highlight:**
   - `kubecon-london-interpreter.webp`
   - `jsconf-budapest-2024` (TBD from blog)
   - `sign-to-text` related image

### Image Optimization
- Format: WebP preferred
- Max size: 1MB per image
- `alt` text: descriptive, accessible
- Loading: `loading="lazy"` except hero

---

## 8. Content Guidelines

### Tone & Voice
- **Direct:** No marketing fluff
- **Human:** Personal, authentic
- **Confident:** Expert positioning
- **Inclusive:** Welcoming language

### Writing Rules
1. **Lead with value:** What's in it for the visitor?
2. **Show, don't tell:** Use specific examples
3. **Active voice:** "We build" not "Software is built"
4. **Concise:** Every word earns its place
5. **Scannable:** Use headings, bullets, short paragraphs

### SEO Considerations
- H1: One per page, includes primary keyword
- Meta description: 150-160 characters
- Image alt text: Descriptive, keyword-aware
- Internal links: Strategic to `/about`, `/projects`, `/blog`

---

## 9. Technical Implementation

### File Structure
```
src/
├── components/
│   └── home/
│       ├── HeroSection.astro          (new)
│       ├── MissionStatement.astro     (new)
│       ├── ValueProposition.astro     (new)
│       ├── ImpactShowcase.astro       (new)
│       ├── CommunityHighlight.astro   (new)
│       └── CTASection.astro           (new)
├── pages/
│   └── index.astro                    (refactor)
└── styles/
    └── global.css                     (maintain current)
```

### Component Architecture
```astro
---
// src/pages/index.astro
import Layout from '../layouts/Layout.astro';
import HeroSection from '../components/home/HeroSection.astro';
import MissionStatement from '../components/home/MissionStatement.astro';
import ValueProposition from '../components/home/ValueProposition.astro';
import ImpactShowcase from '../components/home/ImpactShowcase.astro';
import CommunityHighlight from '../components/home/CommunityHighlight.astro';
import CTASection from '../components/home/CTASection.astro';
---

<Layout title="Sign Language Tech | Accessible Software by Deaf Engineers">
  <HeroSection />
  <MissionStatement />
  <ValueProposition />
  <ImpactShowcase />
  <CommunityHighlight />
  <CTASection />
</Layout>
```

### Styling Strategy
- **Scoped Styles:** Each component has `<style>` block
- **Global Utilities:** Use existing classes (`.primary-button`, `.mb-2`)
- **Responsive:** Mobile-first approach
- **Dark Mode:** Use existing `@media (prefers-color-scheme: dark)`

### Performance
- **Lazy Loading:** Images below fold
- **WebP Format:** All images
- **Minimal JS:** Astro static generation
- **CSS:** Scoped, no duplication

---

## 10. Implementation Phases

### Phase 1: Foundation (Week 1)
- [ ] Archive old components (move to `/archive`)
- [ ] Create component file structure
- [ ] Set up base styling framework
- [ ] Gather/optimize image assets

### Phase 2: Core Components (Week 2)
- [ ] Build HeroSection.astro
- [ ] Build MissionStatement.astro
- [ ] Build ValueProposition.astro
- [ ] Test responsive behavior

### Phase 3: Dynamic Components (Week 3)
- [ ] Build ImpactShowcase.astro
- [ ] Build CommunityHighlight.astro (with dynamic blog data)
- [ ] Build CTASection.astro
- [ ] Integrate BookAppointmentButton

### Phase 4: Polish & QA (Week 4)
- [ ] Cross-browser testing
- [ ] Accessibility audit (WCAG 2.1 AA)
- [ ] Performance optimization
- [ ] SEO verification
- [ ] Dark mode refinement

### Phase 5: Launch
- [ ] Stakeholder review
- [ ] Final content approval
- [ ] Deploy to production
- [ ] Monitor analytics

---

## 11. Success Metrics

### Primary KPIs
1. **Conversion Rate:**
   - Consultation bookings (via Cal.com)
   - Target: 3-5% of visitors

2. **Engagement:**
   - Time on page: >90 seconds
   - Scroll depth: 75%+ reach CTA

3. **Navigation:**
   - Click-through to `/about`: 15-20%
   - Click-through to `/projects`: 20-25%
   - Click-through to `/blog`: 10-15%

### Secondary Metrics
- Bounce rate: <40%
- Mobile vs. desktop engagement
- Dark mode usage percentage
- Geographic distribution (CNCF events)

### Analytics Setup
- Google Analytics 4 (if not already)
- Event tracking: CTA clicks, section views
- Heatmaps (Hotjar/similar): User behavior
- A/B testing framework (future iterations)

---

## 12. Content Differentiation Matrix

**Ensures no duplication with existing pages:**

| Content Type | Homepage | About Page | Projects Page | Blog |
|-------------|----------|------------|---------------|------|
| **Founder Story** | Brief hook ("We are Deaf engineers") | Full narrative, values, team | Not applicable | Historical posts |
| **Mission** | Condensed (2 paragraphs) | Detailed mission, vision, values | Not applicable | Occasional references |
| **Projects** | 1 featured (Sign Tours) | Not applicable | All projects with full details | Individual post-mortems |
| **Technical Skills** | Implied (cloud-native mention) | Overview of capabilities | Demonstrated per project | Deep dives on specific topics |
| **Community Work** | 3 curated blog posts | Mention of community values | Open-source projects only | All content chronologically |
| **Call to Action** | Final section (consultation) | Contact info | Project inquiry | Subscribe, read more |

**Key Principle:** Homepage is the "appetizer plate" - samples that drive visitors to main courses (About, Projects, Blog).

---

## 13. Accessibility Checklist

Must meet **WCAG 2.1 Level AA** at minimum:

### Visual
- [ ] Color contrast ratio ≥4.5:1 (body text)
- [ ] Color contrast ratio ≥3:1 (large text, UI)
- [ ] No information conveyed by color alone
- [ ] Text resizable to 200% without loss of content
- [ ] No horizontal scrolling at 320px width

### Semantic
- [ ] Proper heading hierarchy (H1 → H2 → H3)
- [ ] Meaningful link text ("Read more about KubeCon" not "Click here")
- [ ] Alt text for all images
- [ ] ARIA labels where needed
- [ ] Landmark roles (`<main>`, `<nav>`, `<section>`)

### Interactive
- [ ] Keyboard navigation (Tab order logical)
- [ ] Focus indicators visible
- [ ] Skip to main content link
- [ ] No keyboard traps
- [ ] Buttons vs. links used correctly

### Forms (CTA)
- [ ] Labels associated with inputs
- [ ] Error messages descriptive
- [ ] Required fields indicated

### Testing Tools
- axe DevTools
- WAVE browser extension
- Lighthouse accessibility audit
- Screen reader testing (NVDA/JAWS)

---

## 14. Migration Strategy

### Before Launch
1. **Backup Current:** Git branch `homepage-v1`
2. **Staging Environment:** Test on `dev.signlanguagetech.com`
3. **User Testing:** 5-10 community members
4. **Stakeholder Sign-off:** Founders approve

### During Launch
1. **Deploy Outside Peak:** Low-traffic window
2. **Monitor Errors:** Real-time error tracking
3. **Quick Rollback Plan:** Revert script ready

### After Launch
1. **Week 1:** Daily monitoring (traffic, conversions, errors)
2. **Week 2-4:** A/B test variations
3. **Month 2:** Iterate based on data
4. **Quarterly:** Major content refresh

---

## 15. Future Enhancements (Post-Launch)

### Version 1.1
- [ ] Animated hero (subtle motion)
- [ ] Interactive stats counter (projects delivered, etc.)
- [ ] Video testimonials (sign language)
- [ ] Live chat integration

### Version 1.2
- [ ] Personalization (returning visitors)
- [ ] A/B tested headlines
- [ ] Multi-language support (Spanish)
- [ ] Progressive Web App features

### Version 2.0
- [ ] Interactive portfolio showcase
- [ ] Client success dashboard
- [ ] Community forum integration
- [ ] Advanced analytics/attribution

---

## 16. Dependencies & Resources

### Team
- **Content:** Marketing lead + founders (approval)
- **Design:** UX/UI designer (icons, imagery)
- **Development:** 1 frontend engineer
- **QA:** Accessibility specialist

### Timeline
- **Design Phase:** 1 week
- **Development:** 3 weeks
- **QA/Testing:** 1 week
- **Total:** 5 weeks

### Budget Estimate
- Design assets (icons, photos): $500-1000
- Development: 80-100 hours
- QA/Testing: 20 hours
- Hosting/tooling: Existing infrastructure

---

## 17. Risk Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| Content approval delays | Timeline slip | Schedule early review checkpoints |
| Image assets not ready | Visual impact reduced | Use existing assets, optimize later |
| Accessibility issues post-launch | Legal/brand risk | Pre-launch audit mandatory |
| Performance regression | SEO/UX degradation | Lighthouse CI in deployment pipeline |
| Dark mode inconsistencies | UX fragmentation | Dedicated dark mode testing phase |

---

## Conclusion

This redesign transforms the homepage from a generic services site to a **powerful statement of identity and capability**. By leading with the founders' unique story, we create immediate differentiation. By showcasing real impact (Sign Tours Hungary), we build credibility. By maintaining accessibility as a core value throughout, we walk the talk.

**Next Step:** Proceed to Phase 1 implementation upon approval.
