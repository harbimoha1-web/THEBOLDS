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

---

# ADVANCED FRAMEWORKS

---

# INTERACTION DESIGN
## Gestures, Microinteractions, Animation & State Management

---

## GESTURE DESIGN FRAMEWORK

### Core Mobile Gestures

| Gesture | Use Case | Feedback Required |
|---------|----------|-------------------|
| **Tap** | Selection, navigation | Immediate visual + optional haptic |
| **Double Tap** | Zoom, like, edit mode | Visual confirmation |
| **Long Press** | Context menu, reorder | Haptic + visual (scale/glow) |
| **Swipe** | Navigation, delete, refresh | Follow finger + reveal action |
| **Pinch** | Zoom in/out | Scale transformation |
| **Pan** | Move, scroll, drag | 1:1 finger tracking |
| **Rotate** | Rotation (photos, maps) | Visual rotation feedback |

### Gesture Design Rules

**1. Discoverability First**
- Every gesture MUST have a visible alternative (button, menu)
- First-time users can't discover hidden gestures
- Use progressive disclosure: show hint after failed attempts

**2. Consistency**
- Same gesture = same action throughout app
- Follow platform conventions (iOS/Android differ!)
- Don't override system gestures

**3. Reversibility**
- Gestures should be undoable
- Swipe to delete → Show undo toast
- Drag to move → Allow return to original

**4. Feedback**
- Visual: Element follows finger, color change
- Haptic: Light/medium/heavy impact feedback
- Audio: Optional confirmation sounds

### Swipe Patterns

**Swipe to Delete (iOS Pattern)**
```
[  Item Content  ] →→→ [Delete Button Reveals]

States:
1. Resting: Item at full width
2. Swiping: Red background reveals proportionally
3. Threshold: Past 50%, snaps to reveal delete
4. Below threshold: Snaps back to resting
5. Deleted: Item slides out, list reflows
```

**Swipe Actions (Multi-action)**
```
←← [Archive] [Delete] [  Item  ] [Star] [Share] →→

Rules:
- Destructive actions: Right side (red)
- Positive actions: Left side (blue/green)
- Max 2-3 actions per side
- Most common action closest to content
```

### Pull to Refresh
```
Pull down ↓
  ↓
[Spinner appears]
  ↓
Release triggers refresh
  ↓
Content updates, spinner dismisses
```

**Timing:**
- Threshold: 60-80px pull distance
- Animation: 0.3s spring back
- Spinner: Show immediately at threshold
- Completion: Fade out over 0.2s

---

## MICROINTERACTIONS

### The Microinteraction Model (Dan Saffer)

```
┌────────────────────────────────────────────────┐
│                MICROINTERACTION                 │
├─────────────┬─────────────┬─────────────┬──────┤
│   TRIGGER   │    RULES    │  FEEDBACK   │ LOOPS│
│             │             │             │ MODE │
│ What starts │ What        │ What user   │ What │
│ it?         │ happens?    │ perceives   │ next?│
└─────────────┴─────────────┴─────────────┴──────┘
```

### Common Microinteractions

**1. Button Press**
```
Trigger: Tap/click
Rules:
  - Scale to 0.95 on press
  - Change background opacity
  - Disable during loading
Feedback:
  - Visual: Scale + color change
  - Haptic: Light impact (mobile)
Loops: Return to resting state on release
```

**2. Toggle Switch**
```
Trigger: Tap
Rules:
  - State flips (on ↔ off)
  - Thumb slides to opposite side
Feedback:
  - Visual: Thumb animation + color change
  - Haptic: Medium impact on state change
Loops: Persist state, sync to server
```

**3. Like Animation (Heart)**
```
Trigger: Double-tap or tap heart
Rules:
  - Toggle like state
  - If liking: Play celebration
Feedback:
  - Visual: Heart scales up (1.3x), particles burst
  - Haptic: Success feedback
Loops: Return to base size, update count
```

**4. Form Validation**
```
Trigger: Field blur or submit
Rules:
  - Validate against criteria
  - Show error if invalid
Feedback:
  - Visual: Red border + error message
  - Position: Error below field
Loops: Re-validate on change, clear error when fixed
```

### Microinteraction Timing Guidelines

| Element | Duration | Easing |
|---------|----------|--------|
| Button state change | 100-150ms | ease-out |
| Toggle switch | 200-300ms | spring |
| Modal appear | 200-250ms | ease-out |
| Modal dismiss | 150-200ms | ease-in |
| Hover state | 100-150ms | ease |
| Skeleton shimmer | 1.5s loop | linear |
| Success checkmark | 300-400ms | spring |
| Error shake | 400ms | ease-in-out |

---

## ANIMATION PRINCIPLES

### 12 Disney Principles Applied to UI

**1. Squash & Stretch**
- Buttons compress on press
- Modals slightly stretch when appearing
- Gives life and elasticity

**2. Anticipation**
- Brief wind-up before main action
- Pull-to-refresh indicator before spinner
- Prepares user for what's coming

**3. Staging**
- Direct attention with motion
- Dim background when modal opens
- Focus on what matters

**4. Straight Ahead vs Pose to Pose**
- UI uses pose-to-pose (keyframes)
- Define start and end states
- Let easing handle the middle

**5. Follow Through & Overlapping Action**
- Elements don't stop together
- Card content settles after card lands
- Creates natural feel

**6. Slow In, Slow Out (Ease)**
- Objects accelerate and decelerate
- Never linear motion for UI
- ease-out for entrances, ease-in for exits

**7. Arc**
- Natural motion follows curves
- Floating action buttons arc to position
- Avoid robotic straight-line motion

**8. Secondary Action**
- Badge bounces when notification arrives
- Icon wiggles in delete mode
- Supports primary action without distracting

**9. Timing**
- Speed communicates character
- Fast = snappy, responsive
- Slow = elegant, important
- Too slow = sluggish

**10. Exaggeration**
- Amplify for clarity
- Error shake is exaggerated
- Don't be subtle with feedback

**11. Solid Drawing (Consistent Design)**
- Maintain visual consistency during motion
- Shadows, colors stay coherent
- No "breaking" of elements

**12. Appeal**
- Motion should feel good
- Avoid jarring, robotic animations
- Aim for delight, not distraction

### Motion Timing Cheat Sheet

```typescript
// React Native / CSS timing
const timing = {
  // Instant feedback
  instant: 50,        // Haptic, micro state changes

  // Quick transitions
  fast: 100,          // Button states, hover

  // Standard UI
  normal: 200,        // Most transitions

  // Deliberate motion
  slow: 300,          // Modals, page transitions

  // Complex sequences
  deliberate: 400,    // Multi-step animations

  // Emphasis
  dramatic: 500,      // Important state changes
};

// Easing curves
const easing = {
  // Entrances (decelerating)
  easeOut: 'cubic-bezier(0, 0, 0.2, 1)',

  // Exits (accelerating)
  easeIn: 'cubic-bezier(0.4, 0, 1, 1)',

  // Symmetric
  easeInOut: 'cubic-bezier(0.4, 0, 0.2, 1)',

  // Bouncy (for emphasis)
  spring: 'cubic-bezier(0.175, 0.885, 0.32, 1.275)',
};
```

---

## STATE TRANSITIONS

### The Five UI States

Every interactive element has five states:

```
┌─────────────────────────────────────────────────────┐
│                    ELEMENT STATES                    │
├──────────┬──────────┬──────────┬──────────┬─────────┤
│  IDEAL   │  EMPTY   │ LOADING  │  ERROR   │ PARTIAL │
│          │          │          │          │         │
│ Content  │ No data  │ Fetching │ Failed   │ Some    │
│ present  │ to show  │ data     │ request  │ data    │
└──────────┴──────────┴──────────┴──────────┴─────────┘
```

### Designing Each State

**1. IDEAL STATE**
- Full content displayed
- Primary use case
- Don't forget this is the goal!

**2. EMPTY STATE**
```
┌──────────────────────────────────────┐
│                                      │
│          [Illustration]              │
│                                      │
│        No messages yet               │
│    Start a conversation with         │
│    someone you know.                 │
│                                      │
│      [ Find People to Chat ]         │
│                                      │
└──────────────────────────────────────┘

Components:
- Illustration or icon
- Headline (what's missing)
- Description (why/what to do)
- CTA (how to fix it)
```

**3. LOADING STATE**

Types of loading indicators:
| Type | Use When | Example |
|------|----------|---------|
| Spinner | Short wait (<3s) | Button submit |
| Skeleton | Content loading | List items |
| Progress bar | Known duration | File upload |
| Shimmer | Card/list loading | Feed items |

**Skeleton Screen Pattern:**
```
┌──────────────────────────────────────┐
│ [████████]  [████████████████████]   │ ← Avatar + Title
│             [████████████]           │ ← Subtitle
├──────────────────────────────────────┤
│ [████████]  [████████████████████]   │
│             [████████████]           │
├──────────────────────────────────────┤
│ [████████]  [████████████████████]   │
│             [████████████]           │
└──────────────────────────────────────┘

Animation: Shimmer effect left-to-right
Color: gray-200 background, gray-300 shimmer
Duration: 1.5s loop
```

**4. ERROR STATE**
```
┌──────────────────────────────────────┐
│                                      │
│          [Error Illustration]        │
│                                      │
│     Something went wrong             │
│   We couldn't load your messages.    │
│   Check your connection and try      │
│   again.                             │
│                                      │
│          [ Try Again ]               │
│                                      │
└──────────────────────────────────────┘

Components:
- Error icon/illustration (not scary)
- What went wrong (plain language)
- Why it might have happened
- How to fix it (actionable CTA)
```

**5. PARTIAL STATE**
- Some data loaded, some failed
- Show what you can
- Indicate what's missing
- Offer retry for failed parts

### State Transition Flow

```
START
  ↓
[Loading] ──→ Success ──→ [Ideal]
    │
    ├──→ Empty ──→ [Empty State]
    │
    └──→ Error ──→ [Error State] ──→ Retry ──→ [Loading]
```

---

## HAPTIC FEEDBACK STRATEGY

### iOS Haptic Types

```typescript
import * as Haptics from 'expo-haptics';

// Impact - Physical feedback
Haptics.impactAsync(Haptics.ImpactFeedbackStyle.Light);   // Subtle
Haptics.impactAsync(Haptics.ImpactFeedbackStyle.Medium);  // Standard
Haptics.impactAsync(Haptics.ImpactFeedbackStyle.Heavy);   // Strong

// Notification - Semantic feedback
Haptics.notificationAsync(Haptics.NotificationFeedbackType.Success);
Haptics.notificationAsync(Haptics.NotificationFeedbackType.Warning);
Haptics.notificationAsync(Haptics.NotificationFeedbackType.Error);

// Selection - For UI changes
Haptics.selectionAsync();
```

### When to Use Haptics

| Action | Haptic Type | Intensity |
|--------|-------------|-----------|
| Button tap | Impact | Light |
| Toggle switch | Impact | Medium |
| Success confirmation | Notification | Success |
| Error/failure | Notification | Error |
| Picker scroll | Selection | - |
| Pull-to-refresh threshold | Impact | Medium |
| Swipe action trigger | Impact | Medium |
| Delete confirmation | Impact | Heavy |
| Long press activation | Impact | Heavy |

### Haptic Guidelines

**DO:**
- Use for significant state changes
- Match intensity to importance
- Be consistent throughout app
- Test on real devices

**DON'T:**
- Overuse (causes fatigue)
- Use for every tap
- Mix styles inconsistently
- Forget users can disable haptics

---

# PERSUASION & CONVERSION DESIGN
## Cialdini's Principles Applied to UI

---

## CIALDINI'S 6 PRINCIPLES

### 1. Reciprocity
**Give first, then ask.**

**In UI:**
- Free trial before payment
- Free valuable content before signup
- Helpful onboarding before asking for permissions
- Give value in empty states

```
✓ DO: "Here's a free template to get started"
        [Download Free Template]

✗ DON'T: "Sign up to see templates"
          [Sign Up Required]
```

### 2. Scarcity
**Limited availability increases desire.**

**In UI:**
- Stock indicators: "Only 3 left"
- Time limits: "Offer ends in 2:34:12"
- Exclusive access: "Limited to first 100 users"
- Waitlists create desire

```
┌────────────────────────────────────┐
│  🔥 Only 3 spots remaining         │
│                                    │
│  [Premium Plan - $99/mo]           │
│                                    │
│  87 people viewing this right now  │
│                                    │
│     [ Claim Your Spot ]            │
└────────────────────────────────────┘

Rules:
- Must be TRUE (fake scarcity damages trust)
- Specific numbers beat vague ("few left")
- Countdown timers create urgency
```

### 3. Authority
**Expertise signals build trust.**

**In UI:**
- Expert endorsements
- Credentials display
- Media logos ("As seen in...")
- Certifications and badges
- Data and statistics

```
┌────────────────────────────────────┐
│  Trusted by 50,000+ companies      │
│                                    │
│  [Google] [Microsoft] [Apple]      │
│                                    │
│  "Best productivity app of 2024"   │
│  - TechCrunch                      │
└────────────────────────────────────┘
```

### 4. Consistency
**People honor their commitments.**

**In UI:**
- Progressive commitment (small ask → big ask)
- Checklists create commitment
- Progress indicators motivate completion
- Defaults set expectations

```
Commitment escalation:
1. Free account (email only)
2. Profile completion (name, photo)
3. First project (invested time)
4. Team invite (social commitment)
5. Paid upgrade (financial commitment)

Each step increases switching cost.
```

### 5. Liking
**We say yes to people we like.**

**In UI:**
- Friendly, conversational copy
- Attractive visual design
- Personalization ("Welcome back, Sarah!")
- Similarity signals
- Compliments and positive feedback

```
✓ "Nice work! You've completed 80% of your profile"
✓ "You're in good company - 10,000 designers like you..."
✗ "Profile incomplete. Add more information."
```

### 6. Consensus (Social Proof)
**We follow what others do.**

**Types of Social Proof:**
| Type | Example | Best For |
|------|---------|----------|
| User count | "Join 1M+ users" | Mass appeal |
| Testimonials | Quotes with photos | Trust building |
| Reviews/Ratings | "4.8 ★ (10K reviews)" | Decision support |
| Real-time activity | "Sarah just purchased..." | Urgency |
| Case studies | Detailed success stories | B2B/high-ticket |
| Logos | Client/media logos | Authority |

```
┌────────────────────────────────────┐
│  ★★★★★ 4.9 out of 5               │
│  Based on 12,847 reviews           │
│                                    │
│  "Changed how we work..."          │
│  - Sarah M., Product Manager       │
│    [Photo]                         │
│                                    │
│  🟢 John from NYC just signed up   │
└────────────────────────────────────┘
```

---

## CTA DESIGN OPTIMIZATION

### CTA Hierarchy

```
PRIMARY CTA    →  Bold, filled, brand color
                  ONE per screen

SECONDARY CTA  →  Outlined or subtle fill
                  Support actions

TERTIARY CTA   →  Text link style
                  Low-priority actions
```

### CTA Copy Rules

**Action-Oriented Language:**
```
✓ "Get Started Free"
✓ "Start My Trial"
✓ "Download Now"
✓ "Claim Your Spot"

✗ "Submit"
✗ "Click Here"
✗ "Continue"
✗ "Next"
```

**First Person vs Second Person:**
```
First person (higher conversion):
"Start my free trial"
"Get my report"
"Create my account"

Second person:
"Start your free trial"
"Get your report"
```

### CTA Button Design

**Size:**
- Mobile: Minimum 48px height
- Desktop: 40-48px height
- Width: At least 120px or full-width on mobile

**Color:**
- Primary: Brand color with strong contrast
- Text: White on dark, dark on light
- Hover: 10-15% darker
- Active: 20% darker

**Placement:**
- Above fold for key actions
- End of content sections
- Sticky for mobile (bottom bar)
- F-pattern and Z-pattern endpoints

### CTA Microcopy

**Reduce Friction:**
```
[Sign Up Free] → "No credit card required"
[Download] → "PDF, 2.3MB"
[Start Trial] → "Cancel anytime"
```

**Create Urgency:**
```
[Get 50% Off] → "Offer ends midnight"
[Reserve Seat] → "Only 12 spots left"
```

---

## LANDING PAGE HIERARCHY

### Above the Fold Formula

```
┌─────────────────────────────────────────────────────┐
│  [Logo]                    [Nav]  [CTA Button]      │
├─────────────────────────────────────────────────────┤
│                                                     │
│  HEADLINE (Value Proposition)                       │
│  One clear benefit in 6-10 words                    │
│                                                     │
│  Subheadline                                        │
│  Support headline with specifics                    │
│                                                     │
│        [ Primary CTA Button ]                       │
│        "No credit card required"                    │
│                                                     │
│  [Hero Image / Video / Product Screenshot]          │
│                                                     │
│  [Logo] [Logo] [Logo] [Logo] - Social proof         │
│                                                     │
└─────────────────────────────────────────────────────┘
```

### Full Page Structure

```
1. HERO (Above fold)
   - Headline + Subhead + CTA + Image + Social proof

2. SOCIAL PROOF BAR
   - Logos, review count, user count

3. PROBLEM/SOLUTION
   - Articulate the pain
   - Present your solution

4. FEATURES/BENEFITS
   - 3-4 key benefits with icons
   - Benefits > Features

5. HOW IT WORKS
   - 3-step process
   - Reduce complexity anxiety

6. TESTIMONIALS
   - Real photos, names, titles
   - Specific results

7. PRICING (if applicable)
   - Clear comparison
   - Highlight recommended plan

8. FAQ
   - Overcome objections
   - Address concerns

9. FINAL CTA
   - Repeat main value prop
   - Urgency element
   - Trust signals

10. FOOTER
    - Links, legal, contact
```

---

## FORM CONVERSION OPTIMIZATION

### Form Design Rules

**1. Minimize Fields**
```
Every field reduces completion by ~5-10%

Essential only:
✓ Email
✓ Password

Nice to have (ask later):
- Name (can derive from email)
- Company (ask in onboarding)
- Phone (only if required)
```

**2. Single Column Layout**
```
✓ One field per row
✓ Labels above inputs
✓ Full-width on mobile

✗ Multiple columns
✗ Side-by-side fields
✗ Inline labels
```

**3. Smart Defaults & Autofill**
```
- Pre-fill country from IP
- Enable browser autofill (correct autocomplete attributes)
- Remember previous entries
- Default to most common choice
```

**4. Progressive Disclosure**
```
Step 1: Email only
   ↓
Step 2: Password
   ↓
Step 3: Profile (after signup)

Show one thing at a time.
Progress indicator builds commitment.
```

**5. Real-Time Validation**
```
✓ Validate on blur (when leaving field)
✓ Clear error when user starts fixing
✓ Show success state when valid
✓ Specific error messages

✗ Validate only on submit
✗ Generic "Invalid" errors
✗ Clear field on error
```

**6. Mobile Optimization**
```
- Correct keyboard type (email, phone, number)
- Large touch targets (48px)
- Avoid date pickers when text works
- Show/hide password toggle
```

### Form Microcopy

**Labels:**
```
✓ "Email address" (clear)
✓ "Create a password" (action-oriented)

✗ "Email" (ambiguous)
✗ "Password" (passive)
```

**Placeholders:**
```
- Use as hints, not labels
- Disappear on focus (accessibility issue)
- Format examples: "you@example.com"
```

**Error Messages:**
```
✓ "Please enter a valid email address (example: you@company.com)"
✗ "Invalid email"

✓ "Password must be at least 8 characters"
✗ "Password too short"
```

**Help Text:**
```
Below field, smaller gray text:
"We'll never share your email with anyone else."
"Use 8+ characters with a mix of letters and numbers."
```

---

# ADVANCED ACCESSIBILITY (WCAG 2.2)
## Complete Guidelines for Inclusive Design

---

## WCAG 2.2 OVERVIEW

### The Four Principles (POUR)

```
┌──────────────────────────────────────────────────────┐
│                    WCAG PRINCIPLES                    │
├─────────────┬──────────────┬─────────────┬───────────┤
│ PERCEIVABLE │  OPERABLE    │ UNDERSTAND- │  ROBUST   │
│             │              │    ABLE     │           │
│ Can users   │ Can users    │ Can users   │ Works     │
│ perceive    │ operate the  │ understand  │ with      │
│ the info?   │ interface?   │ the info?   │ all tech? │
└─────────────┴──────────────┴─────────────┴───────────┘
```

### Conformance Levels

| Level | Meaning | Target |
|-------|---------|--------|
| **A** | Minimum | Must meet |
| **AA** | Standard | Should meet (legal requirement) |
| **AAA** | Enhanced | Nice to have |

---

## PERCEIVABLE

### Text Alternatives (1.1)

**Images:**
```html
<!-- Informative image -->
<img src="chart.png" alt="Sales increased 40% from Q1 to Q2">

<!-- Decorative image -->
<img src="decoration.png" alt="" role="presentation">

<!-- Complex image -->
<img src="diagram.png" alt="Network architecture" aria-describedby="diagram-desc">
<p id="diagram-desc">Detailed description of the network...</p>
```

**Icons:**
```html
<!-- Icon with meaning -->
<button aria-label="Close dialog">
  <svg aria-hidden="true">...</svg>
</button>

<!-- Icon as decoration -->
<span aria-hidden="true">🎉</span>
```

### Color Contrast (1.4.3, 1.4.6)

| Content Type | AA Minimum | AAA Enhanced |
|--------------|------------|--------------|
| Normal text (<18px) | 4.5:1 | 7:1 |
| Large text (≥18px or 14px bold) | 3:1 | 4.5:1 |
| UI components | 3:1 | - |
| Graphical objects | 3:1 | - |

**Tools:**
- WebAIM Contrast Checker
- Stark (Figma plugin)
- Color Oracle (simulator)

### Don't Rely on Color Alone (1.4.1)

```
✗ Red = error, Green = success (color only)

✓ 🔴 Red + "Error" label + icon
✓ 🟢 Green + "Success" label + checkmark
```

**For links:**
```css
/* Color + underline */
a {
  color: #2563EB;
  text-decoration: underline;
}

/* Or significant contrast difference */
a {
  color: #2563EB; /* 3:1 contrast with surrounding text */
  text-decoration: none;
}
a:hover, a:focus {
  text-decoration: underline;
}
```

### Text Spacing (1.4.12)

Must be readable with these overrides:
- Line height: 1.5x font size
- Paragraph spacing: 2x font size
- Letter spacing: 0.12x font size
- Word spacing: 0.16x font size

**Test:** Use browser extension to apply these styles.

---

## OPERABLE

### Keyboard Navigation (2.1)

**All functionality must work with keyboard:**

| Key | Action |
|-----|--------|
| Tab | Move to next focusable element |
| Shift+Tab | Move to previous |
| Enter/Space | Activate buttons/links |
| Arrow keys | Navigate within components |
| Escape | Close modals, cancel |

**Focus Order:**
```
1. Logical reading order (top-to-bottom, left-to-right)
2. Skip links at top
3. Tab through interactive elements in order
4. Modal focus trapped within modal
5. Focus returns when modal closes
```

**Focus Indicators:**
```css
/* Default - visible focus ring */
:focus {
  outline: 2px solid #2563EB;
  outline-offset: 2px;
}

/* Remove only if custom indicator provided */
:focus {
  outline: none;
  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.5);
}
```

### Target Size (2.5.5, 2.5.8)

**WCAG 2.2 requirements:**
- **AA:** 24x24px minimum (or exceptions apply)
- **AAA:** 44x44px minimum

**Best practice for mobile:** 48x48px

```css
.touch-target {
  min-width: 44px;
  min-height: 44px;
  padding: 12px; /* Expand hit area beyond visible bounds */
}
```

**Spacing between targets:**
- At least 8px between adjacent targets
- Or make targets larger

### Skip Links (2.4.1)

```html
<body>
  <a href="#main-content" class="skip-link">
    Skip to main content
  </a>

  <nav>...</nav>

  <main id="main-content">
    ...
  </main>
</body>
```

```css
.skip-link {
  position: absolute;
  top: -40px;
  left: 0;
  padding: 8px;
  background: #000;
  color: #fff;
  z-index: 100;
}

.skip-link:focus {
  top: 0;
}
```

### Timing (2.2)

**Session Timeouts:**
- Warn before timeout (at least 20 seconds notice)
- Allow extension
- Provide option to disable timeout

**Moving/Blinking Content:**
- Auto-updating content: pause/stop controls
- Animations: respect `prefers-reduced-motion`

```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation: none !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## UNDERSTANDABLE

### Language (3.1)

```html
<html lang="en">
  <!-- Primary language -->

  <p>Welcome! <span lang="ar">مرحبا</span></p>
  <!-- Language changes -->
</html>
```

### Predictable (3.2)

**No unexpected changes:**
- Focus doesn't trigger major changes
- Input doesn't auto-submit
- Navigation consistent across pages

**Consistent identification:**
- Same icon = same meaning
- Same term = same function
- Same pattern = same behavior

### Error Handling (3.3)

**Input Error Identification (3.3.1):**
```
✓ Identify which field has error
✓ Describe the error in text
✓ Don't rely on color alone

Error example:
[Email field - red border]
"Please enter a valid email address. Example: name@company.com"
```

**Labels/Instructions (3.3.2):**
```html
<label for="email">Email address (required)</label>
<input type="email" id="email" required aria-describedby="email-hint">
<span id="email-hint">We'll send your receipt to this address</span>
```

**Error Suggestion (3.3.3):**
```
Instead of: "Invalid date"
Say: "Please enter date as MM/DD/YYYY"
```

**Error Prevention (3.3.4):**
For legal/financial submissions:
1. Reversible (can undo)
2. Checked (validate before submit)
3. Confirmed (review before final submit)

---

## SCREEN READER PATTERNS

### Semantic HTML First

```html
<!-- Use native elements -->
<button>Click me</button>      ✓
<div onclick="...">Click</div> ✗

<nav>...</nav>                  ✓
<div class="nav">...</div>     ✗

<main>...</main>               ✓
<div class="main">...</div>    ✗
```

### ARIA Landmarks

```html
<header role="banner">...</header>
<nav role="navigation">...</nav>
<main role="main">...</main>
<aside role="complementary">...</aside>
<footer role="contentinfo">...</footer>
```

### ARIA Labels

```html
<!-- Invisible label -->
<button aria-label="Close dialog">
  <svg>X icon</svg>
</button>

<!-- Reference visible text -->
<div id="dialog-title">Settings</div>
<div role="dialog" aria-labelledby="dialog-title">
  ...
</div>

<!-- Describe the element -->
<input aria-describedby="password-requirements">
<div id="password-requirements">
  Password must be 8+ characters
</div>
```

### Live Regions

```html
<!-- Announce changes -->
<div aria-live="polite">
  <!-- Dynamic content updates here -->
  3 items in cart
</div>

<!-- Urgent announcements -->
<div aria-live="assertive">
  Error: Payment failed
</div>

<!-- Status messages -->
<div role="status">
  File uploaded successfully
</div>
```

### Forms

```html
<form>
  <div>
    <label for="name">Full name</label>
    <input
      type="text"
      id="name"
      aria-required="true"
      aria-invalid="false"
    >
  </div>

  <fieldset>
    <legend>Notification preferences</legend>
    <label>
      <input type="checkbox" name="email-notif">
      Email notifications
    </label>
    <label>
      <input type="checkbox" name="sms-notif">
      SMS notifications
    </label>
  </fieldset>

  <button type="submit">Save changes</button>
</form>
```

---

## COGNITIVE ACCESSIBILITY

### Principles

**1. Clear Language**
- Simple words over complex
- Short sentences
- Avoid jargon
- Define technical terms

**2. Predictable Interface**
- Consistent navigation
- Consistent behavior
- No surprises
- Clear affordances

**3. Focus Support**
- One task at a time
- Clear progress indicators
- Save state automatically
- Minimize distractions

**4. Memory Support**
- Don't require memorization
- Show instructions where needed
- Persistent help access
- Copy-paste friendly

### Implementation

**Error Prevention:**
```
- Confirm destructive actions
- Undo capability
- Auto-save drafts
- Clear validation before submit
```

**Orientation:**
```
- Breadcrumbs
- Clear page titles
- Progress indicators
- Section headings
```

**Time & Pressure:**
```
- No time limits when possible
- Extend time limits
- Save progress automatically
- Don't auto-advance
```

---

# DESIGN SYSTEMS MATURITY
## Tokens, Components, and Theming

---

## DESIGN TOKEN ARCHITECTURE

### What are Design Tokens?

Design tokens are the atomic values of your design system:
- Colors, spacing, typography stored as variables
- Single source of truth
- Platform-agnostic

### Token Hierarchy

```
┌─────────────────────────────────────────────────────┐
│                    TOKEN LEVELS                      │
├─────────────────────────────────────────────────────┤
│                                                      │
│  PRIMITIVE TOKENS (Raw values)                      │
│  ├── blue-500: #3B82F6                              │
│  ├── space-4: 16px                                  │
│  └── font-size-md: 16px                             │
│                    ↓                                 │
│  SEMANTIC TOKENS (Purpose-based)                    │
│  ├── color-primary: {blue-500}                      │
│  ├── color-error: {red-500}                         │
│  ├── spacing-component: {space-4}                   │
│  └── text-body: {font-size-md}                      │
│                    ↓                                 │
│  COMPONENT TOKENS (Specific to component)           │
│  ├── button-bg: {color-primary}                     │
│  ├── button-padding: {spacing-component}            │
│  └── input-text: {text-body}                        │
│                                                      │
└─────────────────────────────────────────────────────┘
```

### Token File Structure

```
tokens/
├── primitives/
│   ├── colors.json
│   ├── spacing.json
│   ├── typography.json
│   └── shadows.json
├── semantic/
│   ├── colors.json      (maps primitives to meaning)
│   ├── spacing.json
│   └── typography.json
├── components/
│   ├── button.json
│   ├── input.json
│   └── card.json
└── themes/
    ├── light.json
    └── dark.json
```

### Token Naming Convention

```
[category]-[property]-[variant]-[state]

Examples:
color-background-primary
color-text-secondary
spacing-padding-sm
border-radius-md
shadow-elevation-high
font-size-heading-xl
```

### Token Implementation

```typescript
// tokens.ts
export const primitives = {
  color: {
    blue: {
      50: '#EFF6FF',
      100: '#DBEAFE',
      500: '#3B82F6',
      600: '#2563EB',
      900: '#1E3A8A',
    },
    gray: {
      50: '#F9FAFB',
      100: '#F3F4F6',
      500: '#6B7280',
      900: '#111827',
    },
  },
  spacing: {
    0: 0,
    1: 4,
    2: 8,
    3: 12,
    4: 16,
    6: 24,
    8: 32,
  },
};

export const semantic = {
  color: {
    primary: primitives.color.blue[500],
    primaryHover: primitives.color.blue[600],
    background: primitives.color.gray[50],
    text: primitives.color.gray[900],
    textSecondary: primitives.color.gray[500],
  },
  spacing: {
    xs: primitives.spacing[1],
    sm: primitives.spacing[2],
    md: primitives.spacing[4],
    lg: primitives.spacing[6],
    xl: primitives.spacing[8],
  },
};

export const components = {
  button: {
    background: semantic.color.primary,
    backgroundHover: semantic.color.primaryHover,
    padding: `${semantic.spacing.sm}px ${semantic.spacing.md}px`,
    borderRadius: 8,
  },
};
```

---

## COMPONENT API DESIGN

### Component Interface Principles

**1. Minimal Required Props**
```typescript
// ✓ Good - works with minimal config
<Button>Click me</Button>

// ✗ Bad - requires too much
<Button
  variant="primary"
  size="medium"
  onClick={fn}
  type="button"
>
  Click me
</Button>
```

**2. Sensible Defaults**
```typescript
interface ButtonProps {
  variant?: 'primary' | 'secondary' | 'ghost';  // default: 'primary'
  size?: 'sm' | 'md' | 'lg';                    // default: 'md'
  disabled?: boolean;                            // default: false
  loading?: boolean;                             // default: false
  fullWidth?: boolean;                           // default: false
  children: React.ReactNode;
  onPress?: () => void;
}
```

**3. Consistent Prop Names**
```typescript
// Use same props across components
size: 'sm' | 'md' | 'lg'           // Not: small/medium/large elsewhere
variant: 'primary' | 'secondary'    // Not: type, kind, style
disabled: boolean                   // Not: isDisabled
loading: boolean                    // Not: isLoading, showSpinner
```

**4. Composition Over Configuration**
```typescript
// ✓ Compose simple components
<Card>
  <CardHeader>
    <CardTitle>Title</CardTitle>
  </CardHeader>
  <CardBody>Content</CardBody>
  <CardFooter>
    <Button>Action</Button>
  </CardFooter>
</Card>

// ✗ Mega-component with tons of props
<Card
  title="Title"
  body="Content"
  footerButton="Action"
  footerButtonVariant="primary"
  headerIcon="settings"
  ...
/>
```

### Component Documentation Template

```markdown
# Button

Primary action trigger for user interactions.

## Usage

\`\`\`tsx
import { Button } from '@design-system/components';

<Button variant="primary" onPress={handlePress}>
  Submit
</Button>
\`\`\`

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| variant | 'primary' \| 'secondary' \| 'ghost' | 'primary' | Visual style |
| size | 'sm' \| 'md' \| 'lg' | 'md' | Button size |
| disabled | boolean | false | Disable interaction |
| loading | boolean | false | Show loading spinner |
| fullWidth | boolean | false | Expand to container width |
| children | ReactNode | required | Button content |
| onPress | () => void | - | Press handler |

## Examples

### Variants
[Visual examples of each variant]

### Sizes
[Visual examples of each size]

### States
[Visual examples: default, hover, pressed, disabled, loading]

## Accessibility

- Uses native `<Pressable>` for touch handling
- Supports keyboard navigation
- Loading state disables button and announces to screen readers
- Minimum touch target: 44x44px

## Design Tokens

- `button.background.primary`
- `button.background.secondary`
- `button.text.primary`
- `button.padding.sm/md/lg`
- `button.borderRadius`
```

---

## THEMING STRATEGY

### Theme Structure

```typescript
// themes/types.ts
interface Theme {
  colors: {
    primary: string;
    primaryHover: string;
    background: string;
    surface: string;
    text: string;
    textSecondary: string;
    border: string;
    error: string;
    success: string;
    warning: string;
  };
  spacing: {
    xs: number;
    sm: number;
    md: number;
    lg: number;
    xl: number;
  };
  typography: {
    fontFamily: string;
    sizes: { /* ... */ };
    weights: { /* ... */ };
  };
  shadows: {
    sm: object;
    md: object;
    lg: object;
  };
  borderRadius: {
    sm: number;
    md: number;
    lg: number;
    full: number;
  };
}
```

### Light/Dark Themes

```typescript
// themes/light.ts
export const lightTheme: Theme = {
  colors: {
    primary: '#3B82F6',
    primaryHover: '#2563EB',
    background: '#FFFFFF',
    surface: '#F9FAFB',
    text: '#111827',
    textSecondary: '#6B7280',
    border: '#E5E7EB',
    error: '#EF4444',
    success: '#10B981',
    warning: '#F59E0B',
  },
  // ...
};

// themes/dark.ts
export const darkTheme: Theme = {
  colors: {
    primary: '#60A5FA',          // Lighter for dark bg
    primaryHover: '#93C5FD',
    background: '#111827',
    surface: '#1F2937',
    text: '#F9FAFB',
    textSecondary: '#9CA3AF',
    border: '#374151',
    error: '#F87171',
    success: '#34D399',
    warning: '#FBBF24',
  },
  // ...
};
```

### Theme Context (React Native)

```typescript
// ThemeProvider.tsx
import React, { createContext, useContext, useState } from 'react';
import { lightTheme, darkTheme, Theme } from './themes';

interface ThemeContextType {
  theme: Theme;
  isDark: boolean;
  toggleTheme: () => void;
}

const ThemeContext = createContext<ThemeContextType | undefined>(undefined);

export function ThemeProvider({ children }: { children: React.ReactNode }) {
  const [isDark, setIsDark] = useState(false);

  const toggleTheme = () => setIsDark(!isDark);
  const theme = isDark ? darkTheme : lightTheme;

  return (
    <ThemeContext.Provider value={{ theme, isDark, toggleTheme }}>
      {children}
    </ThemeContext.Provider>
  );
}

export function useTheme() {
  const context = useContext(ThemeContext);
  if (!context) throw new Error('useTheme must be within ThemeProvider');
  return context;
}

// Usage in components
function Card({ children }) {
  const { theme } = useTheme();

  return (
    <View style={{
      backgroundColor: theme.colors.surface,
      borderRadius: theme.borderRadius.md,
      padding: theme.spacing.md,
    }}>
      {children}
    </View>
  );
}
```

### Dark Mode Design Considerations

**Colors:**
- Don't just invert: pure white on pure black is harsh
- Use dark grays instead of pure black (#121212 not #000000)
- Reduce contrast slightly (avoid pure white text)
- Saturate colors less on dark backgrounds

**Elevation:**
- Light mode: shadows show elevation
- Dark mode: lighter surfaces show elevation
- Each elevation level = slightly lighter gray

```typescript
// Dark mode elevation colors
const darkElevation = {
  0: '#121212',   // Background
  1: '#1E1E1E',   // Card
  2: '#232323',   // Raised card
  3: '#272727',   // Modal
  4: '#2C2C2C',   // Dropdown
};
```

**Imagery:**
- Consider slightly reducing image brightness
- Use semitransparent overlays if needed
- Dark mode icons may need adjustment

---

# RESEARCH METHODS FOR DESIGNERS
## Usability Testing, A/B Design & User Research

---

## USABILITY TESTING PROTOCOLS

### Moderated Testing (Live)

**Setup:**
- Quiet room with computer/device
- Screen + face recording
- Observer notes template
- Task scenarios

**Process:**
```
1. WELCOME (5 min)
   - Introduce yourself
   - Explain: "We're testing the design, not you"
   - Get consent for recording
   - Ask background questions

2. TASKS (30-40 min)
   - Present one task at a time
   - "Please think aloud as you work"
   - Don't help or lead
   - Ask probing questions: "What did you expect?"

3. DEBRIEF (10 min)
   - Overall impressions
   - What was easy/hard?
   - Any suggestions?
   - Thank and compensate
```

**Task Design:**
```
✓ Good task: "You want to add a new team member. Please show me how you would do that."

✗ Bad task: "Click the Add button in the top right to add a team member."

Good tasks:
- Realistic scenario
- Goal-oriented (not step-by-step)
- No UI terminology
- Specific enough to measure success
```

**Probing Questions:**
- "What are you thinking right now?"
- "What do you expect to happen if you click that?"
- "Is this what you expected to see?"
- "Where would you look for X?"
- "On a scale of 1-5, how confident are you?"

### Unmoderated Testing (Remote)

**Platforms:** UserTesting, Maze, Lookback, UsabilityHub

**Best For:**
- Large sample sizes
- Quick turnaround
- Geographic diversity
- Budget constraints

**Limitations:**
- No follow-up questions
- Tasks must be very clear
- Can't course-correct
- Less depth

**Writing Unmoderated Tasks:**
```
Be extremely specific:

"Imagine you're looking for a restaurant that's open now
and has good reviews. Starting from this screen, find a
Thai restaurant within 2 miles of your location and make
a reservation for 2 people tonight at 7pm."

Include:
- Context/scenario
- Specific goal
- Success criteria
```

### Analysis Template

```markdown
## Usability Test Report

### Overview
- Date: [Date]
- Participants: [Number]
- Device: [Mobile/Desktop]
- Build tested: [Version]

### Task Completion

| Task | Success | Partial | Fail | Avg Time |
|------|---------|---------|------|----------|
| Task 1 | 4 | 1 | 0 | 45s |
| Task 2 | 2 | 2 | 1 | 2:30 |

### Key Findings

**Critical Issues (Must Fix)**
1. [Issue] - 4/5 participants struggled
   - Evidence: [Quote/observation]
   - Recommendation: [Solution]

**Major Issues (Should Fix)**
1. [Issue] - 3/5 participants affected
   ...

**Minor Issues (Nice to Fix)**
1. [Issue] - 1-2 participants affected
   ...

### Recommendations
Prioritized list of changes
```

---

## A/B TEST DESIGN FOR DESIGNERS

### What to Test

**High Impact:**
- Headlines and value props
- CTA button text, color, placement
- Form length and field order
- Page layout and hierarchy
- Pricing presentation
- Onboarding flow

**Lower Impact (but still worth testing):**
- Icon choices
- Image selection
- Color variations
- Microcopy
- Animation presence

### Test Design Principles

**1. One Variable at a Time**
```
✓ Test: Button color only (blue vs green)
✗ Test: Button color AND text AND size

If multiple things change, you don't know what caused the difference.
```

**2. Meaningful Difference**
```
✓ Test: "Start Free Trial" vs "Get Started Free"
✗ Test: "Start Free Trial" vs "Start free trial"

Test things different enough to potentially matter.
```

**3. Measure What Matters**
```
Primary metric: The ONE thing you're trying to improve
- Signup rate
- Purchase completion
- Feature adoption

Secondary metrics: Watch for negative effects
- Bounce rate
- Time on page
- Support tickets
```

### Design Documentation for A/B Tests

```markdown
## A/B Test: Pricing Page Redesign

### Hypothesis
If we simplify the pricing page to show 2 plans instead of 4,
then more users will start a trial because of reduced choice paralysis.

### Control (A)
[Screenshot of current 4-plan layout]

### Variant (B)
[Screenshot of proposed 2-plan layout]

### Metrics
- Primary: Trial start rate
- Secondary: Time to decision, Plan selection distribution

### Sample Size Needed
~5,000 visitors per variant (calculated for 80% power, 5% significance)

### Duration
Estimated 2 weeks

### Segment
New visitors only (returning users see control)
```

---

## USER INTERVIEW TECHNIQUES

### Planning Interviews

**Research Questions → Interview Questions**
```
Research question: Why do users abandon checkout?

Interview questions:
- "Tell me about the last time you bought something online."
- "Walk me through what happened when you were shopping."
- "What made you decide to buy/not buy?"
- "What would have made that easier?"
```

### Interview Guide Template

```markdown
## Interview Guide: [Topic]

### Intro (5 min)
- Introduce yourself and purpose
- "No right or wrong answers"
- Permission to record

### Warm-up (5 min)
- Background questions
- Establish rapport

### Main Questions (30 min)

**Opening:**
"Tell me about the last time you..."

**Deep Dive:**
"Can you walk me through what happened?"
"What were you thinking at that point?"
"How did that make you feel?"

**Specific Topics:**
[Topic 1 questions]
[Topic 2 questions]

**Reactions to Concept:**
[Show prototype/concept]
"What are your first impressions?"
"What questions do you have?"

### Wrap-up (5 min)
"Is there anything else you'd like to share?"
"Any questions for me?"

### Probes to Have Ready
- "Tell me more about that."
- "Why was that important?"
- "What do you mean by [term]?"
- "Can you give me an example?"
```

### Interview Best Practices

**DO:**
- Ask open-ended questions
- Let silences happen (people will fill them)
- Follow interesting threads
- Ask "why" multiple times
- Take notes on emotions, not just facts

**DON'T:**
- Ask leading questions
- Suggest answers
- Fill silences immediately
- Defend your design
- Ask about future behavior ("Would you use this?")

```
✓ "What happened next?"
✗ "Did you find it confusing?"

✓ "How did you feel about that?"
✗ "That must have been frustrating, right?"

✓ "Tell me about how you currently do this."
✗ "Would you use a feature that does X?"
```

---

## HEAT MAPPING & ANALYTICS

### Heat Map Types

**Click/Tap Maps:**
- Where users click/tap
- Identify: Popular areas, dead clicks, missed CTAs

**Scroll Maps:**
- How far users scroll
- Identify: Content below fold, drop-off points

**Move/Hover Maps:**
- Where cursor moves (desktop)
- Indicates: Attention, reading patterns

**Attention Maps:**
- Eye tracking or gaze prediction
- Shows: What users actually look at

### Interpreting Heat Maps

**High Activity (Hot):**
- Users interacting here
- If on CTA: Good
- If on non-clickable: Bad (false affordance)

**Low Activity (Cold):**
- Users ignoring this area
- Important content cold? Move it up
- Non-essential content cold? Maybe remove

**Patterns to Look For:**
```
✓ Hot spots on CTAs → Working as intended
✓ Scroll depth past key content → Good placement

✗ Clicks on non-clickable elements → Add affordance or make clickable
✗ 70% drop-off before seeing CTA → Move CTA up
✗ Hot spots on decorative elements → Wasted attention
```

### Combining Quant + Qual

```
Quantitative (What):
- Heat maps show WHERE users click
- Analytics show HOW MANY complete tasks
- A/B tests show WHICH version wins

Qualitative (Why):
- User interviews explain WHY they clicked there
- Usability tests show WHERE they get confused
- Open feedback tells you WHAT they want
```

---

# RTL & LOCALIZATION DESIGN
## Arabic-First Design Patterns

---

## RTL FUNDAMENTALS

### What Flips, What Doesn't

**DOES Mirror (RTL):**
- Reading direction (right-to-left)
- Layout direction (sidebar on right)
- Navigation order
- Progress indicators
- Checkmarks (typically)
- Back/forward arrows
- Sliders
- Text alignment (default right)

**DOESN'T Mirror:**
- Clock direction (always clockwise)
- Video playback controls (play/pause universal)
- Music notes (inherently directional)
- Phone icons (handset shape)
- Check marks (sometimes kept LTR)
- Brand logos
- Images with text baked in (need new assets)

### Layout Mirroring

```
LTR Layout:
┌──────────────────────────────────────────┐
│ [Logo]    [Nav]              [Search] [☰] │
├──────────────────────────────────────────┤
│ [Sidebar]  │    Main Content             │
│            │                             │
│            │                             │
└──────────────────────────────────────────┘

RTL Layout:
┌──────────────────────────────────────────┐
│ [☰] [Search]              [Nav]    [Logo] │
├──────────────────────────────────────────┤
│             Main Content   │  [Sidebar]  │
│                           │             │
│                           │             │
└──────────────────────────────────────────┘
```

### Icon Direction

```
Icons that SHOULD flip:
←  →    Arrows (back/forward)
📖      Book/magazine (spine position)
💬      Chat bubble (tail direction)
🔍      Search (if includes text lines)
📝      Notepad with lines
↩️      Reply arrow
📤📥    Send/receive

Icons that SHOULDN'T flip:
✓      Checkmark (universal)
⏯️      Play/pause (universal)
⏰      Clock (clockwise is universal)
📞      Phone (shape doesn't change)
🎵      Music note
📷      Camera
```

### CSS for RTL

```css
/* Use logical properties instead of directional */

/* Instead of: */
margin-left: 16px;
padding-right: 8px;
text-align: left;
float: left;

/* Use: */
margin-inline-start: 16px;
padding-inline-end: 8px;
text-align: start;
float: inline-start;

/* CSS direction */
html[dir="rtl"] {
  direction: rtl;
}

/* Component-level override */
.ltr-always {
  direction: ltr;
}
```

### React Native RTL

```typescript
import { I18nManager, StyleSheet } from 'react-native';

// Force RTL (usually done based on language)
I18nManager.forceRTL(true);
I18nManager.allowRTL(true);

// Check direction
const isRTL = I18nManager.isRTL;

// Styles that auto-flip
const styles = StyleSheet.create({
  container: {
    flexDirection: 'row',      // Auto-flips in RTL
    paddingStart: 16,          // Logical property
    marginEnd: 8,              // Logical property
  },
});

// Explicit non-flipping (if needed)
const noFlipStyles = StyleSheet.create({
  mediaControls: {
    flexDirection: 'row',
    transform: [{ scaleX: I18nManager.isRTL ? -1 : 1 }],  // Force LTR
  },
});
```

---

## ARABIC TYPOGRAPHY

### Font Selection

**Arabic-Optimized Fonts:**
- **Noto Sans Arabic** - Google, excellent coverage
- **Cairo** - Modern, geometric
- **Tajawal** - Clean, good for UI
- **IBM Plex Arabic** - Professional
- **Dubai** - Microsoft, widely available

**Font Pairing:**
```css
font-family: 'Cairo', 'SF Pro Display', sans-serif;
/* Arabic font first, falls back to Latin */
```

### Typography Adjustments

**Line Height:**
- Arabic typically needs more line height
- 1.7-1.8 instead of 1.5

**Letter Spacing:**
- Don't add letter-spacing to Arabic
- Arabic letters connect, spacing breaks words

**Font Size:**
- Arabic may appear smaller at same point size
- Consider 10-15% larger for Arabic

```css
/* Responsive to language */
:lang(ar) {
  font-size: 1.1em;      /* Slightly larger */
  line-height: 1.8;      /* More space */
  letter-spacing: 0;     /* Never add spacing */
}
```

### Bidirectional Text (BiDi)

When mixing Arabic and English:

```html
<!-- Use unicode-bidi and direction -->
<p dir="rtl">
  هذا نص عربي مع <span dir="ltr">English text</span> في المنتصف
</p>
```

**Numbers in Arabic context:**
```
Arabic text ١٢٣ Arabic text  (Arabic numerals)
Arabic text 123 Arabic text  (Western numerals - commonly used)

Both are acceptable. Be consistent within app.
```

---

## CULTURAL CONSIDERATIONS

### Color Meanings

| Color | Western | Arabic/Islamic |
|-------|---------|----------------|
| Green | Go, nature, money | Islam, prosperity, paradise |
| White | Purity, weddings | Mourning (some contexts) |
| Black | Mourning, elegance | Elegance, formality |
| Red | Danger, passion | Danger (universal) |
| Blue | Trust, calm | Evil eye protection, trust |
| Gold | Luxury | Luxury, prestige, important |

**Implications:**
- Green is very positive in Arabic contexts
- White for mourning may affect some design choices
- Gold accents resonate strongly

### Imagery Guidelines

**DO:**
- Include Arab representation
- Show appropriate dress (can be modern but mindful)
- Family-friendly imagery
- Show both genders (with cultural awareness)

**DON'T:**
- Images with alcohol prominently featured
- Overly revealing clothing
- Left hand for important actions (culturally)
- Dogs in prominent positive contexts (varies by region)
- Images that could be seen as religiously insensitive

### Date & Time

**Calendar:**
- Gregorian is common in business
- Hijri calendar for religious dates
- Some users prefer Hijri for personal use

**Date Format:**
```
Gregorian: DD/MM/YYYY (not MM/DD/YYYY)
Hijri: DD/MM/YYYY هـ

Example:
25/03/2024
15/09/1445 هـ
```

**Week Start:**
- Some countries: Sunday
- Some countries: Saturday
- Allow configuration if calendar features

---

# ADVANCED DESIGN PATTERNS
## Information Architecture, Progressive Disclosure & More

---

## INFORMATION ARCHITECTURE

### Card Sorting

**Open Card Sort:**
- Users group items into categories
- Users name the categories
- Reveals natural mental models

**Closed Card Sort:**
- Users place items into predefined categories
- Tests if your categories make sense

**Hybrid:**
- Predefined categories but users can create new ones

**Analysis:**
```
1. Similarity matrix: How often items grouped together
2. Dendrogram: Hierarchical clustering visualization
3. Outliers: Items that don't fit anywhere
4. Category names: User language vs your language
```

### Tree Testing

Test your hierarchy without design influence:

```
Task: "Find how to change your password"

Tree:
├── Profile
│   ├── Personal Info
│   └── Settings ← Expected path
│       └── Change Password ← Target
├── Security
│   └── Privacy Settings
└── Help
    └── Account Help
```

**Metrics:**
- Success rate: Found correct location
- Directness: Went straight there (no backtracking)
- Time: How long to find it

### Navigation Patterns

**Flat Navigation:**
```
[Tab 1] [Tab 2] [Tab 3] [Tab 4] [Tab 5]
       Main content area
```
- Max 5 items
- Equal importance
- Quick switching

**Hierarchical:**
```
Home > Category > Subcategory > Item
```
- Deep content structures
- Clear location indication
- May need search for deep items

**Hub and Spoke:**
```
        ┌──────┐
        │ Hub  │
        └──────┘
       ↙   ↓   ↘
   Spoke  Spoke  Spoke
```
- Return to hub between sections
- Good for distinct task areas
- Used in: iOS Settings, many dashboards

**Nested Doll:**
```
Screen 1 → Screen 2 → Screen 3 → Screen 4
    ←          ←          ←
```
- Linear, sequential flow
- Good for wizards, onboarding
- Clear back navigation

---

## PROGRESSIVE DISCLOSURE

### The Principle

**Show only what's needed, when it's needed.**

Reduce cognitive load by hiding complexity until relevant.

### Patterns

**1. Read More / Show More**
```
Article summary text that gives an overview...
[Read more]

─── After click ───

Full article text with all the details...
[Show less]
```

**2. Accordion**
```
▶ Section 1
  └─ [Hidden content]
▼ Section 2 (expanded)
  └─ Visible content here
▶ Section 3
  └─ [Hidden content]
```

**3. Tooltips / Popovers**
```
Label [?]
       └─ More information appears on hover/tap
```

**4. Stepped Flow**
```
Step 1 of 3: Basic Info
[Name field]
[Email field]
[Next →]

────

Step 2 of 3: Details
[Additional fields revealed]
[← Back] [Next →]
```

**5. Advanced Settings**
```
Basic settings visible by default

[Show Advanced ▼]
  └─ Power user options hidden until requested
```

### When to Use

**Progressive Disclosure IS good for:**
- Complex forms with optional fields
- Expert settings most users don't need
- Long content that can be summarized
- Secondary information

**Progressive Disclosure is NOT good for:**
- Critical information users need to see
- Primary navigation
- Legal/required information
- Error messages

---

## EMPTY STATES THAT CONVERT

### Empty State Components

```
┌──────────────────────────────────────────┐
│                                          │
│         [Illustration/Icon]              │  ← Visual (friendly, on-brand)
│                                          │
│         Title (What's missing)           │  ← Headline
│                                          │
│   Brief explanation of why it's empty    │  ← Description
│   and what value they'll get when it's   │
│   populated.                             │
│                                          │
│         [ Primary Action ]               │  ← CTA to fix it
│          Secondary link                  │  ← Optional secondary action
│                                          │
└──────────────────────────────────────────┘
```

### Empty State Types

**1. First Use (Zero Data)**
```
Welcome! 👋

You haven't created any projects yet.
Projects help you organize your work
and collaborate with your team.

[ Create Your First Project ]
or import from another tool
```

**2. No Results (Search/Filter)**
```
No results for "purple unicorn"

Try:
• Checking your spelling
• Using fewer keywords
• Removing filters

[ Clear Filters ]
```

**3. Completed (All Done)**
```
✓ All caught up!

You've completed all your tasks.
Time for a break? ☕

[ Add New Task ]
```

**4. Error State**
```
😕 Couldn't load messages

We're having trouble connecting.
Check your internet connection
and try again.

[ Retry ]
```

### Empty State Copy Tips

**Headline:**
- State what's missing, not what went wrong
- "No projects yet" not "Empty"

**Description:**
- Explain the value of what goes here
- Keep it brief (2-3 lines max)
- Be encouraging, not scolding

**CTA:**
- Action-oriented verb
- Specific to the empty state
- "Create First Project" not "Get Started"

---

## ONBOARDING PATTERNS

### Onboarding Types

**1. Feature Tours**
```
┌──────────────────────────────────────────┐
│  ┌────────────────────────────────────┐  │
│  │ This is the dashboard where you    │  │
│  │ can see all your metrics at a      │  │
│  │ glance.                            │  │
│  │                         [Next →]   │  │
│  └───────────────────────────────────┬┘  │
│                                      │   │
│  [Dashboard]────────────────────────▲┘   │
│                                          │
└──────────────────────────────────────────┘

Tooltip pointing to relevant UI element.
Step indicator: ● ● ○ ○
```

**2. Progressive Onboarding**
```
Show features in context, as user encounters them.

First time seeing inbox:
"This is your inbox. New messages appear here."
[Got it]

First time composing:
"Tap + to compose a new message."
[Got it]

Contextual, not overwhelming.
```

**3. Onboarding Checklist**
```
Get Started:
☑ Create your account
☑ Add profile photo
☐ Invite team members
☐ Create first project
☐ Complete tutorial

Progress: 40% complete
```

**4. Welcome Wizard**
```
Step 1: What brings you here?
○ Personal use
○ Team collaboration
○ Business management

[Continue →]

────

Step 2: Tell us about yourself
[Name]
[Role]
[Company size]

[← Back] [Continue →]
```

### Onboarding Best Practices

**DO:**
- Keep it short (3-5 steps max)
- Show value quickly (aha moment)
- Make skippable (for returning users)
- Personalize based on answers
- Celebrate completion

**DON'T:**
- Block all access until complete
- Show everything at once
- Make it mandatory for basic use
- Forget about returning users
- Show features they can't use yet

### First-Run Experience Checklist

```markdown
☐ Clear value proposition on first screen
☐ Minimal required info before entry
☐ Progressive profile completion (not all at once)
☐ Quick path to core value (< 2 minutes)
☐ Contextual help over front-loaded tutorials
☐ Empty states guide next actions
☐ Easy way to get help if stuck
☐ Skip option that doesn't punish user
☐ Remember progress if user leaves
☐ Celebrate first success (first post, first project, etc.)
```

---

# EXPANDED CHECKLISTS

---

## INTERACTION DESIGN CHECKLIST

- [ ] All gestures have visible alternatives
- [ ] Feedback is immediate (< 100ms)
- [ ] States are clearly differentiated (default, hover, pressed, disabled)
- [ ] Loading states show progress
- [ ] Animations respect prefers-reduced-motion
- [ ] Microinteractions are consistent
- [ ] Haptics used appropriately (not overused)
- [ ] Error states are recoverable

## CONVERSION CHECKLIST

- [ ] Single, clear CTA above fold
- [ ] Value proposition in headline
- [ ] Social proof visible
- [ ] Form fields minimized
- [ ] Trust signals present
- [ ] Urgency is authentic (not fake)
- [ ] Objections addressed
- [ ] Mobile experience optimized

## ACCESSIBILITY DEEP CHECKLIST

- [ ] Contrast ratio 4.5:1 for text
- [ ] Contrast ratio 3:1 for UI elements
- [ ] Focus visible on all interactive elements
- [ ] Tab order logical
- [ ] Skip link present
- [ ] All images have alt text
- [ ] Forms have proper labels
- [ ] Errors described in text
- [ ] ARIA used correctly
- [ ] Tested with screen reader
- [ ] Touch targets 44px minimum
- [ ] Motion can be disabled

## RTL CHECKLIST

- [ ] Layout mirrors correctly
- [ ] Icons that should flip, do
- [ ] Icons that shouldn't flip, don't
- [ ] Text aligns correctly
- [ ] Numbers display correctly
- [ ] Bidirectional text handled
- [ ] Arabic typography optimized
- [ ] Cultural imagery appropriate

---

*This expanded document adds frameworks from interaction design, persuasion psychology (Cialdini), WCAG 2.2 accessibility guidelines, design systems best practices, UX research methods, and RTL/localization patterns to create a comprehensive design reference.*
