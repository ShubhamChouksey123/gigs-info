# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a **Fiverr gig marketing repository** containing professionally crafted gig descriptions, HTML-based image templates, and portfolio documentation for freelance software development services. The repository does NOT contain application code—it's a collection of marketing materials, gig descriptions, and visual assets.

## Repository Structure

```
gigs-info/
├── full-stack-gig/           # Full-stack Java Spring Boot development gig
│   ├── full-stack-java-gig.md
│   ├── gig-update.md
│   └── images-html/          # HTML templates for gig images (1280x752px)
├── rest-api/                 # REST API development gig (Spring Boot)
│   ├── java-springboot-api-fiverr-gig.md
│   ├── GIGS-IMAGES-SUMMARY.md
│   └── images-html/          # HTML templates for gig images
├── restaurant-menu/          # Restaurant digital menu management gig
│   ├── restaurant_menu.md
│   ├── restaurant-digital-menu.md
│   └── images-html/          # HTML templates for gig images
├── fiverr-gig-template.md    # Master template for creating new Fiverr gigs
├── README.md                 # Comprehensive documentation
└── .claude/
    └── agents/
        └── portfolio-project-architect.md  # Custom agent for portfolio work
```

## Key Concepts

### 1. Gig Structure
Each gig directory contains:
- **Main gig file** (`*-gig.md`): Complete Fiverr gig description following the 6-step Fiverr form structure
- **Portfolio version** (`restaurant_menu.md`, etc.): Portfolio-optimized project descriptions with business value focus
- **images-html/** directory: HTML files designed to generate professional gig images at exactly 1280x752px

### 2. HTML-Based Image Generation
The `images-html/` directories contain standalone HTML files that serve as visual templates for Fiverr gig images:
- **Fixed dimensions**: Always 1280px × 752px (Fiverr's optimal aspect ratio)
- **Self-contained**: All CSS is inline; no external dependencies
- **Workflow**: Open in browser → Take screenshot → Upload to Fiverr
- **Design principles**: Fixed height (`height: 752px`), flexbox layouts, progressive content reduction strategy

### 3. Two Documentation Approaches

**Fiverr Gig Format** (e.g., `full-stack-java-gig.md`):
- Follows Fiverr's 6-step creation form
- Includes: Overview, Pricing, Description & FAQ, Requirements, Gallery, Publish
- Character limits enforced (title: 80 chars, description: 1200 chars)
- Focused on selling services to Fiverr buyers

**Portfolio Format** (e.g., `restaurant_menu.md`):
- Business value and impact-first approach
- Complete technology stack explicitly listed
- SEO-optimized with 10-15 technical keywords
- Target: ~1300 characters with catchy closing statement
- Quantifiable metrics (cost savings %, time reduction, etc.)

### 4. Custom Portfolio Architect Agent
The `.claude/agents/portfolio-project-architect.md` agent is specialized for:
- Converting technical projects into professional portfolio presentations
- Filling portfolio submission forms with strategic content
- SEO optimization with natural keyword integration
- Business value extraction and quantification

## Common Commands

### Opening HTML Image Templates
```bash
# Open all gig images for a specific gig in browser
open full-stack-gig/images-html/*.html
open rest-api/images-html/*.html
open restaurant-menu/images-html/*.html

# Open specific image template
open restaurant-menu/images-html/fiverr-gig-cover.html
```

### Viewing Gig Documentation
```bash
# View main gig descriptions
open full-stack-gig/full-stack-java-gig.md
open rest-api/java-springboot-api-fiverr-gig.md
open restaurant-menu/restaurant-digital-menu.md

# View portfolio versions
open restaurant-menu/restaurant_menu.md
```

### Working with Templates
```bash
# View the master Fiverr gig template
open fiverr-gig-template.md

# View comprehensive repository documentation
open README.md
```

## Content Guidelines

### When Creating/Editing Gig Descriptions
1. **Character limits are critical**:
   - Gig title: 80 characters
   - Package descriptions: 100 characters
   - Main description: 1200 characters
   - Search tags: 5 tags only

2. **Fiverr's 6-step structure**:
   - Step 1: Overview (title, category, metadata, tags)
   - Step 2: Pricing (Basic/Standard/Premium packages)
   - Step 3: Description & FAQ
   - Step 4: Requirements (buyer questions)
   - Step 5: Gallery (images, video, documents)
   - Step 6: Publish

3. **Key differentiators**:
   - Live demo URL: http://161.118.188.237:8080 (Quiz platform on OCI)
   - Technology stack emphasis (Spring Boot 3.x, Java 21, React 18)
   - Enterprise-grade quality positioning
   - 30-day support period

### When Creating/Editing HTML Image Templates
1. **ALWAYS use fixed dimensions**:
   ```css
   .card {
       width: 1280px;
       height: 752px;  /* NEVER use "auto" */
       overflow: hidden;
   }
   ```

2. **Progressive reduction strategy** (if content doesn't fit):
   - First reduce: padding/margins (40px → 30px → 25px → 20px)
   - Then reduce: gaps between elements (30px → 25px → 20px)
   - Then reduce: font sizes (32px → 28px → 24px)
   - Last resort: remove content

3. **Layout structure**:
   ```css
   .card { display: flex; flex-direction: column; }
   .header { /* fixed height */ }
   .main-content { flex: 1; /* fills available space */ }
   .footer { /* fixed height */ }
   ```

4. **Testing checklist**:
   - Open HTML in browser
   - Inspect computed dimensions (should be exactly 1280×752)
   - Verify no scrolling needed
   - Take screenshot at 100% zoom
   - Verify file size < 5MB

### When Creating Portfolio Documentation
1. **Business value first**: Lead with quantifiable impact (cost savings %, time reduction, users served)
2. **Complete tech stack**: Explicitly list all technologies with version numbers (Java 21, Spring Boot 3.2, React 18)
3. **SEO optimization**: Naturally incorporate 10-15 technical keywords
4. **Target 1300 characters**: Leave room for impactful closing statement
5. **Catchy closing**: End with memorable, professional tagline that captures transformation
6. **Structure**: Context & Business Value → Solution & Tech Stack → Results & Impact → Catchy Closing

## Important References

### Live Portfolio Demo
- **URL**: http://161.118.188.237:8080
- **Description**: Production Spring Boot quiz platform with authentication, email verification, admin panel, 1000+ questions
- **Deployment**: Oracle Cloud Infrastructure (OCI)

### Target Services
1. **Full-stack Java Development**: Spring Boot 3, PostgreSQL, authentication, admin panels
2. **REST API Development**: Secure APIs, Spring Security, JWT, database integration
3. **Restaurant Digital Menu**: QR code systems, contactless menus, admin dashboards

### Pricing Reference
- **Basic**: $200-250 (5-7 days, simple CRUD, 5 pages)
- **Standard**: $500-600 (14 days, full-featured with auth, admin panel)
- **Premium**: $1000+ (21 days, enterprise with payments, SMS, CI/CD)

## HTML Image Design Principles

### Color Scheme
- **Primary**: Deep blues (#1a237e, #283593) for headers
- **Accent**: Green (#4CAF50, #27c93f) for highlights
- **Background**: Light grays (#f8f9fa, #e9ecef) for cards
- **Text**: Dark gray (#333) on light backgrounds

### Typography Guidelines
- **H1 (Main title)**: 28-36px
- **H2 (Section headers)**: 20-26px
- **Card titles**: 16-20px
- **Body text**: 14-16px
- **Icons**: 32-48px (headers), 28-36px (cards)

### Common Issues & Solutions
- **Content overflows**: Reduce main-content padding and gap
- **Cards look cramped**: Reduce items or use smaller fonts
- **Text wrapping**: Reduce font size or shorten content
- **Misalignment**: Use `flex: 1` on middle section, fixed padding on header/footer

## SEO Keywords by Gig Type

### Full-Stack Development
spring-boot, java-development, full-stack-developer, postgresql, web-application, authentication, rest-api, hibernate, maven, docker-deployment

### REST API Development
rest-api, spring-boot, java, api-development, microservices, spring-security, jwt-authentication, postgresql, api-documentation, backend-development

### Restaurant Menu
restaurant-menu, digital-menu, qr-code, contactless-menu, spring-boot, react-admin, food-service, menu-management, restaurant-technology

## Notes for Future Work

- All HTML image templates are self-contained with inline CSS
- README.md contains extensive best practices for HTML image creation (lines 76-230)
- The fiverr-gig-template.md is the master template—always reference it when creating new gigs
- Portfolio descriptions should follow the structure in portfolio-project-architect.md
- Git status shows modified fiverr-gig-template.md and untracked GIGS-IMAGES-SUMMARY.md in rest-api/
