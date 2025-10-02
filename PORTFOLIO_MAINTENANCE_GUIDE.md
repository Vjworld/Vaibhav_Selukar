# Portfolio Website Maintenance Guide

## 📚 Table of Contents
1. [Introduction](#introduction)
2. [File Structure](#file-structure)
3. [How to Edit Content](#how-to-edit-content)
4. [Adding New Sections](#adding-new-sections)
5. [Updating Existing Sections](#updating-existing-sections)
6. [Managing Vibe Coding Projects](#managing-vibe-coding-projects)
7. [Managing Affiliate Links](#managing-affiliate-links)
8. [Managing Social Media Links](#managing-social-media-links)
9. [Managing Certifications](#managing-certifications)
10. [Deleting Sections](#deleting-sections)
11. [Color Customization](#color-customization)
12. [Mobile Responsiveness](#mobile-responsiveness)
13. [Troubleshooting](#troubleshooting)

---

## Introduction

This guide will help you maintain and update your portfolio website without needing extensive technical knowledge. The website is built as a **single HTML file** (`index.html`) with inline CSS styles and JavaScript functionality.

**Key Features:**
- ✅ Single file - easy to manage and deploy
- ✅ No external dependencies
- ✅ GitHub Pages ready
- ✅ Mobile responsive
- ✅ Smooth animations and interactions

---

## File Structure

```
portfolio/
├── index.html                          # Main portfolio file (ALL content here)
├── PORTFOLIO_MAINTENANCE_GUIDE.md      # This guide
└── attached_assets/                    # Resume PDFs and reference images
```

**Everything is in `index.html`** - all HTML content, CSS styling, and JavaScript functionality!

---

## How to Edit Content

### Step 1: Open the File
- Open `index.html` in any text editor (VS Code, Notepad++, Sublime Text, or even Notepad)
- Press `Ctrl+F` (Windows) or `Cmd+F` (Mac) to search for specific content

### Step 2: Find the Section
- Use the search function to find the text you want to change
- Each section has a clear HTML structure with comments

### Step 3: Make Changes
- Edit the text between HTML tags
- Save the file (`Ctrl+S` or `Cmd+S`)
- Refresh your browser to see changes

---

## Adding New Sections

### Example: Adding a "Testimonials" Section

**Step 1: Choose Location**
Decide where to place the new section. Typically, add it before the Contact section.

**Step 2: Find the Contact Section**
Search for: `<section id="contact"`

**Step 3: Add New Section Before It**
Insert this template BEFORE the contact section:

```html
<section id="testimonials" class="compact">
    <div class="section-content">
        <h2 class="section-title" data-number="09.">Testimonials</h2>
        <div class="projects-grid">
            <div class="project-card fade-in">
                <div class="project-content">
                    <h3 class="project-title">Client Name</h3>
                    <p class="project-description">
                        "Testimonial text goes here..."
                    </p>
                </div>
            </div>
            <!-- Add more testimonial cards here -->
        </div>
    </div>
</section>
```

**Step 4: Update Navigation**
Find the navigation menu: `<ul class="nav-links"`

Add a new navigation link:
```html
<li><a href="#testimonials"><span>09.</span>Testimonials</a></li>
```

**Step 5: Update Section Numbers**
Update the `data-number` attribute for all sections after the new one (increment by 1).

---

## Updating Existing Sections

### Updating the Hero Section

**What to Update:**
- Name
- Title/Subtitle
- Description
- Badges

**How to Find It:**
Search for: `<section id="hero">`

**Example - Changing Your Title:**
```html
<!-- FIND THIS: -->
<h2 class="hero-subtitle">Certified Scrum Master & Agile Consultant</h2>

<!-- CHANGE TO: -->
<h2 class="hero-subtitle">Your New Title Here</h2>
```

**Example - Adding a Badge:**
```html
<!-- FIND THE BADGES SECTION: -->
<div class="hero-badges">
    <span class="badge">PSM Certified</span>
    <span class="badge">PMP Certified</span>
    <span class="badge">6+ Years Experience</span>
    <span class="badge">AI Automation</span>
</div>

<!-- ADD A NEW BADGE: -->
<div class="hero-badges">
    <span class="badge">PSM Certified</span>
    <span class="badge">PMP Certified</span>
    <span class="badge">6+ Years Experience</span>
    <span class="badge">AI Automation</span>
    <span class="badge">New Badge Text</span> <!-- NEW BADGE -->
</div>
```

### Updating the About Section

Search for: `<section id="about">`

**Change Text:**
Find the paragraph you want to edit and update the text between `<p>` and `</p>` tags.

**Update Stats:**
```html
<!-- FIND THIS: -->
<div class="stat-card">
    <div class="stat-number">6+</div>
    <div class="stat-label">Years Experience</div>
</div>

<!-- CHANGE THE NUMBER AND LABEL: -->
<div class="stat-card">
    <div class="stat-number">10+</div>
    <div class="stat-label">Years Experience</div>
</div>
```

### Updating Skills Section

Search for: `<section id="skills">`

**Adding a New Skill:**
```html
<!-- FIND A SKILL CATEGORY: -->
<div class="skill-category fade-in">
    <h3>🎯 Agile Facilitation</h3>
    <ul class="skill-list">
        <li>Remote Scrum Ceremonies</li>
        <li>Sprint Planning & Retrospectives</li>
        <!-- ADD NEW SKILL HERE: -->
        <li>Your New Skill Here</li>
    </ul>
</div>
```

**Adding a New Skill Category:**
```html
<!-- ADD THIS AFTER THE LAST SKILL CATEGORY: -->
<div class="skill-category fade-in">
    <h3>🆕 New Category Name</h3>
    <ul class="skill-list">
        <li>Skill 1</li>
        <li>Skill 2</li>
        <li>Skill 3</li>
    </ul>
</div>
```

### Updating Experience Section

Search for: `<section id="experience">`

**Adding a New Job:**
```html
<!-- ADD THIS AFTER THE TIMELINE OPENING TAG: -->
<div class="experience-item fade-in">
    <div class="experience-header">
        <h3 class="experience-title">Job Title</h3>
        <div class="experience-company">Company Name</div>
        <div class="experience-date">Month Year – Month Year | Location</div>
    </div>
    <ul class="experience-description">
        <li>Responsibility 1</li>
        <li>Responsibility 2</li>
        <li>Responsibility 3</li>
    </ul>
</div>
```

**Editing Existing Job:**
- Find the job by searching for the company name
- Update title, dates, or responsibilities as needed

---

## Managing Vibe Coding Projects

### Location
Search for: `<section id="vibe-coding">`

### Adding a New Project

**Step 1: Copy Template**
Copy this template:

```html
<div class="project-card fade-in">
    <div class="project-image">🎨</div> <!-- Change emoji -->
    <div class="project-content">
        <h3 class="project-title">Project Name</h3>
        <p class="project-description">
            Project description goes here. Explain what the project does and what makes it special.
        </p>
        <div class="project-tags">
            <span class="project-tag">Tool Name</span>
            <span class="project-tag">Technology</span>
            <span class="project-tag">Category</span>
        </div>
        <div class="project-links">
            <a href="YOUR_PRODUCT_LINK" target="_blank" rel="noopener noreferrer" class="project-link">View Live</a>
            <a href="YOUR_YOUTUBE_LINK" target="_blank" rel="noopener noreferrer" class="project-link youtube">🎬 Demo</a>
        </div>
    </div>
</div>
```

**Step 2: Customize the Project**
1. **Change the emoji** - Replace `🎨` with an appropriate emoji for your project
2. **Update the title** - Change "Project Name" to your project's name
3. **Write description** - Describe what your project does
4. **Add tags** - Update tags to reflect tools/technologies used
5. **Add links:**
   - Replace `YOUR_PRODUCT_LINK` with your live product URL
   - Replace `YOUR_YOUTUBE_LINK` with your YouTube video URL

**Step 3: Insert Project**
- Find the vibe-coding section
- Paste your new project card inside `<div class="projects-grid">`
- Save and refresh

### Updating an Existing Project

**Changing Product Link:**
```html
<!-- FIND THE PROJECT: -->
<a href="https://old-link.com" target="_blank" rel="noopener noreferrer" class="project-link">View Live</a>

<!-- UPDATE TO: -->
<a href="https://new-link.com" target="_blank" rel="noopener noreferrer" class="project-link">View Live</a>
```

**Changing YouTube Link:**
```html
<!-- FIND THE YOUTUBE LINK: -->
<a href="https://youtube.com/old-video" target="_blank" rel="noopener noreferrer" class="project-link youtube">🎬 Demo</a>

<!-- UPDATE TO: -->
<a href="https://youtube.com/new-video" target="_blank" rel="noopener noreferrer" class="project-link youtube">🎬 Demo</a>
```

### Deleting a Project

1. Find the project you want to delete
2. Look for the opening `<div class="project-card fade-in">` tag
3. Find the matching closing `</div>` tag
4. Delete everything between and including these tags
5. Save the file

---

## Managing Affiliate Links

### Location
Search for: `<section id="affiliates">`

### Adding a New Affiliate Partner

**Template:**
```html
<div class="affiliate-card fade-in">
    <div class="affiliate-icon">🔮</div> <!-- Change emoji -->
    <h3 class="affiliate-title">Tool Name</h3>
    <p class="affiliate-description">
        Description of the tool and why you recommend it. Explain the benefits and features.
    </p>
    <a href="YOUR_AFFILIATE_LINK_HERE" target="_blank" rel="noopener noreferrer" class="affiliate-link">Try Tool Name 🚀</a>
    <div class="affiliate-badge">💰 Earn Commission</div>
</div>
```

**Steps:**
1. Copy the template above
2. Change the **emoji** to represent the tool
3. Update the **tool name**
4. Write a compelling **description**
5. **Replace** `YOUR_AFFILIATE_LINK_HERE` with your actual affiliate link
6. Update the **button text**
7. Paste into the affiliates section

### Updating Affiliate Links

**Important:** When you get a new affiliate link or need to update an existing one:

```html
<!-- FIND THIS: -->
<a href="https://replit.com?ref=oldlink" target="_blank" rel="noopener noreferrer" class="affiliate-link">Try Replit Free 🚀</a>

<!-- UPDATE TO: -->
<a href="https://replit.com?ref=newlink" target="_blank" rel="noopener noreferrer" class="affiliate-link">Try Replit Free 🚀</a>
```

**Key Points:**
- Always include `?ref=yourname` or similar tracking parameter
- Keep `target="_blank"` to open in new tab
- Keep `rel="noopener noreferrer"` for security

### Removing an Affiliate Partner

1. Find the affiliate card to remove
2. Delete from `<div class="affiliate-card fade-in">` to its closing `</div>`
3. Save the file

---

## Managing Social Media Links

### Locations Where Social Links Appear:
1. **Hero Section** - Small icons below CTA buttons
2. **Contact Section** - Large circular icons
3. **Footer** - Text links

### Updating Social Media URLs

**In Hero Section:**
Search for: `<div class="social-links">`

```html
<!-- FIND YOUR PLATFORM: -->
<a href="https://linkedin.com/in/old-username" target="_blank" rel="noopener noreferrer" class="social-link" title="LinkedIn">💼</a>

<!-- UPDATE URL: -->
<a href="https://linkedin.com/in/new-username" target="_blank" rel="noopener noreferrer" class="social-link" title="LinkedIn">💼</a>
```

**In Contact Section:**
Search for: `<div class="social-links-section">`

Same process - find and update the `href` attribute.

**In Footer:**
Search for: `<div class="footer-content">`

Update text links the same way.

### Adding a New Social Media Platform

**Step 1: Choose an Emoji**
Pick an emoji that represents the platform (e.g., 📸 for Instagram)

**Step 2: Add to Hero Section:**
```html
<div class="social-links">
    <!-- Existing links -->
    <a href="https://instagram.com/yourhandle" target="_blank" rel="noopener noreferrer" class="social-link" title="Instagram">📸</a>
</div>
```

**Step 3: Add to Contact Section:**
```html
<div class="social-links-section">
    <!-- Existing links -->
    <a href="https://instagram.com/yourhandle" target="_blank" rel="noopener noreferrer" class="social-link-large" title="Instagram">📸</a>
</div>
```

**Step 4: Add to Footer:**
```html
<p style="margin-top: 1rem; font-size: 0.9rem;">
    <!-- Existing links -->
    <a href="https://instagram.com/yourhandle" target="_blank" rel="noopener noreferrer" style="color: var(--slate); text-decoration: none;">Instagram</a>
</p>
```

---

## Managing Certifications

### Location
Search for: `<section id="certifications">`

### Adding a New Certification

**Template:**
```html
<div class="cert-card fade-in">
    <div class="cert-icon">🏆</div> <!-- Choose emoji -->
    <h3 class="cert-title">Certification Name</h3>
    <div class="cert-org">Issuing Organization</div>
    <div class="cert-date">Month Year</div>
    <a href="YOUR_CERTIFICATION_LINK" target="_blank" rel="noopener noreferrer" class="cert-link">View Certificate</a>
</div>
```

**Steps:**
1. Copy the template
2. Choose an appropriate emoji
3. Update certification name
4. Update organization name
5. Update date
6. Add link to Credly, certificate URL, or verification page
7. Paste in certifications section

### Updating Certification Links

```html
<!-- FIND: -->
<a href="https://www.credly.com/users/old-username" target="_blank" rel="noopener noreferrer" class="cert-link">View on Credly</a>

<!-- UPDATE: -->
<a href="https://www.credly.com/users/new-username" target="_blank" rel="noopener noreferrer" class="cert-link">View on Credly</a>
```

---

## Deleting Sections

### To Remove an Entire Section:

**Step 1: Find the Section**
Search for the section ID, for example: `<section id="projects"`

**Step 2: Find Section Boundaries**
- Opening tag: `<section id="projects">`
- Closing tag: `</section>`

**Step 3: Delete the Section**
Delete everything from opening `<section>` to closing `</section>`

**Step 4: Update Navigation**
Find and remove the corresponding navigation link:
```html
<!-- REMOVE THIS LINE: -->
<li><a href="#projects"><span>05.</span>Projects</a></li>
```

**Step 5: Renumber Remaining Sections**
Update `data-number` attributes for sections that come after the deleted one.

---

## Color Customization

### Location
Search for: `:root {`

You'll find color variables at the top of the CSS:

```css
:root {
    --navy: #0A192F;           /* Dark navy background */
    --light-navy: #112240;     /* Card backgrounds */
    --lightest-navy: #233554;  /* Borders */
    --mint: #64FFDA;           /* Primary accent color */
    --slate: #8892B0;          /* Body text */
    --light-slate: #A8B2D1;    /* Lighter text */
    --lightest-slate: #CCD6F6; /* Headings */
    --white: #FFFFFF;          /* Pure white */
    --deep-navy: #020C1B;      /* Page background */
    --orange: #FF6B35;         /* Affiliate cards */
    --purple: #A855F7;         /* Future use */
}
```

### Changing Colors

**Example - Change Accent Color:**
```css
/* CHANGE FROM: */
--mint: #64FFDA;

/* TO YOUR COLOR: */
--mint: #FF6B9D;  /* Pink accent */
```

**Example - Change Background:**
```css
/* CHANGE FROM: */
--deep-navy: #020C1B;

/* TO YOUR COLOR: */
--deep-navy: #1A1A2E;  /* Different dark color */
```

**Color Codes:**
- Use hex codes like `#64FFDA`
- Or use RGB like `rgb(100, 255, 218)`
- Find colors at: https://colorhunt.co or https://coolors.co

---

## Mobile Responsiveness

The portfolio is automatically mobile responsive! However, if you need to adjust mobile behavior:

### Location
Search for: `@media (max-width: 768px)`

This section contains mobile-specific styles.

### Common Mobile Adjustments

**Changing Mobile Font Size:**
```css
@media (max-width: 768px) {
    .hero-title {
        font-size: 2.5rem;  /* Adjust this value */
    }
}
```

**Changing Mobile Spacing:**
```css
@media (max-width: 768px) {
    section {
        padding: 80px 1.5rem;  /* Adjust padding */
    }
}
```

---

## Troubleshooting

### Problem: Changes Not Showing

**Solution:**
1. Make sure you saved the file (`Ctrl+S` or `Cmd+S`)
2. Hard refresh your browser:
   - **Windows:** `Ctrl + Shift + R` or `Ctrl + F5`
   - **Mac:** `Cmd + Shift + R`
3. Clear browser cache

### Problem: Section Numbers Wrong

**Solution:**
Update the `data-number` attribute for each section:
```html
<h2 class="section-title" data-number="01.">About Me</h2>
<h2 class="section-title" data-number="02.">Skills</h2>
<h2 class="section-title" data-number="03.">Experience</h2>
```

### Problem: Smooth Scroll Not Working

**Solution:**
Make sure section IDs match navigation href values:
```html
<!-- Navigation: -->
<a href="#about">About</a>

<!-- Section: -->
<section id="about">  <!-- Must match! -->
```

### Problem: Links Not Working

**Solution:**
Check that links include `https://` or `http://`:
```html
<!-- WRONG: -->
<a href="linkedin.com/in/yourname">LinkedIn</a>

<!-- CORRECT: -->
<a href="https://linkedin.com/in/yourname">LinkedIn</a>
```

### Problem: Layout Broken on Mobile

**Solution:**
1. Check that you didn't accidentally delete CSS code
2. Make sure all opening tags have closing tags
3. Validate your HTML at: https://validator.w3.org

### Problem: Icons/Emojis Not Showing

**Solution:**
1. Make sure you're using valid Unicode emojis
2. Check that your text editor is using UTF-8 encoding
3. Copy emojis from: https://emojipedia.org

---

## Quick Reference: Common Tasks

### ✅ Update Your Phone Number
Search for: `+91 8805555263` → Replace with new number

### ✅ Update Your Email
Search for: `vaibhav.selukar@gmail.com` → Replace with new email

### ✅ Update LinkedIn URL
Search for: `linkedin.com/in/vaibhav-selukar` → Replace with your URL

### ✅ Add a New Project
Go to vibe-coding section → Copy project card template → Customize

### ✅ Update Affiliate Link
Find the affiliate card → Update `href` attribute → Save

### ✅ Change Accent Color
Go to `:root` section → Update `--mint` color value

### ✅ Add a New Skill
Find skills section → Add `<li>Skill Name</li>` to appropriate category

### ✅ Update Job Experience
Find experience timeline → Update or add experience item

---

## Best Practices

### DO:
✅ Keep backups before making major changes  
✅ Test changes in a browser before deploying  
✅ Use consistent formatting and indentation  
✅ Keep section numbers sequential  
✅ Use descriptive project titles and descriptions  
✅ Keep affiliate links up to date  
✅ Regularly update experience and skills  

### DON'T:
❌ Delete CSS code unless you know what you're doing  
❌ Remove closing tags (always keep `</tag>` pairs)  
❌ Use relative URLs (always use full URLs with https://)  
❌ Forget to test on mobile devices  
❌ Leave placeholder text in production  
❌ Use expired affiliate links  

---

## Deployment to GitHub Pages

### Step 1: Create GitHub Repository
1. Go to https://github.com
2. Click "New Repository"
3. Name it: `your-username.github.io`
4. Make it public

### Step 2: Upload File
1. Click "Upload files"
2. Drag and drop `index.html`
3. Commit changes

### Step 3: Enable GitHub Pages
1. Go to repository Settings
2. Click "Pages" in sidebar
3. Select "main" branch
4. Save

### Step 4: Access Your Site
Your portfolio will be live at: `https://your-username.github.io`

---

## Support and Resources

### Helpful Websites:
- **HTML Tutorial:** https://www.w3schools.com/html/
- **CSS Tutorial:** https://www.w3schools.com/css/
- **Color Picker:** https://colorhunt.co
- **Emoji Finder:** https://emojipedia.org
- **HTML Validator:** https://validator.w3.org

### Need More Help?
- Search Google: "How to [your question] HTML"
- Ask ChatGPT or Claude AI for specific code help
- Check YouTube tutorials for visual guidance

---

## Changelog

Keep track of major changes you make:

```
## 2025-10-02
- Initial portfolio created
- Added 8 main sections
- Added 6 vibe coding projects
- Added 6 affiliate partners

## [Future Date]
- Your changes here
```

---

**Remember:** This portfolio is YOUR digital presence. Keep it updated, accurate, and reflective of your current skills and experiences. Update it regularly to showcase your growth and new projects!

Good luck! 🚀
