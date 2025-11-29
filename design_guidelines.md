# Design Guidelines: Multilingual Biological Knowledge & Health Platform

## Design Approach: Material Design System
Selected for content-rich health applications requiring strong information hierarchy, trustworthy presentation, and extensive data organization. Drawing inspiration from WebMD, Healthline, and Mayo Clinic for medical content credibility while maintaining modern visual appeal.

## Core Design Principles
1. **Trust & Credibility**: Clean, professional layouts that inspire confidence in medical information
2. **Information Density**: Efficient display of extensive health data without overwhelming users
3. **Accessibility First**: Clear typography and navigation for diverse global audience
4. **Progressive Disclosure**: Hierarchical content reveal from overview to detailed solutions

## Typography System
- **Primary Font**: Roboto (Google Fonts) - excellent multilingual support for 150+ languages
- **Secondary Font**: Merrifield or Lora for body content - improved readability for long-form health articles
- **Hierarchy**:
  - H1: text-4xl md:text-5xl font-bold (page titles, body system names)
  - H2: text-3xl md:text-4xl font-semibold (section headers, problem categories)
  - H3: text-2xl font-semibold (individual problems, subsections)
  - H4: text-xl font-medium (solution steps, criteria)
  - Body: text-base leading-relaxed (medical content, descriptions)
  - Small: text-sm (metadata, disclaimers)

## Layout System
**Spacing Units**: Consistent use of Tailwind units 4, 6, 8, 12, 16, 24 for predictable rhythm
- Section padding: py-16 md:py-24
- Card spacing: p-6 md:p-8
- Component gaps: gap-4 to gap-8
- Container max-width: max-w-7xl with px-4 md:px-6

## Component Library

### Navigation
- **Sticky Header**: Fixed top navigation with language selector (dropdown with 150+ options, Uzbek as default), search bar, and main menu
- **Mega Menu**: Dropdown showing all 30 body systems organized in 6-column grid on desktop, accordion on mobile
- **Breadcrumbs**: Always visible for deep navigation (Body System → Problem Category → Specific Problem → Solution)

### Hero Section
**Full-width Hero** (h-96 md:h-[500px]) with:
- Medical/scientific imagery (abstract cellular structures, human anatomy illustrations)
- Centered content overlay with blurred background buttons
- H1 headline, descriptive subtitle, dual CTAs (Browse Body Systems + Search Problems)
- Language switcher prominently displayed

### Body System Cards (Homepage)
**Grid Layout**: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6
- Each card: Rounded corners (rounded-xl), shadow (shadow-lg), hover elevation
- Icon/illustration at top (use Material Icons for body systems)
- System name (H3)
- Problem count badge ("100+ conditions")
- Quick access link

### Problem Categories Layout
**Two-Column Split** (lg:grid-cols-3):
- Left sidebar (sticky): Category navigation for 100+ problems, filterable
- Main content: Problem cards in grid, each showing: title, severity indicator, solution preview, "Learn More" CTA

### Solution Pages
**Single Column** max-w-4xl:
- Problem title (H1) with severity badge
- Quick summary card (elevated, distinct background)
- Tabbed sections: Overview, Causes, Symptoms, Solutions, Prevention
- Solution steps as numbered cards or accordion items
- Related problems sidebar (3-4 suggestions)

### Special Focus Sections (Overweight, Depression, Stress)
**Featured prominently** on homepage:
- Dedicated horizontal cards with imagery
- Direct access CTAs
- Curated solution pathways
- Progress tracking suggestions

### Search & Filter System
- **Global search**: Full-text search across all 3000+ problems (30 systems × 100 problems)
- **Filter panel**: By body system, severity, type (acute/chronic), solution type
- **Results grid**: Preview cards with highlighting matched terms

### Footer
**Four-Column Layout** (md:grid-cols-4):
- Body systems quick links (organized by category)
- About, disclaimer, medical advisory
- Language resources
- Social proof (users served, problems documented)
- Medical disclaimer text (required for health content)

## Responsive Behavior
- Mobile (< 768px): Single column, collapsible navigation, stacked cards
- Tablet (768-1024px): Two-column grids, visible categories
- Desktop (> 1024px): Full multi-column layouts, persistent sidebars

## Animations
**Minimal & Purposeful**:
- Card hover: subtle lift (translate-y-1)
- Page transitions: fade-in content
- Accordion expand/collapse: smooth height transitions
- NO scroll-triggered animations to maintain focus on medical content

## Icons
**Material Icons** (via CDN) for:
- Body system representations (heart, brain, lungs icons)
- UI actions (search, language, menu)
- Severity indicators (info, warning, critical)

## Images
**Hero Image**: Abstract medical/scientific visualization (DNA helix, cellular structures, or anatomical illustration) - sophisticated, professional
**Body System Cards**: Optional illustrative icons or simple medical diagrams
**Solution Pages**: Relevant diagrams explaining conditions (use placeholder comments for custom medical illustrations)

## Critical UX Patterns
- **Language persistence**: Remember user's language choice across sessions
- **Reading progress**: Indicate progress through long solution articles
- **Print-friendly**: Solutions formatted for printing/saving
- **Share functionality**: Individual problems shareable via link
- **Medical disclaimer**: Visible on every solution page

This design balances extensive information architecture with approachable, modern aesthetics suitable for a global health education platform.