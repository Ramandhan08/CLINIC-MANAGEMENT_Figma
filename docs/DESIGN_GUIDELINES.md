# Design Guidelines

## Comprehensive Design Standards & Best Practices

---

## Table of Contents

1. [Visual Design](#visual-design)
2. [Typography](#typography)
3. [Color System](#color-system)
4. [Component Guidelines](#component-guidelines)
5. [Spacing & Layout](#spacing--layout)
6. [Accessibility](#accessibility)
7. [Interactions](#interactions)
8. [Content Guidelines](#content-guidelines)
9. [Mobile Design](#mobile-design)

---

## Visual Design

### Design Principles

#### 1. **Clarity**
- Clear hierarchy and visual structure
- Obvious primary and secondary actions
- Unambiguous information presentation
- Consistent visual language

#### 2. **Efficiency**
- Minimize steps to complete tasks
- Reduce cognitive load
- Logical grouping of related items
- Predictable navigation

#### 3. **Confidence**
- Clear feedback for user actions
- Error prevention and recovery
- Reassuring visual states
- Professional appearance

#### 4. **Accessibility**
- Sufficient color contrast
- Readable text sizes
- Keyboard navigation
- Screen reader support

### Visual Hierarchy

**Primary Information**
- Large, bold text
- Strategic use of color
- Central positioning
- High contrast background

**Secondary Information**
- Medium size text
- Subtle colors
- Secondary positioning
- Standard contrast

**Tertiary Information**
- Small text
- Gray color (#8E8E93)
- Lower visual weight
- Supporting role

### Depth & Elevation

Use subtle shadows to indicate layering:

```
Level 1 (Base): No shadow
Level 2 (Cards, Modals): 
  Box shadow: 0px 2px 8px rgba(0, 0, 0, 0.1)
Level 3 (Dropdowns, Popovers): 
  Box shadow: 0px 4px 16px rgba(0, 0, 0, 0.15)
Level 4 (Overlays, Top Menus): 
  Box shadow: 0px 8px 32px rgba(0, 0, 0, 0.2)
```

---

## Typography

### Font Family

- **Primary Font:** Poppins (Headings, Display)
  - Google Fonts: https://fonts.google.com/specimen/Poppins
  - Weights: Bold (700), SemiBold (600), Medium (500)

- **Secondary Font:** Inter (Body, UI)
  - Google Fonts: https://fonts.google.com/specimen/Inter
  - Weights: Regular (400), SemiBold (600)

### Type Scale

| Usage | Font | Size | Weight | Line Height | Letter Spacing |
|-------|------|------|--------|-------------|---|
| Display | Poppins | 32px | Bold (700) | 40px | -0.5px |
| Heading 1 | Poppins | 24px | SemiBold (600) | 32px | -0.3px |
| Heading 2 | Poppins | 20px | SemiBold (600) | 28px | -0.2px |
| Heading 3 | Poppins | 18px | SemiBold (600) | 26px | -0.1px |
| Subheading | Poppins | 16px | Medium (500) | 24px | 0px |
| Body | Inter | 14px | Regular (400) | 20px | 0.2px |
| Caption | Inter | 12px | Regular (400) | 16px | 0.3px |
| Button | Inter | 14px | SemiBold (600) | 20px | 0.5px |

### Text Styling

**All Caps**
- Use sparingly
- Increase letter spacing by 0.5px
- Use for labels and emphasis only
- Example: "ACTIVE STATUS"

**Emphasis**
- Use bold for important information
- Use color sparingly for emphasis
- Don't underline text (reserved for links)
- Use italics for medical terms only

**Links**
- Color: #007AFF (Medical Blue)
- Underline only on hover
- Pointer cursor on hover
- Never use "click here" as link text

### Text Truncation

- Single line text: Truncate with ellipsis (...)
- Multi-line text: Show 2-3 lines before truncating
- Always provide full text on hover/detail view
- Example: "Long patient name..." [Hover to see full name]

---

## Color System

### Primary Colors

| Color | Hex | RGB | Usage | Example |
|-------|-----|-----|-------|---------|
| Medical Blue | #007AFF | 0, 122, 255 | Primary buttons, links, focus | CTA buttons, active tabs |
| Health Green | #34C759 | 52, 199, 89 | Success, approval | Successful actions, confirmed |
| Alert Red | #FF3B30 | 255, 59, 48 | Errors, warnings, danger | Delete button, errors |
| Warning Yellow | #FF9500 | 255, 149, 0 | Caution, warnings | Warnings, pending actions |

### Neutral Colors

| Color | Hex | RGB | Usage |
|-------|-----|-----|-------|
| Black | #000000 | 0, 0, 0 | Primary text, strong emphasis |
| Dark Gray | #333333 | 51, 51, 51 | Secondary text, headings |
| Medium Gray | #8E8E93 | 142, 142, 147 | Tertiary text, labels, disabled |
| Light Gray | #F2F2F7 | 242, 242, 247 | Backgrounds, borders, dividers |
| White | #FFFFFF | 255, 255, 255 | Cards, input backgrounds |
| Border Gray | #E5E5EA | 229, 229, 234 | Component borders |

### Color Usage Rules

**Don't Use Color Alone**
- Always combine with text or icons
- Example: Don't just show red background; add error icon

**Semantic Colors**
- Blue = Action, Information, Link
- Green = Success, Approval, Positive
- Red = Error, Danger, Negative
- Yellow = Warning, Caution, Needs Attention

**Contrast Requirements**
- Text on background: Minimum 4.5:1 contrast ratio
- Graphical elements: Minimum 3:1 contrast ratio
- Disabled state: 3:1 contrast ratio

### Color States

**Button Color States:**
- Default: #007AFF
- Hover: #0051D5 (Darker blue)
- Active/Pressed: #003D99 (Even darker)
- Disabled: #8E8E93 (Gray)
- Loading: Add opacity

**Input Color States:**
- Default: #F2F2F7 background, #000000 text
- Focus: #007AFF border, #FFFFFF background
- Error: #FF3B30 border, #FFF5F5 background
- Disabled: #E5E5EA background, #8E8E93 text
- Filled: #E5E5EA background, #000000 text

---

## Component Guidelines

### Buttons

#### Button Sizes

```
Small:      32px height, 12px - 16px padding
Regular:    44px height, 14px - 18px padding (Default)
Large:      56px height, 16px - 24px padding
```

#### Button States

**Default State**
- Background: Color varies by type
- Border: 1px solid transparent
- Cursor: Pointer
- Text: White or dark based on color

**Hover State**
- Background: Slightly darker than default
- Slight scale: 1.02
- Shadow: Light shadow for elevation

**Active/Pressed State**
- Background: Darker shade
- No scale change
- Pressed appearance

**Disabled State**
- Background: Light gray #E5E5EA
- Text: Medium gray #8E8E93
- Cursor: Not-allowed
- No hover effects

**Loading State**
- Show spinner
- Text: Hidden or "Loading..."
- Button: Non-interactive
- Duration: Don't exceed 3 seconds

#### Button Types

**Primary Button**
- Use for main actions
- Background: Medical Blue #007AFF
- Text: White
- Shape: 8px border radius
- Example: "Save Patient", "Schedule Appointment"

**Secondary Button**
- Use for alternative actions
- Background: Light Gray #F2F2F7
- Text: Medical Blue #007AFF
- Border: 1px solid #E5E5EA
- Example: "Cancel", "Reset"

**Danger Button**
- Use for destructive actions
- Background: Alert Red #FF3B30
- Text: White
- Require confirmation before action
- Example: "Delete Patient", "Cancel Appointment"

**Text Button**
- Use for lower priority actions
- Background: Transparent
- Text: Medical Blue #007AFF
- Underline: Only on hover
- Example: "Learn more", "View details"

### Input Fields

#### Input Field Sizes

```
Small:      32px height, 12px padding
Regular:    44px height, 14px padding (Default)
Large:      56px height, 16px padding
```

#### Input States

**Default State**
- Background: White #FFFFFF
- Border: 1px solid #E5E5EA
- Text: Black #000000
- Placeholder: Medium Gray #8E8E93

**Focused State**
- Border: 2px solid #007AFF (Medical Blue)
- Box shadow: 0px 0px 0px 4px rgba(0, 122, 255, 0.1)
- Outline: None

**Filled State**
- Background: Light Gray #F2F2F7
- Border: 1px solid #E5E5EA
- Text: Black #000000

**Error State**
- Border: 2px solid #FF3B30 (Alert Red)
- Background: White with slight red tint #FFF5F5
- Icon: Red error icon
- Message: Error text below in red

**Disabled State**
- Background: Light Gray #F2F2F7
- Border: 1px solid #E5E5EA
- Text: Medium Gray #8E8E93
- Cursor: Not-allowed

#### Input Field Types

**Text Input**
- Single line text entry
- For names, emails, etc.
- Clear button on focus

**Email Input**
- Email validation
- Mobile keyboard: Email format
- Show error if invalid format

**Phone Input**
- Auto-format phone numbers
- Support multiple formats
- Mobile keyboard: Phone pad

**Number Input**
- Numeric keyboard
- Min/max validation
- Spinner controls (optional)

**Date Input**
- Calendar picker
- Keyboard entry support
- Format: MM/DD/YYYY or DD/MM/YYYY

**Time Input**
- Time picker interface
- 12-hour or 24-hour format
- Minutes increment: 15 minutes

**Select/Dropdown**
- Closed by default, shows selected value
- Open to show all options
- Searchable for >5 items
- Single or multi-select option

**Textarea**
- For longer text input
- Minimum: 100px height
- Auto-resize or scrollable
- Character counter (optional)

### Cards

#### Card Layout

```
Padding: 16px
Border Radius: 12px
Border: 1px solid #E5E5EA
Background: White #FFFFFF
Shadow: Light shadow (0px 2px 8px rgba(0,0,0,0.1))
```

#### Card Types

**Info Card**
- Display static information
- No interactive elements
- Used for patient info, appointment details

**Action Card**
- Clickable cards with actions
- Hover effect: Slight scale, shadow increase
- Button in bottom right
- Used for patient list, appointment list

**Status Card**
- Show status with visual indicator
- Color-coded status dot
- Status text below
- Used for appointment status, patient status

#### Card Content

**Header**
- Title: Heading 3 (18px SemiBold)
- Optional icon in top right
- 16px padding

**Body**
- Body text: 14px Regular
- Content: 16px padding
- Proper spacing between items

**Footer**
- Optional action buttons
- Gray background #F2F2F7
- 12px padding
- Right-aligned buttons

### Modals & Dialogs

#### Modal Sizing

```
Small:       400px width (for simple actions)
Regular:     600px width (Default)
Large:       800px width (for complex forms)
Max Height:  90vh (with scrollable content)
```

#### Modal Structure

```
┌─────────────────────────────┐
│ Title            X Close    │ ← Header (24px SemiBold Poppins)
├─────────────────────────────┤
│                             │
│       Modal Content         │ ← Body (scrollable if needed)
│                             │
├─────────────────────────────┤
│        Cancel    Save        │ ← Footer (buttons right-aligned)
└─────────────────────────────┘
```

#### Modal Types

**Confirmation Dialog**
- Simple yes/no question
- Action + Cancel buttons
- Explain consequence of action

**Alert Dialog**
- Important notification
- Single acknowledgment button
- Use sparingly

**Form Modal**
- Data entry modal
- Save and Cancel buttons
- Validation on submit

**Message Modal**
- Information or success message
- Single close/OK button
- Auto-close after 3 seconds (optional)

### Tabs

#### Tab Styling

**Inactive Tab**
- Text color: Medium Gray #8E8E93
- Border bottom: 2px solid transparent
- Cursor: Pointer
- Padding: 12px 16px

**Active Tab**
- Text color: Medical Blue #007AFF
- Border bottom: 2px solid #007AFF
- Background: White or light background

**Hover Tab** (Inactive)
- Text color: Dark Gray #333333
- Slight background tint

#### Tab Usage

- Use for switching between related content
- Maximum 5 tabs per row
- Wrap to new row if more tabs
- Show tab content on selection
- Maintain scroll position when switching

### Navigation

#### Top Navigation Bar

```
Height: 64px
Padding: 12px 24px
Components: Logo, Menu, User Profile
Background: White
Border bottom: 1px solid #E5E5EA
```

#### Sidebar Navigation

```
Width: 280px (Desktop)
Padding: 16px
Background: White or Light Gray
Border right: 1px solid #E5E5EA
Items: Icons + Label (16px)
Active item: Medical Blue background
Hover: Light Gray background
Collapse button: Reduce to 80px
```

---

## Spacing & Layout

### Spacing Scale

Use 8px as base unit for consistent spacing:

```
2px   = 0.25x (divider, minimal space)
4px   = 0.5x  (micro spacing)
8px   = 1x    (base unit, component padding)
12px  = 1.5x  (section spacing)
16px  = 2x    (card padding, common gap)
24px  = 3x    (section separation)
32px  = 4x    (major section separation)
48px  = 6x    (page section separation)
```

### Grid System

**Desktop Layout**
- 12-column grid
- Column width: 70px
- Gutter: 24px
- Margin: 24px

**Tablet Layout**
- 8-column grid
- Column width: 60px
- Gutter: 20px
- Margin: 20px

**Mobile Layout**
- 4-column grid
- Column width: 100% / 4
- Gutter: 16px
- Margin: 16px

### Common Layouts

**Two Column**
- 6 + 6 columns
- Gap: 24px
- Use for balanced content

**Three Column**
- 4 + 4 + 4 columns
- Gap: 24px
- Use for card layouts

**Sidebar + Content**
- 3 + 9 columns
- Gap: 24px
- Use for navigation + main content

---

## Accessibility

### Color Contrast

**WCAG AA Standards**
- Normal text: 4.5:1 contrast ratio
- Large text (18px+): 3:1 contrast ratio
- Graphics: 3:1 contrast ratio

**Testing Tools**
- WebAIM Contrast Checker
- WAVE Browser Extension
- Color Contrast Analyzer

### Typography Accessibility

**Font Size**
- Minimum 12px for body text
- 14px preferred for main content
- 18px minimum for large text

**Line Height**
- Minimum 1.4 (1.4x font size)
- Preferred 1.5 or higher
- Example: 14px × 1.5 = 21px line height

**Letter Spacing**
- Normal: 0.2px - 0.5px
- Increased: 0.8px - 1px for emphasis

### Interactive Elements

**Button Size**
- Minimum: 44px × 44px (WCAG standard)
- Touch target: 48px × 48px (mobile)
- Spacing between buttons: 8px minimum

**Clickable Area**
- Minimum: 44px height or width
- Sufficient spacing from other elements
- Visible focus indicator

**Focus Indicators**
- 2px solid #007AFF border
- Visible on all interactive elements
- High contrast with background

### Keyboard Navigation

**Tab Order**
- Logical tab order (left to right, top to bottom)
- Skip to main content link
- Tab order visible with indicator

**Keyboard Shortcuts**
- Common shortcuts: Ctrl+S (Save), Ctrl+Z (Undo)
- Escape closes modals
- Arrow keys for navigation
- Enter to submit forms

### Screen Reader Support

**Proper Semantic HTML**
- Use appropriate heading levels (h1, h2, etc.)
- Use label elements for form fields
- Use semantic buttons and links
- Alt text for images

**ARIA Labels**
- aria-label for icon buttons
- aria-describedby for complex descriptions
- aria-live for dynamic content updates
- role attributes for custom components

### Motion & Animation

**Respects Prefers Reduced Motion**
- Check user OS settings
- Disable animations if prefers-reduced-motion
- Provide static alternative

**Animation Duration**
- Maximum: 300ms for interactions
- Faster: <100ms feedback animations
- Slower: >500ms for transitions

---

## Interactions

### Hover States

**Button Hover**
- Slight scale increase: 1.02
- Subtle shadow increase
- Color slightly darker
- Cursor: Pointer

**Card Hover**
- Slight shadow increase
- Scale: 1.01
- Optional text color change
- Cursor: Pointer

**Text Hover**
- Color change or underline
- No scale change
- Cursor: Pointer

### Click/Active States

**Button Active**
- Pressed appearance (no scale)
- Darker color
- Optional shadow decrease

**Link Active**
- Color: Visited blue #5AC8FA (optional)
- Underline persistent

### Focus States

**All Interactive Elements**
- 2px solid Medical Blue #007AFF border
- Or 2px outline
- Sufficient contrast
- No outline removal without replacement

### Transitions

**Standard Transition**
```
transition: all 0.2s ease-in-out;
```

**Slide Transition**
```
transition: transform 0.3s ease-out;
```

**Fade Transition**
```
transition: opacity 0.2s ease-in;
```

### Loading States

**Loading Spinner**
- Show spinner icon
- Rotate animation: 1s / 360°
- Continuous rotation
- Centered in container

**Loading Skeleton**
- Gray placeholder
- Pulse animation
- Match content shape
- Remove when loaded

**Progress Bar**
- Width increases with progress
- Color: Medical Blue #007AFF
- Smooth animation
- Show percentage (optional)

### Animations to Avoid

- ❌ Blinking text
- ❌ Auto-playing video
- ❌ Rapid flashing (more than 3x/sec)
- ❌ Excessively long animations
- ❌ Animations that can't be paused

---

## Content Guidelines

### Messaging

**User Feedback**
- Clear and concise
- Action-oriented
- Use simple language
- Avoid jargon

**Error Messages**
- Explain what went wrong
- Suggest how to fix
- Use red color (#FF3B30)
- Include error icon

**Success Messages**
- Confirm action completed
- Use green color (#34C759)
- Include checkmark icon
- Auto-dismiss after 3 seconds

**Warning Messages**
- Explain potential consequence
- Use yellow color (#FF9500)
- Include warning icon
- Require acknowledgment for critical warnings

### Form Labels

**Labels**
- Always provide labels
- Place above input (default)
- Use clear, descriptive text
- Indicate required fields with * or "Required"

**Placeholder Text**
- Don't replace labels with placeholders
- Use for format hints
- Example: "MM/DD/YYYY" for date field
- Light gray color (#8E8E93)

**Help Text**
- Explain complex fields
- Place below input
- Use small font (12px)
- Optional but recommended

### Language

**Tone**
- Professional but friendly
- Clear and direct
- Empathetic
- Positive whenever possible

**Terminology**
- Use consistent terminology throughout
- Avoid medical jargon unless necessary
- Define abbreviations first use
- Use standard medical terms appropriately

**Call-to-Action (CTA)**
- Action verbs: "Save", "Submit", "Create"
- Be specific: "Save Patient" not "Submit"
- Avoid: "Click here", "OK", "Yes/No"

---

## Mobile Design

### Responsive Breakpoints

```
Mobile:     320px - 480px (Portrait)
Mobile Landscape: 480px - 768px
Tablet:     768px - 1024px
Desktop:    1024px+
Large Desktop: 1440px+
```

### Mobile Touch Targets

**Minimum Size**
- 44px × 44px (WCAG AA)
- 48px × 48px (Recommended)

**Spacing**
- 8px minimum between interactive elements
- 12px preferred spacing

### Mobile Navigation

**Primary Navigation**
- Bottom tab navigation for main sections
- 4-5 tabs maximum
- Icons + labels (below icons)
- Active tab: Medical Blue highlight

**Alternative: Hamburger Menu**
- Only if more than 5 main sections
- Top right corner
- Animated icon (3 horizontal lines)
- Drawer menu slides from left

### Mobile Optimization

**Text Size**
- Body: 14-16px (readable)
- Buttons: 14px minimum
- Inputs: 16px to prevent zoom on focus

**Tap Areas**
- All buttons: 44x44px minimum
- Form fields: Full width
- List items: 48px minimum height

**Thumb Zone**
- Bottom 40% of screen easiest to reach
- Top 20% requires reach (ok for less frequent actions)
- Center: 20-40% of screen

**Landscape Handling**
- Hide non-essential elements
- Stack horizontally instead of vertically
- Use landscape-optimized layout

### Mobile Performance

**Image Optimization**
- Use WebP format where supported
- Responsive images (srcset)
- Optimize for mobile sizes
- Lazy load below fold

**Touch Interactions**
- Avoid hover states (limited on touch)
- Show feedback immediately
- Avoid double-tap zoom (use viewport meta tag)
- Support pull-to-refresh

---

## Design Tokens

### Token Structure

```
{Component}-{Property}-{State}

Example: button-background-hover
         card-border-color
         input-padding-regular
```

### Common Tokens

**Color Tokens**
- color-primary: #007AFF
- color-success: #34C759
- color-error: #FF3B30
- color-warning: #FF9500
- color-text-primary: #000000
- color-text-secondary: #333333
- color-text-tertiary: #8E8E93
- color-background-light: #F2F2F7
- color-background-white: #FFFFFF
- color-border: #E5E5EA

**Spacing Tokens**
- spacing-xs: 4px
- spacing-sm: 8px
- spacing-md: 16px
- spacing-lg: 24px
- spacing-xl: 32px
- spacing-xxl: 48px

**Typography Tokens**
- font-family-primary: Poppins
- font-family-secondary: Inter
- font-size-sm: 12px
- font-size-md: 14px
- font-size-lg: 16px
- font-size-xl: 18px
- font-size-2xl: 24px

**Shadow Tokens**
- shadow-sm: 0px 2px 8px rgba(0,0,0,0.1)
- shadow-md: 0px 4px 16px rgba(0,0,0,0.15)
- shadow-lg: 0px 8px 32px rgba(0,0,0,0.2)

**Border Radius Tokens**
- radius-sm: 4px
- radius-md: 8px
- radius-lg: 12px
- radius-full: 50%

---

## Quality Checklist

Before submitting designs, verify:

- [ ] Contrast ratios meet WCAG AA standards
- [ ] All text is readable at intended sizes
- [ ] Focus states are visible and clear
- [ ] All interactive elements are 44px+ minimum
- [ ] Color is not the only indicator of information
- [ ] Spacing is consistent with 8px grid
- [ ] Typography follows type scale
- [ ] Components follow design system
- [ ] Consistency across all screens
- [ ] Mobile responsive layouts work properly
- [ ] Loading states are handled
- [ ] Error states are handled
- [ ] Empty states are designed
- [ ] Animations are smooth and purposeful
- [ ] Content is clear and concise

---

## Resources

- [Figma Design System](https://www.figma.com/design/AOMwW42pw53xu6RIOaWJE0/Clinic-Management-Screens)
- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [Material Design](https://material.io/design/)
- [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)

---

**Version:** 1.0  
**Last Updated:** [Current Date]

