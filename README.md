# Easy Rx Landing Page

## Project Overview

As the lead developer, I built a fully bilingual, mobile-responsive landing page for Easy Rx, a clinical decision-support app for BMDC-registered medical practitioners. The goal was to create a high-converting page that would communicate the product’s value, drive WhatsApp-based free trial sign-ups, and project a professional, trustworthy, modern brand tone.

The client presented a detailed structure with 10 content sections, specific copy, and placeholder requirements. The initial build was a single-language English page. The client then requested a Bangla version with a live language toggle, followed by a request to enhance the page with scroll and hover animations to improve engagement and perceived quality.

Below is a breakdown of the requirements and exactly what was delivered.

## Client Requirements (Phased)

### Phase 1 – Core Landing Page (English)
- A single-page, mobile-responsive layout.
- Sections: Hero, Daily Challenges, Why Easy Rx, Core Features, Specialty Coverage, Dermatology Highlight, Pediatric Dose Highlight, Digital Prescription, Testimonials, FAQ, and Final CTA.
- Placeholder images for app mockups, screenshots, and review avatars (all to be stored in a `src` folder).
- Two primary call-to-action buttons: “Get 1 Day Free Full Access” and “Message on WhatsApp.”
- Professional medical aesthetic with trust-building elements.

### Phase 2 – Bangla Translation & Language Toggle
- Translate all visible text into Bangla (Bengali) while preserving the exact same structure and placeholders.
- Add a toggle button (`EN | বাংলা`) at the top of the page to switch languages seamlessly.
- The toggle must remember the user's preference using `localStorage`.

### Phase 3 – Animated Interactions
- Animate elements when they scroll into view (fade, slide, scale).
- Add hover effects to cards, buttons, images, and the sticky header.
- Smooth transitions that feel modern without impacting performance.

## What I Delivered

1. **Fully Responsive, Single-Page HTML/CSS/JS Application**
   - No external frameworks (other than Font Awesome for icons). The entire page is self-contained.
   - Responsive breakpoints ensure optimal display on mobile, tablet, and desktop.
   - A sticky header with a WhatsApp CTA and language switcher for persistent accessibility.

2. **Complete Bilingual Implementation**
   - Every user-facing string exists in both English and Bangla.
   - The language toggle uses a clean button design (`EN | বাংলা`) and switches the UI instantly by toggling a CSS class on the `<body>`.
   - The selected language is saved to `localStorage`, so returning visitors see their preferred version automatically.
   - Block and inline elements are correctly handled so that Bangla text displays naturally without layout breaks.

3. **Scroll and Hover Animations**
   - **Scroll-triggered reveals:** Using the Intersection Observer API, elements gain a `visible` class when 15% of them enters the viewport. This triggers:
     - Vertical slide+fade (`.reveal`)
     - Left/right slide+fade (`.reveal-left`, `.reveal-right`)
     - Gentle scale‑up (`.reveal-scale`)
     - Staggered delays (`.delay-100` to `.delay-400`) for card grids and testimonial items.
   - **Hover interactions:**
     - Buttons: Lift, shadow expansion, and a shimmer effect (`::after` pseudo-element).
     - Feature cards: Lift, border color change, icon scale.
     - Specialty items: Background color invert, translate.
     - Testimonial cards: Lift and border highlight.
     - FAQ items: Background highlight and question color change.
     - Hero mockup: 3D hover lift.
     - Screenshot images: Scale on hover.
     - Final CTA box: Soft lift and shadow.
   - **Sticky header:** Shrinks its padding and increases background opacity on scroll.

4. **Functional Elements**
   - FAQ accordions with smooth expand/collapse.
   - All WhatsApp links are pre-filled with relevant messages and point to the specified number.
   - The page loads with the user's saved language preference, defaulting to English.

5. **Placeholder Image System**
   - App mockups, dermatology images, prescription screenshots, and avatar images are all referenced from the `src/` folder.
   - The client simply needs to drop their assets into that directory with the expected filenames (e.g., `easy-rx-mockup.png`, `screenshot-1.png`, etc.).
   - Placeholder styles (background color, minimum height) ensure the layout remains intact even before real images are uploaded.

## Technologies Used

- **HTML5** – Semantic, accessible markup.
- **CSS3** – Custom properties, flexbox/grid, transitions, gradients, hover/active states.
- **JavaScript (Vanilla)** – Intersection Observer for scroll animations, dynamic class toggling for language switching, `localStorage`, and FAQ accordion logic.
- **Font Awesome 6** – Lightweight vector icons.
- **No libraries or frameworks** – The page is dependency-free, making it fast and easy to deploy.

## How the Client Can Use & Customize

1. **Hosting:** Upload the single HTML file and the `src/` folder to any static hosting.
2. **Replace Placeholders:** Add their own app mockups, screenshots, and testimonial photos inside the `src/` folder.
3. **Update WhatsApp Number:** Change the number in the `wa.me` links if needed (search for `01571-760136`).
4. **Edit Copy:** All text is directly inside the HTML; the dual‑language system uses `<span class="lang-en">` and `<span class="lang-bn">` pairs. The developer can easily add or modify any section while keeping both languages in sync.

---

The final deliverable is a polished, production-ready landing page that fulfills all three phases of the client’s request – structure, bilingual support, and animated engagement – while maintaining a professional, trustworthy brand voice.
