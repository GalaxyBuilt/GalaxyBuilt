# Galaxy Built Portfolio Implementation Plan

We will create a high-performance, aesthetically pleasing developer portfolio for "Galaxy Built". 

## Framework Choice: Astro
I recommend **Astro** for this project. 
- **Speed & Lightness**: Astro is designed for content-heavy sites and ships zero JavaScript by default, making it incredibly fast.
- **Familiarity**: You mentioned you are very familiar with it, which will make maintenance easy for you.
- **Modern Features**: We can still use React components if we need interactivity later.

## User Review Required
> [!IMPORTANT]
> Please confirm if you'd like to proceed with Astro. I will start the initialization based on this recommendation.

> [!NOTE]
> I will initialize the GitHub repository as requested: `https://github.com/GalaxyBuilt/GalaxyBuilt`.

## Proposed Changes

### [Component Name]
#### [NEW] [index.astro](file:///c:/Users/NefuTrades/galaxybuilt/src/pages/index.astro)
- Main landing page featuring all project sections.
#### [NEW] [ProjectCard.astro](file:///c:/Users/NefuTrades/galaxybuilt/src/components/ProjectCard.astro)
- Reusable component for showcasing projects with descriptions and links.
### Light Mode & Visibility
- **[MODIFY] [Layout.astro](file:///c:/Users/NefuTrades/galaxybuilt/src/layouts/Layout.astro)**
    - Update nav links to use `text-slate-500 hover:text-black dark:text-slate-400 dark:hover:text-white`.
    - Update logo text to use `text-slate-900 dark:text-white`.
    - Fix footer links and attribution for theme compatibility.
    - Add "AI" link to main navigation.

### AI Agents Section
- **[MODIFY] [index.astro](file:///c:/Users/NefuTrades/galaxybuilt/src/pages/index.astro)**
    - Create `aiProjects` array and move `Txchya` into it.
    - Implement "AI Agents" section above the SaaS platforms section.
    - Update page scroll logic for the new section.


### Project Card Visuals & Content
- **[MODIFY] [ProjectCard.astro](file:///c:/Users/NefuTrades/galaxybuilt/src/components/ProjectCard.astro)**
    - Add `image` prop to the interface.
    - Implement a hero image section with aspect-ratio and lazy loading.
    - Add simple markdown-to-html parsing for the `details` modal to handle `###` and `####` headers.
    - Ensure images have a subtle hover scale effect.

- **[MODIFY] [index.astro](file:///c:/Users/NefuTrades/galaxybuilt/src/pages/index.astro)**
    - Add `image` paths to all project objects in `aiProjects`, `saasProjects`, `megablogProjects`, `tradingProjects`, and `softwareProjects`.
    - Assets will be generated and stored in `/public/images/projects/`.

### Assets Generation
- Generate high-fidelity hero images for:
    - Txchya (Futuristic AI Construct)
    - EverRank (Digital SEO Architecture)
    - FastAIFlow (Connected AI Nodes)
    - Project Genesis (Bitcoin / Institutional)
    ... and others.

## Verification Plan
### Automated Tests
- Run `npm run build` to ensure the project compiles correctly.
- Use `astro check` for type-checking.
### Manual Verification
- Toggle light/dark mode and verify header text is legible.
- Confirm "AI Agents" section appears correctly above "SaaS Platforms".
- Test the "AI" nav link.
- Use Browser tools to verify GA tag is firing.
- Verify responsiveness on mobile and desktop.
- Check all links to external projects.
- Verify GitHub initialization and first push.
