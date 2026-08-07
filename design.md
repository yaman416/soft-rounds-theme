# Soft Rounds Australia Design System

## 1. Brand Overview

Soft Rounds Australia is a premium healthcare apparel and comfort brand for
nurses, healthcare workers, students and other professionals who work long
shifts.

Initial product categories:

- Nursing compression socks
- Premium healthcare scrubs

Future categories may include:

- Scrub caps
- Badge reels
- Pocket organisers
- Shift accessories
- Healthcare gifts

Brand promise:

Premium comfort made for long shifts.

Primary brand qualities:

- Soft
- Durable
- Comfortable
- Professional
- Premium
- Practical
- Modern
- Trustworthy

The website must feel calm, polished and welcoming without looking overly
clinical, childish or excessively feminine.

## 2. Customer Profile

Primary customers include:

- Registered nurses
- Enrolled nurses
- Nursing students
- Aged-care workers
- Disability-support workers
- Allied health professionals
- Healthcare assistants
- Healthcare professionals purchasing gifts

Many customers will browse on mobile phones during breaks, after work or while
commuting.

The shopping experience must therefore be:

- Mobile-first
- Fast
- Easy to scan
- Easy to navigate
- Easy to purchase from
- Clear about sizing
- Clear about delivery
- Clear about returns
- Accessible

## 3. Brand Positioning

Soft Rounds Australia should be positioned as a premium but approachable
Australian healthcare brand.

The brand should communicate:

- Comfort suitable for long shifts
- Thoughtful product design
- Reliable construction
- Professional appearance
- Practical functionality
- Quality materials
- Calm confidence

Avoid unsupported claims such as:

- Best ever
- Number one in Australia
- Guaranteed pain relief
- Doctor approved
- Medical grade
- Clinically proven

These claims must only be used when supported by appropriate evidence.

Preferred messaging examples:

- Premium comfort made for long shifts.
- Soft, durable essentials for healthcare professionals.
- Designed for demanding shifts and everyday comfort.
- Professional essentials that work as hard as you do.

## 4. Visual Direction

The visual style should be:

- Premium
- Clean
- Soft
- Calm
- Modern
- Spacious
- Professional
- Friendly
- Minimal but not empty

Avoid:

- Loud gradients
- Excessive pink
- Harsh clinical blue
- Heavy shadows
- Crowded layouts
- Excessive animation
- Cheap marketplace styling
- Cartoon medical imagery
- Decorative script fonts
- Medical crosses as the primary brand symbol
- Fake reviews or artificial urgency

Rounded corners are a deliberate part of this brand, but they are not uniform.
Surfaces round at 16px, controls at 12px, and only genuinely pill-shaped things
— chips, badges, icon circles — go fully round. Buttons are not pills. See
section 11.

## 5. Colour System

This is Direction C, "Modern Feminine Utility". Every value below exists as a
CSS custom property in `assets/storefront-import-tokens.css`. That file is the
machine-readable copy of sections 5 to 13. **Always style with the token, never
the raw hex.** If the two disagree, this document wins and the token file should
be corrected to match it.

### Surface

| Name | Hex | Token | Use |
|---|---|---|---|
| Warm Ivory | `#F7F5F0` | `--color-ivory`, `--surface-page` | The page floor, and the fill inside quiet controls. |
| Soft White | `#FFFFFF` | `--color-canvas`, `--surface-card` | Cards, header, footer, panels, drawers. Lifts off the ivory. |
| Soft Sand | `#DDD2C2` | `--color-sand` | The announcement bar and the backing behind a loading image. |
| Warm Grey | `#E4E0D8` | `--color-hairline`, `--border-default`, `--surface-strong` | Every 1px border, and the heavier of the two neutral fills. |

### Brand

| Name | Hex | Token | Use |
|---|---|---|---|
| Muted Slate Blue | `#718696` | `--color-slate`, `--color-primary` | The primary action colour: every primary button, the "Why Soft Rounds" panel, focus rings, checklist ticks. |
| Slate Press | `#5F7382` | `--color-slate-press` | Hover and pressed state on slate buttons. |
| Slate Ring | `rgba(113,134,150,.18)` | `--color-slate-ring` | The 3px focus halo around a focused field. |

### Supporting accents

| Name | Hex | Token | Use |
|---|---|---|---|
| Soft Sage | `#A9B5A3` | `--color-sage` | The hero eyebrow pill, and the tint behind the small story image. |
| Soft Clay | `#D69B88` | `--color-clay` | The cart count bubble and the "New" badge. Nothing else. |

Sage and Clay are **accents only** — never a page background, never body text,
never a button. Use at most one of them in a given section.

### Text

| Name | Hex | Token | Use |
|---|---|---|---|
| Deep Charcoal | `#252724` | `--color-ink`, `--text-heading` | Headings, nav, prices, card titles. Never pure black. |
| Muted Charcoal | `#666A64` | `--color-body`, `--text-muted` | Body copy, captions, product metadata, footer links. |
| Placeholder | `#9B9C96` | `--color-muted-soft` | Field placeholder text and disabled labels. |
| On White | `#FFFFFF` | `--color-on-primary` | Text on slate and on charcoal surfaces. |
| On Slate | `#E6E9E5` | `--color-on-slate` | Supporting copy inside the slate panel, where pure white would shout. |

### Semantic

| Name | Hex | Token | Use |
|---|---|---|---|
| Muted Red | `#A64E49` | `--color-error`, `--color-sale` | Field errors, error labels, sale prices. |
| Muted Green | `#55715C` | `--color-success` | Success confirmation only. |

### Fabric swatches

These describe **products, never interface** — they exist so a swatch dot on a
product card matches the garment. Never use them for backgrounds or text.

Blush `#EDAFB6` · Sage `#A8B79B` · Navy `#1F2A52` · Oat `#F1E7D6` ·
Charcoal `#3B3F46` · Black `#16181C` · White `#FBFAF7` ·
Dusty Rose `#C4798C` · Sky `#9FB8D4`

## 6. Colour Usage Rules

- Warm Ivory is the page. Soft White is anything raised off it.
- Deep Charcoal for headings, Muted Charcoal for everything you read in a paragraph.
- Slate Blue means "this is the action". One primary button per view.
- Charcoal is the *secondary* dark action — the cart button and the active filter pill. It never competes with slate for the primary CTA.
- Clay only ever appears on a count bubble or a "New" badge.
- Focus is slate. Selected is charcoal. They are not interchangeable.
- Sale red is not an accent. It appears only on a genuine reduced price.
- Do not rely on colour alone to communicate meaning.
- All text and controls must maintain accessible contrast.

## 7. Typography

**Plus Jakarta Sans** (`--font-display`, `--font-sans`) does all the work —
headings, body, buttons, labels, prices, navigation. Weights 300–700; the system
uses 400 for body, 500 for labels and nav, 600 for headings and buttons.

**Instrument Serif italic** (`--font-accent`, class `.sr-accent`) is the accent
face. It sets **one emphasised phrase inside a heading** and nothing else:

```html
<h1>Premium comfort made for <em class="sr-accent">long shifts</em>.</h1>
```

Never a whole heading, never body copy, never a button, never small text. Used
more than once or twice per page it stops being an accent.

Both families load from Google Fonts in `layout/theme.liquid`.

Avoid:

- Script and decorative faces
- Weights below 300
- Excessive uppercase, except the small tracked labels in section 8
- Body text below 14px

## 8. Type Scale

Every role is a token triplet in `storefront-import-tokens.css`
(`--type-<role>-size`, `-weight`, `-line`, plus `-tracking` where non-zero).

| Role | Size | Weight | Line | Tracking | Use |
|---|---|---|---|---|---|
| `hero` | 46px | 600 | 1.08 | -0.02em | Hero headline (32px on mobile) |
| `display-xl` | 40px | 600 | 1.12 | -0.02em | Story section heading |
| `display-lg` | 34px | 600 | 1.15 | -0.015em | Section headings (26px on mobile) |
| `display-md` | 30px | 600 | 1.2 | -0.015em | Newsletter heading |
| `display-sm` | 21px | 600 | 1.25 | 0 | Category card titles (19px on mobile) |
| `title-md` | 18px | 600 | 1.3 | 0 | Panel column headings |
| `title-sm` | 16px | 600 | 1.35 | 0 | Product card titles |
| `body-lg` | 17px | 400 | 1.6 | 0 | Hero and story paragraphs |
| `body-md` | 16px | 400 | 1.6 | 0 | Default running text |
| `body-sm` | 14.5px | 400 | 1.55 | 0 | Card captions, footer links |
| `price` | 15px | 500 | 1 | 0 | Card price |
| `price-was` | 13px | 400 | 1.4 | 0 | Struck-through compare-at price |
| `caption` | 13px | 500 | 1.4 | 0 | Field labels, spec labels |
| `caption-sm` | 12.5px | 400 | 1.5 | 0 | Disclaimers, legal line |
| `badge` | 11.5px | 600 | 1 | 0.08em | Eyebrow pills (uppercase) |
| `uppercase-tag` | 10.5px | 700 | 1 | 0.1em | "New" badges (uppercase) |
| `eyebrow` | 11px | 600 | 1 | 0.16em | Canvas labels (uppercase) |
| `footer-head` | 12px | 600 | 1 | 0.12em | Footer column heads (uppercase) |
| `button-md` | 15px | 600 | 1 | 0 | Button labels |
| `button-sm` | 13.5px | 500 | 1 | 0 | Pill and chip labels |
| `nav-link` | 14px | 500 | 1 | 0 | Header navigation (600 when active) |

Section headings step down one role on mobile rather than scaling fluidly.
Dawn's generic `h1`–`h4` in `base.css` follow the same ladder.

## 9. Spacing System

Base unit 4px.

| Token | Value | Use |
|---|---|---|
| `--space-xs` | 4px | Micro spacing |
| `--space-sm` | 8px | Compact spacing |
| `--space-md` | 12px | Icon-to-text spacing |
| `--space-base` | 16px | Standard internal spacing, mobile gutters |
| `--space-lg` | 24px | Card padding, grid gaps |
| `--space-xl` | 32px | Component spacing |
| `--space-xxl` | 48px | Panel padding, footer column gutters |
| `--space-section` | 80px | Desktop section spacing |

Sections run 80–88px apart at desktop and 40px on mobile. Card grids stay at
24px. Open bands, tight grids.

## 10. Container System

| Token | Value | Use |
|---|---|---|
| `--container-page` | 1440px | Standard content width |
| `--container-narrow` | 760px | Editorial reading width |

`--container-page` must stay equal to Dawn's `page_width` theme setting, or
custom sections misalign with Dawn's own down the page.

Horizontal page padding, matched between `.sr-container` and `.page-width`:
16px mobile · 24px from 750px · 36px from 990px. The hero card insets 64px from
the page edge at desktop.

### Fixed dimensions

Header 78px (62px mobile) · announcement bar 40px (34px mobile) · button 50px ·
chip 38px · input 52px · header icon circle 42px · card arrow circle 40px ·
swatch dot 15px.

## 11. Border Radius

Two radii carry the whole system.

| Token | Value | Applies to |
|---|---|---|
| `--radius-md` (`--radius-card`) | 16px | Every surface: cards, panels, the hero card, image plates, the newsletter card |
| `--radius-sm` (`--radius-button`, `--radius-input`) | 12px | Everything you click or type into: buttons, inputs |
| `--radius-full` | 999px | Pills, chips, badges, icon circles, swatch dots |

Nothing has a hard 0px corner except the page body. Note the deliberate split:
**surfaces are 16px, controls are 12px, and only genuinely pill-shaped things
are fully round.** Buttons are *not* pills in this direction.

## 12. Borders and Shadows

Default border: 1px solid `--border-default` (`#E4E0D8`).

Focus is a 1px slate border plus a 3px slate halo (`--shadow-focus`), never an
outline offset.

Two elevation tiers only:

| Token | Value | Use |
|---|---|---|
| `--shadow-soft` | `0 4px 20px rgba(37,39,36,.06)` | Cards and panels at rest |
| `--shadow-pop` | `0 12px 40px rgba(37,39,36,.12)` | Card hover, and the floating hero card |

Cards deepen their shadow on hover; they do **not** lift, scale or translate.
`--lift-pop` is 0 in this direction. Depth comes from the shadow alone.

## 13. Buttons

All buttons are 12px radius, 50px tall, label in Plus Jakarta Sans 15px/600.
No press transform. Focus shows the slate halo.

| Variant | Class | Fill | Label | Hover |
|---|---|---|---|---|
| Primary | `.sr-btn--primary` | Slate Blue | White | Slate Press |
| Secondary | `.sr-btn--secondary` | White, 1px warm grey border | Charcoal | Ivory fill |
| Dark | `.sr-btn--ink` | Charcoal | Ivory | `#3E4340` |
| Tertiary | `.sr-btn--tertiary` | None | Charcoal | Underline |

### Chips and pills

`.sr-btn--sm.sr-btn--chip` is the pill used in shortcut rows and filter bars:
38px tall, fully round, white fill with a warm grey border, 13.5px/500 label.
The border darkens to charcoal on hover. The active chip inverts to a charcoal
fill with ivory text at 600.

One primary button per view. If two actions look equally important, one of them
is secondary.

### Text Link

- Clear underline or directional icon
- Visible hover state
- Visible keyboard focus
- Must not rely on colour alone


## 14. Product Cards

Product cards may include:

- Primary product image
- Optional second image on desktop hover
- Product name
- Price
- Compare-at price when applicable
- Colour count where useful
- Genuine product badge
- Review summary only when genuine review data exists

Product cards must:

- Use consistent image ratios
- Keep product names readable
- Show pricing clearly
- Work without hover
- Be easy to tap on mobile
- Avoid excessive borders
- Avoid fake urgency
- Avoid fake stock counts
- Avoid fake ratings
- Avoid unsupported badges

## 15. Photography Direction

Photography should feel:

- Natural
- Bright but soft
- Premium
- Calm
- Comfortable
- Professional
- Realistic
- Inclusive

Use a mixture of:

- Clean product photography
- Lifestyle photography
- Close-up fabric details
- Packaging imagery
- Healthcare-inspired environments
- Realistic workplace scenarios

Avoid:

- Generic staged doctors
- Unrealistic hospital environments
- Harsh clinical lighting
- Over-retouched skin
- Inaccurate AI-generated product details
- Images that misrepresent the actual product

Product images must accurately represent the item sold.

## 16. Icons

Use simple outline icons.

Preferred stroke:

- 1.5px to 2px

Icons should have:

- Consistent visual weight
- Rounded line endings
- Clear meaning
- Accessible labels where required

Do not combine unrelated icon styles.

## 17. Header

Desktop header should support:

- Soft Rounds Australia logo
- Shop menu
- Compression Socks
- Scrubs
- About
- Search
- Account
- Cart

Mobile header should support:

- Menu button
- Logo
- Search
- Cart

Header requirements:

- Clean hierarchy
- Accessible keyboard navigation
- Usable mobile menu
- Compact height
- Optional sticky behaviour
- No excessive announcement bars
- No hardcoded menu items

## 18. Homepage Structure

Recommended homepage order:

1. Announcement bar
2. Header
3. Hero section
4. Shop by category
5. Best sellers
6. Brand benefit strip
7. Featured compression socks
8. Featured scrubs
9. Brand story section
10. Genuine customer reviews when available
11. Email signup
12. Footer

The homepage must quickly answer:

- What does Soft Rounds Australia sell?
- Who are the products for?
- Why are the products useful?
- Why should customers trust the brand?
- Where should customers begin shopping?

## 19. Product Page Structure

Recommended order:

1. Product media gallery
2. Product title
3. Price
4. Genuine review summary when available
5. Short product benefit statement
6. Variant selectors
7. Size guide
8. Quantity selector
9. Add-to-cart button
10. Payment information
11. Shipping and returns summary
12. Product description
13. Materials and care
14. Fit information
15. Compression information where relevant
16. Related products
17. Recently viewed products if implemented carefully

Do not make medical treatment claims unless legally permitted and supported by
appropriate evidence.

## 20. Collection Pages

Collection pages should include:

- Collection heading
- Optional concise introduction
- Product count
- Sort control
- Useful filters
- Responsive product grid
- Empty-state message

Avoid long introductions that push products too far down the page.

## 21. Forms

All forms must include:

- Visible labels
- Clear error messages
- Visible focus states
- Accessible colour contrast
- Touch-friendly input sizes
- Appropriate input types

Do not use placeholder text as the only form label.

## 22. Accessibility

Target WCAG 2.2 AA where practical.

Requirements:

- Semantic HTML
- Keyboard-accessible navigation
- Visible focus states
- Useful alternative text
- Correct heading hierarchy
- Sufficient colour contrast
- Accessible product forms
- Reduced-motion support
- No colour-only communication
- Touch targets around 44px or larger

## 23. Responsive Behaviour

Design mobile-first.

Test at:

- 375px
- 430px
- 768px
- 1024px
- 1280px
- 1440px

At mobile widths:

- Avoid horizontal scrolling
- Maintain readable text sizes
- Keep purchasing actions prominent
- Stack content intentionally
- Preserve image quality
- Avoid tiny controls
- Avoid overcrowded navigation

## 24. Motion

Animations should be subtle and purposeful.

Durations and easing are tokens:

| Token | Value | Use |
|---|---|---|
| `--duration-fast` | 150ms | Hover and colour feedback |
| `--duration-base` | 200ms | Interface transitions, shadow changes |
| `--duration-slow` | 350ms | Larger reveals |
| `--ease-standard` | `cubic-bezier(0.2, 0, 0, 1)` | Everything |

Direction C has no bounce and no press transform. Cards respond by deepening
their shadow, buttons by changing fill. Nothing scales, lifts or overshoots —
the restraint is the point.

Use:

- Gentle opacity transitions
- Small vertical movement
- Button feedback
- Drawer transitions

Avoid:

- Constant movement
- Large parallax effects
- Excessive scroll animation
- Animation that delays shopping

Respect `prefers-reduced-motion`.

## 25. Performance

Requirements:

- Avoid unnecessary JavaScript
- Use responsive Shopify images
- Lazy-load below-the-fold images
- Do not lazy-load the primary hero image
- Reserve image dimensions
- Avoid large autoplay videos
- Avoid excessive third-party apps
- Prefer CSS for simple interactions
- Keep section code modular

## 26. Shopify Theme Editor Requirements

Major sections must be configurable through Shopify.

Merchants should be able to change:

- Heading
- Supporting text
- Images
- Buttons
- Alignment
- Colour scheme
- Section spacing
- Products
- Collections
- Number of visible items where appropriate

Use repeatable blocks for:

- Category cards
- Brand benefits
- Testimonials
- Icons
- FAQ items

Do not hardcode:

- Product titles
- Prices
- Collection handles
- Product URLs
- Image URLs
- Navigation links

## 27. Content Principles

Copy should be:

- Concise
- Specific
- Customer-focused
- Easy to scan
- Warm
- Credible
- Professional

Avoid exaggerated language.

Instead of:

> Experience the ultimate revolution in healthcare comfort.

Use:

> Soft, durable essentials designed for long shifts.

## 28. Development Rules

The Shopify theme must:

- Use valid Shopify Liquid
- Use Online Store 2.0 JSON templates
- Use editable sections and blocks
- Preserve native Shopify commerce behaviour
- Avoid hardcoded store content
- Pass Shopify Theme Check without new errors
- Use semantic HTML
- Use reusable CSS variables
- Remain maintainable
- Avoid unnecessary dependencies
- Avoid modifying checkout
- Avoid fake claims
- Avoid fake reviews
- Avoid unsupported medical statements