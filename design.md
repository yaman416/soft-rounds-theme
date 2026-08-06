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

Rounded corners are a deliberate part of this brand and are applied broadly.
That is not the same as making everything a pill: buttons and small controls
are fully rounded, panels and cards use the softer radii in section 11.

## 5. Colour System

Every value in sections 5 to 13 exists as a CSS custom property in
`assets/storefront-import-tokens.css`. That file is the machine-readable copy of
this document. **Always style with the token, never with the raw hex.** If the
two ever disagree, the token file is wrong and should be corrected to match this
document — not the other way around.

### Surface

| Name | Hex | Token | Use |
|---|---|---|---|
| Warm Ivory | `#F7F5F0` | `--color-ivory`, `--surface-page` | The page floor. Every public page sits on this. |
| Soft White | `#FFFFFF` | `--color-canvas`, `--surface-card` | Cards, forms, drawers, modals, navigation panels. Lifts off the ivory. |
| Surface Soft | `#F1EDE4` | `--color-surface-soft`, `--surface-soft` | Quiet bands inside an ivory page, review cards, hover fills. |
| Surface Strong | `#E9E4D9` | `--color-surface-strong` | Circular icon-button fills, the heavier of the two neutral fills. |
| Cream | `#FBF8EE` | `--color-cream` | Benefit-icon discs and soft editorial tints. |
| Blush | `#F9F0E8` | `--color-blush-bg`, `--surface-photo` | Photo plate backing while an image loads. |
| Coral Wash | `#FFF3F4` | `--color-coral-wash`, `--surface-promo` | Promotional panels and the soft button variant. |

### Brand

| Name | Hex | Token | Use |
|---|---|---|---|
| Coral | `#F26B6B` | `--color-coral`, `--color-primary` | The single brand colour. Primary CTAs, the cart bubble, the active nav underline, filled star ratings, saved-heart state. |
| Coral Press | `#E00B41` | `--color-coral-press` | Hover and pressed state on coral CTAs, and brand-coloured link text. |
| Coral Soft | `#FFD1DA` | `--color-coral-soft` | Disabled CTAs, hover underline on nav links, text selection. |

Coral is used **scarcely**. Most pages should be ivory, white and ink with one
or two coral moments. If a page has more than three coral elements competing in
one viewport, remove some.

### Text

| Name | Hex | Token | Use |
|---|---|---|---|
| Ink | `#222222` | `--color-ink`, `--text-heading` | Headings, nav, prices, most link text. Never pure black. |
| Body | `#3F3F3F` | `--color-body`, `--text-body` | Running paragraph text where ink would feel heavy. |
| Muted | `#6A6A6A` | `--color-muted`, `--text-muted` | Captions, product metadata, footer sub-labels, secondary information. |
| Muted Soft | `#929292` | `--color-muted-soft` | Disabled text. Used sparingly. |
| On Primary | `#FFFFFF` | `--color-on-primary` | Text on coral and on ink surfaces. |

### Borders

| Name | Hex | Token | Use |
|---|---|---|---|
| Hairline | `#DDDDDD` | `--color-hairline`, `--border-default` | The default 1px rule — header base, footer splits, card outlines. |
| Hairline Soft | `#EBEBEB` | `--color-hairline-soft` | Lighter divider inside long editorial copy. |
| Border Strong | `#C1C1C1` | `--color-border-strong` | Heavier stroke on outline buttons and light swatches. |

Focus and selection both use ink (`--border-focus`, `--border-selected`), never
coral. Coral means "act"; ink means "selected".

### Semantic

| Name | Hex | Token | Use |
|---|---|---|---|
| Sale / Error | `#C13515` | `--color-sale`, `--color-error` | Sale prices, sale badges, form validation errors. Deliberately distinct from coral. |
| Error Hover | `#B32505` | `--color-error-hover` | Hover on error links. |
| Success | `#4E7C59` | `--color-success` | Confirmation states. |
| Coming Soon | `#460479` | `--color-coming-soon` | "Coming soon" badges and price placeholders only. |
| Legal Link | `#428BFF` | `--color-legal-link` | Inline links inside legal copy only. |

### Fabric Swatches

These describe **products, never interface**. They exist so colour swatches on a
product card match the garment. Do not use them for backgrounds, buttons or text.

Blush `#EDAFB6` · Sage `#A8B79B` · Navy `#1F2A52` · Oat `#F1E7D6` ·
Charcoal `#3B3F46` · Black `#16181C` · White `#FBFAF7` ·
Dusty Rose `#C4798C` · Sky `#9FB8D4`

## 6. Colour Usage Rules

- Warm Ivory is the page background. Soft White is for cards and raised surfaces.
- Ink for headings and prices, Body for paragraphs, Muted for metadata.
- Coral marks the primary action and nothing else. One primary action per view.
- Selected and focused states are ink, never coral.
- Sale red is not coral. Never substitute one for the other.
- Fabric swatch colours describe products only.
- Do not rely on colour alone to communicate meaning.
- All text and controls must maintain accessible contrast.

## 7. Typography

Two families, both loaded from Google Fonts in `layout/theme.liquid`:

- **Quicksand** (`--font-display`) — headings. Weights 300–700; the system uses
  600 for nearly everything. Rounded terminals, which is why it carries the
  brand.
- **Nunito Sans** (`--font-sans`, `--font-body`) — body, interface, buttons,
  labels, prices. Weights 300–900.

Both fall back to `-apple-system, system-ui, sans-serif`.

A third face, **SoftRounds Custom** (`.sr-wordmark`), is the logo-matched
display font. Its non-logo characters are stylistically reconstructed rather
than original and it has no bold, so it is restricted to short logo-adjacent
display text. Never body copy, never small text, never a paragraph.

Avoid:

- Script fonts
- Weights below 300
- Excessive uppercase text
- Body text below 14px

## 8. Type Scale

Every role below is a token triplet in `storefront-import-tokens.css`
(`--type-<role>-size`, `-weight`, `-line`, and `-tracking` where non-zero).

| Role | Size | Weight | Line | Tracking | Use |
|---|---|---|---|---|---|
| `hero` | 52px | 600 | 1.05 | -1.2px | Homepage hero headline only |
| `display-xl` | 36px | 600 | 1.15 | -0.6px | Section headings, page titles, collection titles |
| `display-lg` | 28px | 600 | 1.2 | -0.4px | Product titles |
| `display-md` | 22px | 600 | 1.3 | -0.2px | Category card titles, drawer headings |
| `display-sm` | 18px | 700 | 1.35 | 0 | Sub-section titles |
| `title-md` | 16px | 700 | 1.35 | 0 | Product card names, cart line items |
| `title-sm` | 15px | 600 | 1.35 | 0 | Footer column heads |
| `body-md` | 16px | 400 | 1.6 | 0 | Default running text |
| `body-sm` | 14px | 400 | 1.5 | 0 | Card meta, review copy |
| `price` | 17px | 700 | 1.3 | 0 | Card prices |
| `price-lg` | 24px | 700 | 1.25 | -0.2px | Product page price |
| `price-was` | 14px | 400 | 1.4 | 0 | Struck-through compare-at price |
| `caption` | 13px | 600 | 1.4 | 0 | Form labels, spec chip labels |
| `caption-sm` | 12px | 400 | 1.4 | 0 | Legal line, footer bottom |
| `badge` | 11px | 700 | 1.2 | 0.2px | Card badges |
| `micro-label` | 12px | 700 | 1.3 | 0 | Dense micro-labels |
| `uppercase-tag` | 10px | 700 | 1.2 | 0.6px | Uppercase tags ("NEW") |
| `button-md` | 15px | 700 | 1.25 | 0 | Primary button labels |
| `button-sm` | 13px | 700 | 1.3 | 0 | Pill and chip labels |
| `link` | 14px | 600 | 1.5 | 0 | Inline links |
| `nav-link` | 15px | 600 | 1.3 | 0 | Header navigation |

Headings use Quicksand. Everything else uses Nunito Sans — including buttons,
prices and card titles. This is deliberate: Quicksand carries brand warmth,
Nunito Sans carries legibility at small sizes.

### Responsive step-down

Section headings drop one role at a time rather than scaling fluidly:
`display-xl` at desktop, `display-lg` below 1080px, `display-md` below 744px.
Dawn's generic `h1`–`h4` in `base.css` follow the same ladder.

## 9. Spacing System

Base unit 4px, with a 2px micro-step.

| Token | Value | Use |
|---|---|---|
| `--space-xxs` | 2px | Hairline nudges |
| `--space-xs` | 4px | Micro spacing |
| `--space-sm` | 8px | Compact spacing, card inner padding |
| `--space-md` | 12px | Icon-to-text spacing |
| `--space-base` | 16px | Standard internal spacing, grid gutters |
| `--space-lg` | 24px | Card padding, footer column gutters |
| `--space-xl` | 32px | Component spacing |
| `--space-xxl` | 48px | Mobile section spacing |
| `--space-section` | 64px | Desktop section band padding |

Bands are 64px vertical at desktop and 48px on mobile. Card grids stay tight at
16px — open bands, dense grids.

Avoid arbitrary spacing values unless required for responsive refinement.

## 10. Container System

| Token | Value | Use |
|---|---|---|
| `--container-page` | 1400px | Standard content width |
| `--container-narrow` | 920px | Editorial reading width |

`--container-page` must stay equal to Dawn's `page_width` theme setting.
Custom `.sr-*` sections read the token; Dawn's own sections read the setting.
If they differ, section edges misalign vertically down the page.

Horizontal page padding, matched between `.sr-container` and Dawn's
`.page-width`:

- Mobile: 16px
- 750px and up: 24px
- 990px and up: 36px

### Fixed dimensions

Nav height 76px · announcement bar 40px · button height 48px (small 38px) ·
input height 50px · size chip 46px · heart button 34px · swatch 22px
(large 34px) · cart drawer 420px.

## 11. Border Radius

| Token | Value | Applies to |
|---|---|---|
| `--radius-sm` | 12px | Inputs, card media, cart line images |
| `--radius-md` | 18px | Product cards, review cards, photo plates |
| `--radius-lg` | 28px | Category cards, product media, cart drawer leading corners |
| `--radius-xl` | 40px | Large editorial panels |
| `--radius-full` | 9999px | Buttons, badges, chips, swatches, icon buttons, quantity steppers |

Semantic aliases: `--radius-button` (full), `--radius-input` (sm),
`--radius-card` (md), `--radius-photo` (md).

Buttons and small controls are fully rounded. Cards and panels use the 18–28px
range. Nothing in the interface has a hard 0px corner except the page body.

## 12. Borders and Shadows

Default border: 1px solid `--border-default` (`#DDDDDD`). Focus rings are 2px
ink, offset 2px.

Three elevation tiers, all in `--shadow-*`:

| Token | Value | Use |
|---|---|---|
| `--shadow-soft` | `0 1px 2px rgba(0,0,0,.04), 0 6px 16px rgba(0,0,0,.06)` | Cards and floating badges at rest |
| `--shadow-pop` | `0 2px 4px rgba(0,0,0,.05), 0 16px 32px rgba(0,0,0,.12)` | Cards on hover, paired with a `-4px` lift |
| `--shadow-overlay` | `0 8px 40px rgba(0,0,0,.18)` | Cart drawer and modals |

Shadows are wide and low-opacity — depth without weight. Never add a fourth
tier; use spacing or a hairline instead.

## 13. Buttons

All buttons are fully rounded, 48px minimum height (small variant 38px), label
in Nunito Sans 15px/700, and squash to `scale(0.97)` on press. Focus shows a 2px
ink outline at 2px offset.

| Variant | Class | Fill | Label | Hover |
|---|---|---|---|---|
| Primary | `.sr-btn--primary` | Coral | White | Coral Press |
| Secondary | `.sr-btn--secondary` | White, 1.5px ink border | Ink | Surface Soft fill |
| Tertiary | `.sr-btn--tertiary` | None | Ink | Underline |
| Soft | `.sr-btn--soft` | Coral Wash | Coral Press | Coral Soft |
| Ink | `.sr-btn--ink` | Ink | White | Body |

Disabled primaries take the Coral Soft fill and `cursor: not-allowed`.

One primary button per view. If two actions look equally important, one of them
is secondary.

### Text Link

- Clear underline or directional icon
- Visible hover state
- Visible keyboard focus
- Must not rely on colour alone

### Text Link

- Clear underline or directional icon
- Visible hover state
- Visible keyboard focus
- Must not rely on colour alone

Preferred labels:

- Shop compression socks
- Explore scrubs
- View new arrivals
- Choose your size
- Add to cart
- View collection

Avoid vague labels such as:

- Click here
- Learn more
- Submit

Use more specific wording whenever possible.

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
| `--duration-fast` | 140ms | Hover and colour feedback |
| `--duration-base` | 220ms | Interface transitions, card lift |
| `--duration-slow` | 400ms | Image zoom on category cards |
| `--ease-standard` | `cubic-bezier(0.2, 0, 0, 1)` | Everything by default |
| `--ease-pop` | `cubic-bezier(0.34, 1.56, 0.64, 1)` | Button press and card lift only |

`--ease-pop` overshoots slightly. That small bounce is the brand's one piece of
playfulness — restrict it to press and lift, never to opacity or colour.

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