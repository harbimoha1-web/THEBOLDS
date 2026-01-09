# Complete Design Framework
## Master Reference from Don't Make Me Think, Refactoring UI, and The Design of Everyday Things

---

# BOOK 1: DON'T MAKE ME THINK
## A Common Sense Approach to Web Usability (Steve Krug)

---

## KRUG'S LAWS OF USABILITY

### First Law: Don't Make Me Think

**The single most important thing to understand about usability.**

When users look at a page, it should be:
1. **Self-evident** (best) - No thought required
2. **Self-explanatory** (acceptable) - Little thought required
3. **Requires thinking** (failure) - Users have to figure it out

**Things that make users think (BAD):**
- Clever names, marketing-speak, or company-specific terms
- Links and buttons that aren't obviously clickable
- Non-standard placement of elements
- Ambiguous instructions

**Things that are self-evident (GOOD):**
- Clear, descriptive labels
- Obvious visual hierarchy
- Standard conventions
- Visible cues for interactive elements

### Second Law: It Doesn't Matter How Many Clicks

**Each click should be a mindless, unambiguous choice.**

A user happily clicking 4 times with confidence beats frustratingly clicking once with confusion.

**Good clicks have:**
- Clear labels
- Obvious next step
- No dead ends
- Confidence they're on the right path

### Third Law: Get Rid of Half the Words

**Then get rid of half of what's left.**

| Before | After |
|--------|-------|
| "Welcome to our website! We're so glad you've decided to visit us today. Please feel free to browse our selection." | "Browse Products" |
| "In order to proceed, you will need to fill out the following form completely." | "Complete this form:" |

**Benefits of concise text:**
- Reduces noise
- Makes useful content more prominent
- Makes pages shorter
- Shows respect for user's time

---

## HOW USERS ACTUALLY USE THE WEB

### They Don't Read, They Scan

**Users glance at each page, scan some text, and click the first link that catches their interest.**

Why scanning?
- Users are usually on a mission
- They know they don't need to read everything
- They're good at scanning (years of practice)

**Implications:**
- Use lots of headings
- Keep paragraphs short
- Use bulleted lists
- Highlight key terms

### They Satisfice, Don't Optimize

**Users don't look for the best choice—they click the first reasonable option.**

Why?
- Time pressure
- Low stakes if wrong
- Weighing options is hard work
- Guessing is more fun

**Implications:**
- Make important options obvious
- Don't hide things in menus
- Put key info at the top

### They Muddle Through

**Users don't read instructions. They wing it.**

Why?
- Instructions are usually useless anyway
- Muddling through is faster
- If something works, they stick with it

**Implications:**
- Make things self-explanatory
- Design so that if users don't read instructions, they still succeed
- Put instructions ONLY where essential and keep them minimal

---

## VISUAL HIERARCHY

### Creating Effective Visual Hierarchy

**Visual hierarchy tells users what's important and how things are organized.**

Three key tasks:
1. **Prominence**: More important = more prominent
2. **Relationship**: Logically related = visually related
3. **Nesting**: What's "inside" what

**Tools for creating hierarchy:**

| Tool | How It Works |
|------|--------------|
| Size | Bigger = more important |
| Weight | Bolder = more important |
| Color | Brighter/contrasting = more important |
| Whitespace | More space around = more important |
| Position | Top/left = more important (in LTR cultures) |
| Proximity | Closer together = more related |

### The Squint Test

**Squint at your page. Can you still tell:**
- What's most important?
- What's clickable?
- What groups together?

If not, your visual hierarchy needs work.

---

## NAVIGATION DESIGN

### The Purpose of Navigation

Navigation tells users:
1. **Where am I?** - Current location
2. **What's here?** - What this site/section offers
3. **Where can I go?** - Available destinations
4. **How do I get there?** - Path to destination
5. **How do I get back?** - Return path

### Navigation Must-Haves

**1. Site ID (Logo)**
- Top left corner (convention)
- Links to home page
- Present on every page

**2. Primary Navigation**
- Top of page or left side
- 4-7 items max
- Clear labels (not clever names)

**3. Utilities**
- Secondary actions (search, account, cart)
- Top right corner
- Consistent across pages

**4. Page Name**
- Large, prominent
- Matches what user clicked
- Only one on the page

**5. You Are Here Indicator**
- Highlight current location
- Use multiple cues (color, weight, pointer)
- Works in navigation AND breadcrumbs

**6. Breadcrumbs**
- Show path from home to here
- Format: Home > Section > Subsection > Current
- Current page not a link
- Small, top of page, out of the way

### The Trunk Test

**Can users answer these on any page?**

1. What site is this? (Site ID)
2. What page am I on? (Page name)
3. What are the major sections? (Primary nav)
4. What are my options at this level? (Local nav)
5. Where am I in the scheme of things? (You are here)
6. How can I search? (Search box)

---

## HOMEPAGE DESIGN

### The Homepage Mission

**The homepage must accomplish several things at once:**

1. **Site identity and mission** - What is this site and what's it for?
2. **Site hierarchy** - What can I find here?
3. **Search** - Let me find what I need
4. **Teases** - Content highlights to draw me in
5. **Timely content** - What's new, deals, news
6. **Shortcuts** - Most popular features
7. **Registration/Login** - Account access

### Homepage Constraints

**The challenge**: Too much to convey, too little space

**Common mistakes:**
- Trying to do everything
- Marketing speak instead of clarity
- No clear starting point
- Changing the homepage constantly

**Solution**: Prioritize ruthlessly. The homepage tagline should explain what the site is in 6-8 words.

### The Homepage Tagline

**Good taglines:**
- Clear (not clever)
- Specific to this site
- Convey value proposition
- Short (6-8 words max)

**Examples:**
- Bad: "Solutions for a Changing World"
- Good: "Compare prices from 100+ stores"
- Bad: "Empowering Innovation"
- Good: "Find recipes by ingredients you have"

---

## USABILITY TESTING

### Krug's One-Morning-a-Month Testing

**Usability testing doesn't have to be expensive or formal.**

**The simple approach:**
- 1 morning per month
- 3 users per session
- Watch them use your site
- Debrief immediately after
- Fix the biggest problems
- Repeat next month

### What You Need

| Item | Details |
|------|---------|
| Users | 3 is enough (find major problems) |
| Tasks | 3-5 realistic scenarios |
| Location | Any quiet room with a computer |
| Recording | Screen + face (optional) |
| Observers | Designers, developers, stakeholders |
| Compensation | $50-100 or gift card |

### How to Run a Test

**1. Before the test:**
- Prepare tasks (realistic scenarios)
- Set up screen recording
- Have observers ready

**2. During the test (45-60 min):**
- Welcome and explain the process
- Ask background questions
- Give tasks one at a time
- Have them think aloud
- Don't help or lead
- Thank and compensate

**3. After the test:**
- Debrief immediately with observers
- Prioritize problems found
- Focus on biggest 3-5 issues
- Fix before next month's test

### Testing Principles

**You're testing the site, not the user.**
- Never say "you did that wrong"
- If they struggle, it's a design problem
- Every confused moment = insight

**Don't explain. Observe.**
- Resist urge to help
- Ask "What are you looking for?"
- Ask "What did you expect to happen?"

**The first three users find most problems.**
- More users = diminishing returns
- Better to test more often with fewer users

---

## MOBILE USABILITY

### Mobile Differences

**Smaller screen amplifies everything:**
- Less room for navigation
- Every tap must count
- No hover states
- Fat finger problem

**Mobile challenges:**
- Managing real estate
- One-thumb operation
- Variable conditions (bright sun, distraction)
- Touch targets (44px minimum)

### Mobile Design Rules

**1. Allow zooming**
Don't disable pinch-to-zoom. Users need it.

**2. Provide an obvious way home**
- Tap logo to return home
- Or persistent home icon

**3. Design for thumb reach**
- Most important = bottom of screen
- Less important = top
- Consider one-handed use

**4. Signify tappability**
- Buttons look like buttons
- Links look like links
- No mystery meat navigation

**5. Avoid text input when possible**
- Use pickers, toggles, selects
- Auto-complete where possible
- Remember previous entries

### Responsive vs. Separate

**Responsive (same URL, adapts to screen):**
- One codebase to maintain
- SEO benefits
- Users get same content everywhere

**Separate mobile site (m.example.com):**
- Can optimize specifically for mobile
- But: maintenance burden, sync issues
- Generally not recommended anymore

---

## ACCESSIBILITY

### Basic Accessibility Principles

**1. Add alt text to images**
- Describe the image's purpose
- Decorative images: empty alt=""
- Informative images: describe content

**2. Use headings properly**
- H1 for main title
- H2-H6 in proper hierarchy
- Don't skip levels

**3. Ensure keyboard navigation**
- Tab through all interactive elements
- Focus states visible
- Skip links for navigation

**4. Color is not the only indicator**
- Don't rely on color alone
- Add icons, patterns, or text

**5. Sufficient contrast**
- 4.5:1 minimum for normal text
- 3:1 for large text
- Use contrast checker tools

**Accessibility helps everyone:**
- Screen readers
- Motor impairments
- Temporary disabilities
- Situational (bright sun, one hand)
- Aging users

---

# BOOK 2: REFACTORING UI
## Practical Design Tips (Adam Wathan & Steve Schoger)

---

## STARTING FROM SCRATCH

### Don't Design Full Pages

**Start with a feature, not a layout.**

Bad approach:
- Open blank canvas
- Draw navigation, sidebar, footer
- Try to fill in content

Good approach:
- What's the core feature?
- Design that feature alone
- Build the page around it

### Detail Comes Later

**Design in grayscale first.**

Why:
- Forces you to rely on spacing and contrast
- Prevents color from covering bad hierarchy
- Makes you focus on structure first

**Add color last, only where it adds meaning.**

### Don't Over-invest Early

**Work low-fidelity first.**

| Stage | Fidelity | Purpose |
|-------|----------|---------|
| Sketching | Low | Explore ideas quickly |
| Wireframes | Low | Test layout and flow |
| Mockups | Medium | Refine visual design |
| High-Fi | High | Final polish |

**Moving to high-fidelity too early = wasted time when things change.**

### Design Systems Come Last

**Don't start with a design system.**

Common mistake:
- Spend weeks on button styles
- Create comprehensive color palette
- Design components in isolation
- ...then realize they don't work together

Better approach:
- Design real features first
- Extract patterns that repeat
- Build system from proven components

---

## HIERARCHY IS EVERYTHING

### Size Isn't Everything

**Stop relying on font size for hierarchy.**

Instead, use:
- **Font weight** (bold = emphasis)
- **Color** (gray = de-emphasized)
- **Spacing** (more space = more important)
- **Letter-spacing** (looser = de-emphasized)

### Limit Your Choices

**Two or three font sizes is enough for most UI.**

| Use Case | Size | Weight |
|----------|------|--------|
| Page title | Large | Bold |
| Section heading | Medium | Bold |
| Body text | Base | Normal |
| Secondary text | Base | Normal (gray) |
| Small labels | Small | Medium |

**Vary weight and color, not size.**

### De-emphasize by De-emphasizing

**Don't try to emphasize everything—de-emphasize the unimportant.**

```
Bad:  TITLE (bold, large, dark)
      Subtitle (bold, medium, dark)

Good: Title (semibold, large)
      Subtitle (normal, medium, gray)
```

### Use Labels as Last Resort

**Data speaks louder than labels.**

| Instead of | Use |
|------------|-----|
| Name: John Smith | John Smith (just the name) |
| Email: john@example.com | john@example.com (email format is obvious) |
| Price: $99 | $99 ($ makes it obvious) |

**When labels are needed, use them as secondary text (smaller, grayer).**

### Separate Visual Hierarchy from Document Hierarchy

**Semantic hierarchy (H1, H2) ≠ Visual hierarchy**

It's okay for an H2 to be visually larger than an H1 if the design calls for it. Style independently from semantics.

---

## LAYOUT AND SPACING

### The Spacing System

**Use a defined spacing scale. Don't eyeball it.**

Base unit: 4px or 8px

**4px-based scale:**
```
4, 8, 12, 16, 24, 32, 48, 64, 96, 128
```

**8px-based scale:**
```
8, 16, 24, 32, 48, 64, 96, 128, 192, 256
```

**Rules:**
- Adjacent values should feel different (not 8 and 10)
- Use relative jumps, not linear
- Pick one scale and stick to it

### Start with Too Much Space

**White space is good. You probably need more.**

Common mistake: Cramming things together to "save space"

Reality: Extra space makes things:
- Easier to scan
- More elegant
- Appear higher quality

**You can always remove space. Start with more.**

### You Don't Need Even Spacing

**Asymmetric spacing often works better.**

Example (card):
```
┌────────────────────────────────┐
│            (more space)        │
│    Title                       │
│    Description text here       │
│            (less space)        │
│    [ Button ]                  │
│            (more space)        │
└────────────────────────────────┘
```

The title and description are related (less space). The button is separate (more space above it).

### Define the Width

**Don't fill the container. Choose a width.**

| Content Type | Max Width |
|--------------|-----------|
| Paragraph text | 60-75 characters (~600px) |
| Headlines | Wider okay |
| Forms | 300-400px |
| Cards | Content-appropriate |

**Full-width text is hard to read. Constrain it.**

### Responsive Grid Isn't Always the Answer

**Grids force artificial relationships.**

Instead of 12-column grid everywhere:
- Let content determine width
- Use max-width constraints
- Stack on mobile, don't squeeze

### Columns Don't Have to Match

**Sidebars don't need to grow with main content.**

```
Bad:  [  Sidebar 25%  ][    Main Content 75%    ]
      (Both grow/shrink proportionally)

Good: [ Sidebar 300px ][    Main Content flex    ]
      (Sidebar stays fixed, content fills rest)
```

---

## TYPOGRAPHY

### Type Scale

**Define a limited type scale upfront.**

```typescript
const fontSize = {
  xs: 12,   // captions, fine print
  sm: 14,   // secondary text
  base: 16, // body text
  lg: 18,   // emphasized body
  xl: 20,   // subheadings
  '2xl': 24, // headings
  '3xl': 30, // page titles
  '4xl': 36, // hero titles
  '5xl': 48, // display
}
```

**Skip sizes that are too close. The difference should be obvious.**

### Line Height

**Line height depends on font size and line length.**

| Font Size | Line Height |
|-----------|-------------|
| Small (12-14px) | 1.5 (150%) |
| Base (16px) | 1.5-1.75 |
| Large (24px+) | 1.25-1.5 |
| Headlines | 1.1-1.25 |

**Wider lines = taller line-height (easier to find next line)**

### Font Weight

**Use weight for hierarchy, not just size.**

```
400 (Normal) - Body text
500 (Medium) - Slightly emphasized
600 (Semibold) - Headings
700 (Bold) - Strong emphasis only
```

**Rule: If everything is bold, nothing is bold.**

### Letter Spacing

**Adjust letter-spacing for headlines and small caps.**

```css
/* Headlines: tighter */
.headline {
  letter-spacing: -0.025em;
}

/* All caps: looser */
.label {
  letter-spacing: 0.05em;
  text-transform: uppercase;
}
```

### Align with Baseline

**When mixing font sizes, align by baseline, not center.**

```
Bad:  Small   LARGE   Small (vertically centered)
Good: Small   LARGE   Small (all sitting on same line)
```

---

## COLOR

### HSL Over Hex

**Use HSL for more intuitive color control.**

```
HSL: Hue, Saturation, Lightness

Hue (0-360): The color (red, blue, green)
Saturation (0-100%): How vivid
Lightness (0-100%): How bright
```

**Why HSL is better:**
- Change brightness without changing color
- Create variations easily
- More intuitive than RGB/Hex

### Building a Color Palette

**For each color, create 9 shades:**

```
50:  Lightest (backgrounds)
100: Very light (hover states)
200: Light
300: Light-mid
400: Mid-light
500: Base (your brand color)
600: Mid-dark
700: Dark
800: Very dark
900: Darkest (text on light bg)
```

**Process:**
1. Pick your base (500)
2. Pick darkest (900) and lightest (50)
3. Fill in between
4. Adjust saturation at extremes (less at edges)

### Perceived Brightness

**Not all colors are equally bright at same lightness.**

Yellow appears brighter than blue at the same HSL lightness.

**Rotate hue as you change brightness:**
- Brighter shades: rotate toward yellow (60°)
- Darker shades: rotate toward blue (240°)

### Don't Use Gray Text on Colored Backgrounds

**Gray text on colors looks washed out.**

Instead:
- Use white with reduced opacity: `rgba(255, 255, 255, 0.8)`
- Or: Pick a color from the same family but lighter

### Semantic Colors

**Define colors by purpose:**

```typescript
const colors = {
  primary: '#3B82F6',    // brand, main CTAs
  secondary: '#6B7280',  // secondary actions
  success: '#10B981',    // confirmations, positive
  warning: '#F59E0B',    // caution, attention
  error: '#EF4444',      // errors, destructive
  info: '#3B82F6',       // informational
}
```

### Accessible Contrast

**Minimum contrast ratios (WCAG):**

| Text Size | Minimum Ratio |
|-----------|---------------|
| Normal text | 4.5:1 |
| Large text (18px+ or 14px bold) | 3:1 |
| UI components | 3:1 |

**Use a contrast checker before finalizing.**

---

## DEPTH

### Shadows > Borders

**Use shadows for depth, not borders.**

| Effect | Use Case |
|--------|----------|
| Border | Separating similar elements |
| Shadow | Elevating element above page |

```css
/* Instead of border */
.card {
  border: 1px solid #e5e7eb;
}

/* Use shadow */
.card {
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}
```

### Shadow Scale

**Define a shadow scale like spacing:**

```typescript
const shadows = {
  sm: '0 1px 2px rgba(0, 0, 0, 0.05)',
  DEFAULT: '0 1px 3px rgba(0, 0, 0, 0.1), 0 1px 2px rgba(0, 0, 0, 0.06)',
  md: '0 4px 6px rgba(0, 0, 0, 0.1), 0 2px 4px rgba(0, 0, 0, 0.06)',
  lg: '0 10px 15px rgba(0, 0, 0, 0.1), 0 4px 6px rgba(0, 0, 0, 0.05)',
  xl: '0 20px 25px rgba(0, 0, 0, 0.1), 0 10px 10px rgba(0, 0, 0, 0.04)',
  '2xl': '0 25px 50px rgba(0, 0, 0, 0.25)',
}
```

### Shadow Properties

**Shadows have multiple properties to control:**

```
X offset: Horizontal (usually 0)
Y offset: Vertical (1-25px)
Blur: Softness (2-50px)
Spread: Size expansion (-2 to 10px)
Color: Usually black with opacity
```

**Key insights:**
- Bigger blur = more diffuse, softer
- Larger Y offset = higher elevation
- Multiple shadows = more realistic

### Shadows Communicate Elevation

| Shadow | Elevation | Use For |
|--------|-----------|---------|
| None | Ground level | Default elements |
| sm | Slightly raised | Cards, wells |
| md | Raised | Dropdowns, tooltips |
| lg | Floating | Modals, dialogs |
| xl | Highest | Popovers, drag-drop |

### Two Shadows

**Combine two shadows for realism:**

```css
box-shadow:
  0 1px 3px rgba(0, 0, 0, 0.12),  /* Ambient: soft, diffuse */
  0 1px 2px rgba(0, 0, 0, 0.24);  /* Direct: sharp, close */
```

---

## IMAGES

### Text on Images

**Make text readable over images:**

1. **Overlay**: Semi-transparent dark overlay
2. **Gradient**: Fade to black at text area
3. **Box**: Background behind text
4. **Colorize**: Reduce image contrast
5. **Text Shadow**: Subtle shadow on text

### Background Image Treatment

```css
/* Dark overlay */
.hero::after {
  background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5));
}

/* Gradient overlay */
.hero::after {
  background: linear-gradient(to top, rgba(0,0,0,0.8), transparent);
}
```

### User-Uploaded Images

**Don't trust user images to be perfect.**

- Set background color (if image fails to load)
- Use object-fit: cover (prevent stretching)
- Consider placeholder silhouettes
- Crop to consistent aspect ratios

```css
.avatar {
  background-color: #e5e7eb;
  object-fit: cover;
  aspect-ratio: 1;
}
```

### Empty States

**Design for when there's no content.**

Components of good empty states:
- Illustration or icon
- Headline (what this area shows)
- Description (why it's empty)
- CTA (how to add content)

```
┌──────────────────────────────────┐
│          [illustration]          │
│                                  │
│      No projects yet             │
│  Create your first project to    │
│  get started.                    │
│                                  │
│      [ Create Project ]          │
└──────────────────────────────────┘
```

---

## COMPONENT PATTERNS

### Buttons

**Button hierarchy:**

```
Primary:   Solid, brand color (1 per screen)
Secondary: Outlined or lighter fill
Tertiary:  Text only, no fill

Destructive: Red for dangerous actions
```

**Button states:**
- Default
- Hover: Slightly darker or lighter
- Active/Pressed: Darker still
- Disabled: Reduced opacity (50-70%)
- Loading: Spinner, disabled state

```typescript
// React Native button styles
const buttonVariants = {
  primary: {
    backgroundColor: '#3B82F6',
    color: '#FFFFFF',
  },
  secondary: {
    backgroundColor: 'transparent',
    borderColor: '#3B82F6',
    borderWidth: 1,
    color: '#3B82F6',
  },
  ghost: {
    backgroundColor: 'transparent',
    color: '#3B82F6',
  },
}
```

### Inputs

**Input field anatomy:**
- Label (above or floating)
- Input field (defined height, padding)
- Placeholder (gray, disappears on focus)
- Help text (below, smaller)
- Error state (red border, error message)

**Input heights:**
```
Small:  32-36px
Medium: 40-44px
Large:  48-52px
```

**Focus states:**
```css
.input:focus {
  border-color: #3B82F6;
  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
  outline: none;
}
```

### Cards

**Card structure:**
```
┌────────────────────────────────┐
│  [Image]                       │
├────────────────────────────────┤
│  Title                         │
│  Description text...           │
│                                │
│  Metadata | More metadata      │
│                                │
│  [Action]          [Action]    │
└────────────────────────────────┘
```

**Card spacing:**
- Content padding: 16-24px
- Gap between sections: 12-16px
- Image bleeds to edge (no padding)

### Tables

**Table design tips:**
- Align text left, numbers right
- Use subtle zebra striping OR row borders (not both)
- Fixed headers on scroll
- Actions column on right
- Don't center anything except icons

### Forms

**Form layout:**
- One column (usually)
- Related fields grouped
- Labels above inputs (mobile-friendly)
- Required indicator: * or "(required)"
- Error messages inline, near field

**Form spacing:**
```
Between fields: 16-24px
Between groups: 32-48px
Label to input: 4-8px
Input to helper: 4px
```

---

## PRACTICAL CODE PATTERNS

### React Native Spacing System

```typescript
export const spacing = {
  0: 0,
  1: 4,
  2: 8,
  3: 12,
  4: 16,
  5: 20,
  6: 24,
  8: 32,
  10: 40,
  12: 48,
  16: 64,
  20: 80,
  24: 96,
} as const;

// Usage
const styles = StyleSheet.create({
  container: {
    padding: spacing[4],      // 16px
    marginBottom: spacing[6], // 24px
  },
});
```

### Typography System

```typescript
export const typography = {
  // Font sizes
  xs: { fontSize: 12, lineHeight: 16 },
  sm: { fontSize: 14, lineHeight: 20 },
  base: { fontSize: 16, lineHeight: 24 },
  lg: { fontSize: 18, lineHeight: 28 },
  xl: { fontSize: 20, lineHeight: 28 },
  '2xl': { fontSize: 24, lineHeight: 32 },
  '3xl': { fontSize: 30, lineHeight: 36 },
  '4xl': { fontSize: 36, lineHeight: 40 },

  // Font weights
  normal: { fontWeight: '400' as const },
  medium: { fontWeight: '500' as const },
  semibold: { fontWeight: '600' as const },
  bold: { fontWeight: '700' as const },
};

// Usage
const styles = StyleSheet.create({
  heading: {
    ...typography['2xl'],
    ...typography.semibold,
  },
  body: {
    ...typography.base,
    ...typography.normal,
  },
});
```

### Color System

```typescript
export const colors = {
  // Grays
  gray: {
    50: '#F9FAFB',
    100: '#F3F4F6',
    200: '#E5E7EB',
    300: '#D1D5DB',
    400: '#9CA3AF',
    500: '#6B7280',
    600: '#4B5563',
    700: '#374151',
    800: '#1F2937',
    900: '#111827',
  },

  // Primary (Blue)
  primary: {
    50: '#EFF6FF',
    100: '#DBEAFE',
    200: '#BFDBFE',
    300: '#93C5FD',
    400: '#60A5FA',
    500: '#3B82F6',
    600: '#2563EB',
    700: '#1D4ED8',
    800: '#1E40AF',
    900: '#1E3A8A',
  },

  // Semantic
  success: '#10B981',
  warning: '#F59E0B',
  error: '#EF4444',
  info: '#3B82F6',
};
```

### Shadow System (React Native)

```typescript
import { Platform } from 'react-native';

export const shadows = {
  sm: Platform.select({
    ios: {
      shadowColor: '#000',
      shadowOffset: { width: 0, height: 1 },
      shadowOpacity: 0.05,
      shadowRadius: 2,
    },
    android: {
      elevation: 1,
    },
  }),
  md: Platform.select({
    ios: {
      shadowColor: '#000',
      shadowOffset: { width: 0, height: 4 },
      shadowOpacity: 0.1,
      shadowRadius: 6,
    },
    android: {
      elevation: 3,
    },
  }),
  lg: Platform.select({
    ios: {
      shadowColor: '#000',
      shadowOffset: { width: 0, height: 10 },
      shadowOpacity: 0.15,
      shadowRadius: 15,
    },
    android: {
      elevation: 6,
    },
  }),
};
```

### Border Radius System

```typescript
export const borderRadius = {
  none: 0,
  sm: 4,
  DEFAULT: 8,
  md: 12,
  lg: 16,
  xl: 24,
  full: 9999,
};
```

---

# BOOK 3: THE DESIGN OF EVERYDAY THINGS
## Psychology of Design (Don Norman)

---

## THE PSYCHOLOGY OF EVERYDAY ACTIONS

### The Two Gulfs

**Gulf of Execution**: The gap between intention and action
- "How do I make this happen?"
- "What can I do?"
- "Is there any feedback that I'm doing it right?"

**Gulf of Evaluation**: The gap between action and understanding
- "What happened?"
- "Did I do what I wanted?"
- "Is this the correct state?"

**Good design minimizes both gulfs.**

### The Seven Stages of Action

```
GOAL
  ↓
┌─────────────────────────────────────┐
│ GULF OF EXECUTION                   │
│  1. Goal (form the goal)            │
│  2. Plan (the action)               │
│  3. Specify (the action sequence)   │
│  4. Perform (the action)            │
└─────────────────────────────────────┘
  ↓
WORLD
  ↓
┌─────────────────────────────────────┐
│ GULF OF EVALUATION                  │
│  5. Perceive (the state of world)   │
│  6. Interpret (the perception)      │
│  7. Compare (outcome to goal)       │
└─────────────────────────────────────┘
  ↓
GOAL (achieved or retry)
```

**Design implications:**
- Make actions discoverable (stages 2-3)
- Provide feedback (stage 5)
- Make state visible (stage 6)
- Show connection between action and result (stage 7)

---

## AFFORDANCES AND SIGNIFIERS

### Affordances

**What an object allows you to do.**

| Object | Affordance |
|--------|------------|
| Chair | Sitting |
| Button | Pushing |
| Knob | Turning |
| Handle | Pulling |
| Flat plate | Pushing |

**Affordances exist whether perceived or not.**

A glass door affords walking through—but if you can't see the glass, you won't know.

### Signifiers

**What signals where action should occur.**

**Signifiers make affordances visible.**

| Affordance | Signifier |
|------------|-----------|
| Door opens | Handle (pull) or plate (push) |
| Button is pressable | 3D appearance, hover state |
| Text is clickable | Underline, blue color |
| Area is tappable | Raised surface, icon |

**The most important design principle:**
When affordances aren't visible, provide signifiers.

### In Digital UI

| Element | Affordance | Signifier |
|---------|------------|-----------|
| Button | Tap/click | Raised appearance, color contrast |
| Link | Navigate | Underline, blue text |
| Slider | Drag | Track + thumb + cursor |
| Input | Type | Border, placeholder |
| Checkbox | Toggle | Box + checkmark |

**Common signifier problems:**
- Flat design removes signifiers
- "Ghost buttons" don't look clickable
- Links without underlines blend with text

---

## MAPPING

### What is Mapping?

**The relationship between controls and their effects.**

**Natural mapping**: Controls are arranged like the things they control.

| Good Mapping | Bad Mapping |
|--------------|-------------|
| Stovetop controls arranged like burners | Row of identical switches |
| Volume slider goes up = louder | Arbitrary button assignments |
| Arrow keys match screen direction | Arrow keys do random things |

### Types of Mapping

**1. Spatial correspondence**
Controls physically match the layout of what they control.

```
Good:
Burner layout:    [1] [2]    Controls:  [1] [2]
                  [3] [4]               [3] [4]

Bad:
Burner layout:    [1] [2]    Controls:  [1] [2] [3] [4]
                  [3] [4]
```

**2. Cultural conventions**
- Red = stop, danger
- Green = go, success
- Up/right = increase
- Down/left = decrease

**3. Semantic**
Related functions grouped together.

### Digital Mapping Examples

**Good mapping:**
- Volume slider goes up = louder (natural)
- Red delete button = dangerous action (cultural)
- Undo/Redo arrows point left/right (temporal direction)
- Related settings grouped (semantic)

**Bad mapping:**
- Arbitrary keyboard shortcuts
- Settings scattered across menus
- Controls far from what they affect

---

## FEEDBACK

### What is Feedback?

**Information about the result of an action.**

Every action should have immediate, obvious feedback.

### Feedback Types

| Type | Example |
|------|---------|
| Visual | Button color change, animation |
| Auditory | Click sound, success chime |
| Haptic | Vibration, force feedback |
| System | Progress bar, loading spinner |

### Good Feedback Is

**1. Immediate**
- Delay = confusion
- Even 100ms feels slow
- Show SOMETHING instantly (skeleton, spinner)

**2. Informative**
- What happened?
- Was it successful?
- What's next?

**3. Proportional**
- Small action = subtle feedback
- Large action = clear confirmation
- Dangerous action = explicit warning

**4. Not annoying**
- Too much = ignored
- Too loud = irritating
- Find balance

### Feedback Examples

```
Action: Button tap
Feedback:
  - Immediate: Color change, press animation
  - Processing: Spinner, disabled state
  - Complete: Success message, screen transition

Action: Form submission
Feedback:
  - Immediate: Button loading state
  - Processing: Progress indication
  - Success: Confirmation message, redirect
  - Error: Inline errors, shake animation

Action: Swipe to delete
Feedback:
  - During: Red background reveals
  - Confirm: Item slides out, undo toast
  - Complete: List reflows
```

---

## CONCEPTUAL MODELS

### What is a Conceptual Model?

**The user's understanding of how something works.**

Users build mental models of systems. Good design provides models that:
- Are simple
- Match reality enough to be useful
- Are learnable

### The Designer's Responsibility

Three models in play:

```
DESIGNER'S MODEL     →    SYSTEM IMAGE    →    USER'S MODEL
(How designer        (What user can      (How user thinks
thinks it works)      see and interact)   it works)
```

**The system image must communicate the designer's model clearly.**

If the system image is poor, users build wrong models and make errors.

### Examples

**Good conceptual model:**
- Desktop metaphor (files, folders, trash)
- Shopping cart (add items, checkout)
- Feed (scroll to see more)

**Poor conceptual model:**
- Complex modal states
- Hidden gestures
- Invisible system modes

### Building Good Models

1. **Consistency**: Similar things work similarly
2. **Visibility**: Show system state
3. **Metaphor**: Map to real-world concepts
4. **Feedback**: Confirm the model is correct

---

## CONSTRAINTS

### What are Constraints?

**Limiting actions to prevent errors.**

Constraints reduce the "space of possible actions" to only valid ones.

### Types of Constraints

**1. Physical Constraints**
Object's shape prevents wrong actions.

| Example | How It Constrains |
|---------|-------------------|
| USB-C port | Only one orientation |
| SIM card | Only fits one way |
| Key slot | Matches key shape |

**Digital equivalent:**
- Disabled buttons (can't click)
- Character limits (can't type more)
- Selection restrictions (can't choose invalid options)

**2. Semantic Constraints**
Meaning restricts possibilities.

| Example | How It Constrains |
|---------|-------------------|
| Motorcycle seat | Obviously for sitting |
| Windshield | Faces forward |

**Digital equivalent:**
- Icons suggest meaning
- Labels explain purpose
- Context suggests action

**3. Cultural Constraints**
Shared conventions.

| Example | Convention |
|---------|------------|
| Red means stop | Traffic light |
| X means close | Window controls |
| Trash icon means delete | Desktop metaphor |

**4. Logical Constraints**
Reasoning about relationships.

| Example | Logic |
|---------|-------|
| Only one piece left = goes here | Puzzle |
| Only option remaining | Elimination |

**Digital equivalent:**
- Required fields can't be skipped
- Certain options only appear in context
- Workflows enforce order

---

## ERROR DESIGN

### Types of Errors

**1. Slips**: Right intention, wrong action
- Typos
- Tapping wrong button
- Accidentally deleting

**2. Mistakes**: Wrong intention
- Misunderstanding the system
- Wrong mental model
- Incorrect decision

### Designing for Slips

**Prevention:**
- Large touch targets (44px minimum)
- Adequate spacing between actions
- Undo capabilities

**Recovery:**
- Easy undo (Cmd+Z, shake to undo)
- Confirmation for destructive actions
- Forgiving input (auto-correct, suggestions)

### Designing for Mistakes

**Prevention:**
- Clear signifiers
- Sensible defaults
- Constrain options
- Make state visible

**Recovery:**
- Clear error messages
- Explanation of what went wrong
- Path to fix it

### Error Message Design

**Bad error messages:**
- "Error 500"
- "Invalid input"
- "Something went wrong"

**Good error messages:**
1. Say what happened (specifically)
2. Explain why it happened (if possible)
3. Tell users how to fix it

```
Bad:  "Invalid email"
Good: "Email address needs an @ symbol. Example: you@email.com"

Bad:  "Upload failed"
Good: "File too large. Please choose an image under 5MB."
```

---

## HUMAN-CENTERED DESIGN

### The HCD Process

```
1. OBSERVE
   ↓ Understand users and their problems
2. IDEATE
   ↓ Generate potential solutions
3. PROTOTYPE
   ↓ Build quick, cheap testable versions
4. TEST
   ↓ Get feedback from real users
5. ITERATE
   ↓ Refine based on learnings
(repeat)
```

### Principles of HCD

**1. Focus on people**
- Who are the users?
- What do they need?
- What are their constraints?

**2. Find the root cause**
- Don't solve the wrong problem
- Ask "why" multiple times
- Understand the real need

**3. Think in systems**
- Consider the whole experience
- How does this fit into their life?
- What happens before and after?

**4. Test rapidly**
- Get feedback early and often
- Cheap prototypes beat expensive development
- Be willing to be wrong

**5. Iterate**
- First solution is rarely best
- Learn and improve continuously
- Small changes, test, repeat

---

## SEVEN DESIGN PRINCIPLES (SUMMARY)

Don Norman's core principles:

### 1. Discoverability
Can users figure out what's possible and how to do it?

### 2. Feedback
Does every action produce feedback about what happened?

### 3. Conceptual Model
Does the design communicate how the system works?

### 4. Affordances
Does the design suggest what actions are possible?

### 5. Signifiers
Are there clear signals for where and how to act?

### 6. Mappings
Is the relationship between controls and effects natural?

### 7. Constraints
Does the design prevent errors and guide correct action?

---

# QUICK REFERENCE CHECKLISTS

---

## UI REVIEW CHECKLIST (KRUG)

### First Impression
- [ ] Can users tell what the site/app is in 5 seconds?
- [ ] Is the main action obvious?
- [ ] Is there a clear visual hierarchy?

### Navigation
- [ ] Can users tell where they are?
- [ ] Is the primary navigation visible?
- [ ] Are labels clear and descriptive?
- [ ] Is there a way to get home?

### Content
- [ ] Is text scannable (headings, bullets)?
- [ ] Have you cut half the words?
- [ ] Are instructions minimal?
- [ ] Do images serve a purpose?

### Interaction
- [ ] Are clickable things obviously clickable?
- [ ] Are forms simple and clear?
- [ ] Is feedback immediate?

---

## COMPONENT DESIGN CHECKLIST (REFACTORING UI)

### Visual Hierarchy
- [ ] Is importance clear without reading?
- [ ] Are you using weight and color, not just size?
- [ ] Is secondary info de-emphasized?

### Spacing
- [ ] Using consistent spacing scale?
- [ ] Is there enough whitespace?
- [ ] Are related items grouped?

### Typography
- [ ] Limited to 2-3 font sizes?
- [ ] Is line-height appropriate?
- [ ] Is text width under 75 characters?

### Color
- [ ] Is color used semantically?
- [ ] Is contrast sufficient?
- [ ] Not relying on color alone?

### Depth
- [ ] Using shadows instead of borders?
- [ ] Is elevation consistent?
- [ ] Do shadows match light source?

---

## USABILITY CHECKLIST (NORMAN)

### Affordances & Signifiers
- [ ] Is it clear what can be interacted with?
- [ ] Do interactive elements look interactive?
- [ ] Are actions discoverable?

### Feedback
- [ ] Does every action have feedback?
- [ ] Is feedback immediate?
- [ ] Is the current state visible?

### Mapping
- [ ] Do controls relate to their effects?
- [ ] Are related controls grouped?
- [ ] Do cultural conventions apply?

### Constraints
- [ ] Are impossible actions prevented?
- [ ] Are errors constrained?
- [ ] Is destructive action protected?

### Error Handling
- [ ] Are errors described clearly?
- [ ] Can users recover easily?
- [ ] Is undo available?

---

## MOBILE DESIGN CHECKLIST

### Touch Targets
- [ ] Minimum 44x44px touch targets?
- [ ] Adequate spacing between targets?
- [ ] Primary actions in thumb zone?

### Performance
- [ ] Fast initial load?
- [ ] Skeleton screens for loading?
- [ ] Optimized images?

### Input
- [ ] Minimized text input?
- [ ] Correct keyboard types?
- [ ] Auto-complete where possible?

### Navigation
- [ ] Clear back navigation?
- [ ] Persistent navigation visible?
- [ ] Gestures have alternatives?

### Responsiveness
- [ ] Works in portrait and landscape?
- [ ] Handles various screen sizes?
- [ ] Text scales appropriately?

---

## ACCESSIBILITY CHECKLIST

### Visual
- [ ] Contrast ratio 4.5:1 minimum?
- [ ] Not relying on color alone?
- [ ] Focus states visible?

### Screen Readers
- [ ] All images have alt text?
- [ ] Heading hierarchy correct?
- [ ] Form labels associated with inputs?

### Interaction
- [ ] Keyboard navigable?
- [ ] Skip links available?
- [ ] Touch targets large enough?

### Content
- [ ] Language simple and clear?
- [ ] Reading order logical?
- [ ] Error messages descriptive?

---

# HOW TO USE THIS DOCUMENT

When working on design tasks, reference specific frameworks:

**For Usability Review:**
- "Apply Krug's usability principles to this screen"
- "Run the Trunk Test on this navigation"
- "Check this page with the Squint Test"

**For Visual Design:**
- "Use the Refactoring UI spacing system"
- "Apply the typography scale to this component"
- "Create a color palette using HSL"

**For Interaction Design:**
- "What affordances and signifiers does this need?"
- "Apply Norman's feedback principles"
- "How can we constrain errors here?"

**For Component Work:**
- "Design this button using the button variants pattern"
- "Create this input following the input field anatomy"
- "Apply the card structure to this content"

**For Review:**
- "Run through the UI Review Checklist"
- "Check against the Accessibility Checklist"
- "Apply the Mobile Design Checklist"

---

*This document contains frameworks and concepts from Don't Make Me Think (Steve Krug), Refactoring UI (Adam Wathan & Steve Schoger), and The Design of Everyday Things (Don Norman) for educational reference.*
