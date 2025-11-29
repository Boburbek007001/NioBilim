# BioHealth - Multilingual Biological Knowledge Platform

## Project Overview
A comprehensive biological knowledge and health guidance website with multilingual support, featuring 30 body systems and health problems with evidence-based solutions. Built with React, Express, TypeScript, and i18next for internationalization.

## Key Features Implemented
✅ **Multilingual Support**: 
- Infrastructure for 150+ languages with i18next
- Full translations for: Uzbek (default), English, Russian
- Partial translations for: Arabic, Chinese, Spanish, French, German, Hindi, Portuguese, Turkish
- English fallback system for all other languages
- Language switcher in header with persistent selection (localStorage)

✅ **30 Body Systems**:
All major body systems implemented with multilingual names and descriptions:
- Cardiovascular, Nervous, Respiratory, Digestive, Endocrine, Skeletal, Muscular
- Urinary, Reproductive, Immune, Integumentary, Lymphatic, Visual, Auditory
- Olfactory, Gustatory, Vestibular, Circulatory, Hepatic, Pancreatic, Renal
- Hematopoietic, Thermoregulatory, Metabolic, Hormonal, Excretory
- Psychological, Nutritional, Sleep, Cognitive

✅ **Featured Health Topics**:
- **Overweight & Obesity**: Comprehensive guidance with causes, symptoms, solutions, and prevention
- **Depression**: Complete mental health resource with professional treatment recommendations
- **Chronic Stress**: Detailed stress management strategies and solutions

✅ **Additional Health Problems**:
- Hypertension, Arrhythmia (Cardiovascular)
- Anxiety, Insomnia (Nervous/Sleep)
- Gastritis, IBS (Digestive)
- Related problems interconnected for easy navigation

✅ **Beautiful UI Design**:
- Medical-themed color palette with green primary color
- Roboto and Lora fonts for professional medical appearance
- Responsive design (mobile, tablet, desktop)
- Dark mode support with theme toggle
- Smooth animations and transitions
- Hero section with medical DNA imagery
- Card-based layouts for systems and problems

✅ **Search Functionality**:
- Full-text search across all problems
- Dedicated search results page
- Real-time filtering by severity level
- Empty states and loading skeletons

✅ **Navigation & Routing**:
- Home page with hero, featured topics, and body systems grid
- System details pages with filterable problem lists
- Problem details pages with tabbed content (overview, causes, symptoms, solutions, prevention)
- Search results page
- Proper SPA navigation with Wouter
- Medical disclaimer on all pages

## Technology Stack
- **Frontend**: React 18, TypeScript, Wouter (routing), TanStack Query, i18next
- **UI Components**: Shadcn UI (Radix UI primitives), Tailwind CSS
- **Backend**: Express.js, TypeScript
- **Data Storage**: In-memory storage (MemStorage)
- **Build Tool**: Vite
- **Theme**: Custom medical theme with dark mode support

## Architecture
- **Schema-First Development**: Shared TypeScript types between frontend and backend
- **Component-Based**: Reusable UI components following Shadcn patterns
- **API Routes**: RESTful endpoints for all data access
- **i18n Structure**: Centralized translation management with fallback system

## Development Status
**Current Sprint**: MVP Complete
- ✅ All core features implemented
- ✅ Search functionality working
- ✅ Multilingual support infrastructure ready
- ✅ Responsive design complete
- ✅ Dark mode implemented

**Future Enhancements**:
- Expand translations for all 150+ languages (currently using English fallback)
- Add more health problems per system (target: 100+ per system)
- Integrate OpenAI API for personalized health advice chatbot
- Add user accounts for saving favorite articles
- Implement symptom checker tool
- Add community forum
- Include multimedia content (diagrams, videos, 3D models)

## Key Files
- `client/src/App.tsx` - Main app component with routing
- `client/src/pages/home.tsx` - Homepage with hero, featured topics, systems grid
- `client/src/pages/system-details.tsx` - System detail view with problem list
- `client/src/pages/problem-details.tsx` - Problem detail view with tabbed content
- `client/src/pages/search.tsx` - Search results page
- `client/src/lib/i18n.ts` - i18next configuration with 150+ language codes
- `client/src/components/header.tsx` - Header with language switcher and theme toggle
- `server/storage.ts` - In-memory database with all biological knowledge data
- `server/routes.ts` - API endpoints for systems, problems, search
- `shared/schema.ts` - TypeScript interfaces for data models

## Running the Project
The application runs on port 5000 with the "Start application" workflow which executes `npm run dev`.

## Notes
- The platform currently focuses on Uzbek, English, and Russian languages with full content translations
- Medical content is educational only - users are advised to consult healthcare providers
- The design follows a medical/healthcare aesthetic with professional color scheme
- All interactive elements include `data-testid` attributes for testing
