# Soft Rounds Australia Shopify Project Plan

## Project Goal

Build a premium, clean, responsive and conversion-focused Shopify Online Store
2.0 theme for Soft Rounds Australia.

Initial product categories:

- Nursing compression socks
- Premium healthcare scrubs

The finished store must be:

- Mobile-first
- Easy to navigate
- Easy to maintain
- Editable through Shopify theme settings
- Accessible
- Fast
- Professional
- Consistent with `brand.md`
- Consistent with `design.md`
- Safe to publish only after full QA

## Working Rules

Before beginning any phase:

1. Read `AGENTS.md`, `design.md`, and `brand.md`.
2. Confirm Git is clean.
3. Explain the intended changes.
4. List all files expected to change.
5. Preserve Dawn commerce functionality.
6. Make the smallest coherent change.
7. Run `shopify theme check`.
8. Review desktop and mobile behaviour.
9. Report confirmed results and unverified assumptions.
10. Commit only after testing.

Do not:

- Publish the theme automatically
- Push the theme without approval
- Modify checkout
- Add unsupported claims
- Add fake reviews
- Add fake urgency
- Hardcode product data
- Install unnecessary dependencies
- Make unrelated changes

---

## Phase 0 — Project Foundation

Status: Complete

### Completed

- [x] Shopify store created
- [x] Local Shopify theme created
- [x] Dawn 15.5.0 imported
- [x] Shopify CLI connected
- [x] Claude Code installed
- [x] Git repository initialised
- [x] `AGENTS.md` created and customised
- [x] `CLAUDE.md` linked to `AGENTS.md`
- [x] `design.md` created
- [x] `brand.md` created
- [x] Theme Check baseline recorded

### Baseline Theme Check

- 169 files inspected
- 0 errors
- 8 warnings
- Warnings are inherited from Dawn 15.5.0

---

## Phase 1 — Global Design Tokens

Status: Complete — reworked 2026-08-05

### Objective

Translate the Soft Rounds design system into reusable global theme settings and
CSS variables.

### 2026-08-05 rework

The original Phase 1 built a slate-blue / sage / clay palette with no token
layer — colours were written straight into `assets/base.css` and
`config/settings_data.json`. That has been replaced by the coral design system
ported from the earlier Soft Rounds build:

- Added `assets/storefront-import-tokens.css` — the full token layer (colour,
  type roles, spacing, shape, elevation, layout, motion) and the only place
  design values are defined.
- Added `assets/component-softrounds.css` — the `.sr-*` component classes plus
  the Dawn selector overrides that retune cards, header, footer, collection,
  product and cart drawer.
- Repalette: Warm Ivory page floor `#F7F5F0`, Soft White cards, Ink `#222222`
  text, Coral `#F26B6B` as the single accent. Slate blue, sage and clay are
  retired.
- Type: Quicksand headings and Nunito Sans body, loaded from Google Fonts in
  `layout/theme.liquid`. Dawn's `h1`–`h4` scale in `base.css` remapped to the
  token type roles.
- `design.md` sections 5–13 and 24 rewritten to describe this system.

Note: `--container-page` in the token file must stay equal to the `page_width`
theme setting (currently 1400px), or custom sections misalign with Dawn's.

### Scope

- Colour schemes
- Typography settings
- Spacing variables
- Container widths
- Border radii
- Borders
- Shadows
- Button styling
- Form styling
- Focus states
- Reduced motion rules

### Likely files

- `config/settings_schema.json`
- `config/settings_data.json` only if strictly necessary
- `assets/base.css`
- Relevant layout or CSS variable files

### Acceptance criteria

- [x] Soft Rounds colour palette available in theme settings
- [ ] Typography options available in theme settings
- [x] Global CSS variables added
- [x] Buttons align with design system
- [x] Forms align with design system
- [x] Focus states remain visible
- [x] No new Theme Check errors
- [x] Desktop and mobile preview verified

---

## Phase 2 — Header and Announcement Bar

Status: Complete

### Objective

Create a clean, premium and accessible header using Shopify navigation settings.

### Scope

- Announcement bar
- Logo presentation
- Desktop navigation
- Mobile navigation
- Search
- Account
- Cart
- Sticky behaviour
- Menu spacing
- Focus states
- Touch targets

### Likely files

- `sections/header.liquid`
- `sections/header-group.json`
- `snippets/header-drawer.liquid`
- `snippets/header-dropdown-menu.liquid`
- `snippets/header-mega-menu.liquid`
- `snippets/header-search.liquid`
- Related CSS assets

### Acceptance criteria

- [x] Menu items remain managed in Shopify
- [x] Search works
- [x] Cart works
- [x] Account link works
- [x] Mobile drawer works
- [x] Keyboard navigation works
- [x] Touch targets are accessible
- [x] No hardcoded navigation links
- [x] No new Theme Check errors

### Notes

- Final logo remains pending.
- The temporary text-based store name is being used.
- Navigation and footer links were configured in Shopify Admin.
- Desktop and mobile navigation were visually tested.

---

## Phase 3 — Footer

Status: Not started

### Objective

Create a professional, compact and configurable footer.

### Scope

- Brand summary
- Navigation menus
- Contact details
- Newsletter form
- Social links
- Policies
- Payment icons
- Copyright

### Likely files

- `sections/footer.liquid`
- `sections/footer-group.json`
- Related CSS assets

### Acceptance criteria

- [ ] Footer content editable in Shopify
- [ ] Newsletter form works
- [ ] Policy links remain dynamic
- [ ] Social links remain configurable
- [ ] Mobile layout is clear
- [ ] No hardcoded business information
- [ ] No new Theme Check errors

---

## Phase 4 — Homepage Structure

Status: In Progress

### Objective

Build a complete homepage that clearly explains the brand and directs customers
to key products.

### Recommended order

1. Announcement bar
2. Header
3. Hero
4. Shop by category
5. Best sellers
6. Brand benefit strip
7. Featured compression socks
8. Featured scrubs
9. Brand story
10. Genuine reviews when available
11. Email signup
12. Footer

### Likely files

- `templates/index.json`
- Existing homepage sections
- New custom sections where required

### New section candidates

- `sections/soft-hero.liquid`
- `sections/shop-by-category.liquid`
- `sections/brand-benefits.liquid`
- `sections/brand-story.liquid`

### Acceptance criteria

- [x] Homepage order matches the approved structure
- [x] All major content editable in Shopify
- [x] No hardcoded products or collections
- [x] Hero works on mobile and desktop
- [x] Images use responsive Shopify image filters
- [x] No fake reviews
- [x] No unsupported claims
- [x] No new Theme Check errors

### 2026-08-05 rebuild

The stock-Dawn homepage (`image-banner`, `collection-list`, `multicolumn`,
`featured-collection`) was replaced with the design-system sections ported from
the earlier build. Existing copy was carried across; the brand-story
`image-with-text` section was kept as-is.

Current order: hero-storefront, category-tiles, featured-collection,
feature-strip, image-with-text.

Sections added: `hero-storefront`, `category-tiles`, `feature-strip`,
`reviews`, `coming-soon`. Each gained the Dawn `{% style %}` padding block —
the originals emitted `section-<id>-padding` on the wrapper but never defined
it, so their padding settings did nothing.

Claim-bearing and fabricated schema defaults were stripped from the ported
sections (see Remaining work).

### Remaining work

- Final logo
- Real hero photography
- Collection images
- Real product images
- **Products.** The store currently has 0 products, so the homepage grid shows
  Dawn's placeholder cards and `/collections/all` is empty.
- **Reviews section.** `sections/reviews.liquid` is installed but deliberately
  not placed on the homepage. It shipped with fabricated reviews as schema
  defaults (named authors, a 4.8/214 average, Verified pre-ticked). Those
  defaults are now blank and the Verified checkbox defaults to off. Only add
  this section once genuine review data exists.
- **Self-hosting Quicksand and Nunito Sans.** They load from Google Fonts,
  which is the sole source of the 3 new Theme Check `RemoteAsset` warnings and
  a third-party request on every page. Serving the woff2 files from `assets/`
  would clear both.
- Final product catalogue
- Final homepage copy review
- Final visual QA

---

## Phase 5 — Product Cards

Status: Not started

### Objective

Create consistent, premium and accessible product cards.

### Scope

- Product image ratio
- Product title
- Price
- Compare-at price
- Sale state
- Sold-out state
- Optional secondary image
- Genuine badges
- Swatches where available

### Likely files

- `snippets/card-product.liquid`
- `snippets/price.liquid`
- `snippets/swatch.liquid`
- `snippets/swatch-input.liquid`
- Related CSS assets

### Acceptance criteria

- [ ] Works without hover
- [ ] Long product titles display correctly
- [ ] Sale pricing is accurate
- [ ] Sold-out state is accurate
- [ ] No fake ratings
- [ ] No fake stock messages
- [ ] Product URLs remain dynamic
- [ ] No new Theme Check errors

---

## Phase 6 — Collection Pages

Status: Not started

### Objective

Create clean, responsive collection pages with usable filtering and sorting.

### Scope

- Collection banner
- Collection description
- Product count
- Filters
- Sorting
- Product grid
- Pagination
- Empty state

### Likely files

- `templates/collection.json`
- `sections/main-collection-banner.liquid`
- `sections/main-collection-product-grid.liquid`
- `snippets/facets.liquid`
- `snippets/card-product.liquid`

### Acceptance criteria

- [ ] Filters work
- [ ] Sorting works
- [ ] Product count is accurate
- [ ] Empty collection state works
- [ ] Mobile filtering is usable
- [ ] No hardcoded collections
- [ ] No new Theme Check errors

---

## Phase 7 — Product Page

Status: Not started

### Objective

Create a clear, premium product page that supports confident purchasing.

### Recommended order

1. Product gallery
2. Product title
3. Price
4. Genuine review summary if available
5. Short benefit statement
6. Variant selector
7. Size guide
8. Quantity
9. Add to cart
10. Payment information
11. Shipping and returns summary
12. Product details
13. Materials and care
14. Fit information
15. Compression information where relevant
16. Related products

### Likely files

- `templates/product.json`
- `sections/main-product.liquid`
- `snippets/product-media-gallery.liquid`
- `snippets/product-media.liquid`
- `snippets/product-media-modal.liquid`
- `snippets/buy-buttons.liquid`
- `snippets/product-variant-picker.liquid`
- `snippets/product-variant-options.liquid`
- `snippets/price.liquid`

### Acceptance criteria

- [ ] Variant selection works
- [ ] Sold-out variants work
- [ ] Product media works
- [ ] Add to cart works
- [ ] Dynamic checkout remains available if enabled
- [ ] App blocks remain supported
- [ ] Size guide is configurable
- [ ] No unsupported medical claims
- [ ] No hardcoded product information
- [ ] No new Theme Check errors

---

## Phase 8 — Cart

Status: Not started

### Objective

Create a clear and trustworthy cart experience.

### Scope

- Cart drawer
- Cart page
- Quantity controls
- Remove item
- Subtotal
- Discounts
- Checkout button
- Shipping note
- Empty cart state

### Likely files

- `templates/cart.json`
- `sections/main-cart-items.liquid`
- `sections/main-cart-footer.liquid`
- `sections/cart-drawer.liquid`
- `snippets/cart-drawer.liquid`
- `snippets/cart-notification.liquid`

### Acceptance criteria

- [ ] Add to cart works
- [ ] Quantity changes work
- [ ] Remove item works
- [ ] Empty cart state works
- [ ] Subtotal is accurate
- [ ] Checkout link remains native Shopify
- [ ] No misleading urgency
- [ ] No new Theme Check errors

---

## Phase 9 — Search

Status: Not started

### Objective

Create a clean search experience for desktop and mobile.

### Scope

- Header search
- Predictive search
- Search results page
- Empty search state
- Product cards
- Article and page results where applicable

### Likely files

- `templates/search.json`
- `sections/main-search.liquid`
- `sections/predictive-search.liquid`
- `snippets/header-search.liquid`

### Acceptance criteria

- [ ] Predictive search works
- [ ] Full search works
- [ ] Empty results state works
- [ ] Keyboard interaction works
- [ ] Mobile search is usable
- [ ] No new Theme Check errors

---

## Phase 10 — Forms and Content Pages

Status: Not started

### Objective

Ensure forms and standard pages are clear, accessible and consistent.

### Scope

- Contact page
- Newsletter
- Customer account forms
- Login
- Registration
- Password reset
- Article pages
- Standard pages
- Policy pages

### Acceptance criteria

- [ ] Visible labels
- [ ] Clear error messages
- [ ] Accessible focus states
- [ ] Mobile-friendly inputs
- [ ] Standard pages use consistent typography
- [ ] No new Theme Check errors

---

## Phase 11 — Accessibility Review

Status: Not started

### Objective

Target WCAG 2.2 AA where practical.

### Review areas

- Keyboard navigation
- Focus order
- Focus visibility
- Heading hierarchy
- Form labels
- Alternative text
- Colour contrast
- Drawer focus management
- Dialog behaviour
- Touch targets
- Reduced motion
- Screen reader labels

### Acceptance criteria

- [ ] Keyboard navigation tested
- [ ] Header and mobile menu tested
- [ ] Product forms tested
- [ ] Cart drawer tested
- [ ] Search tested
- [ ] Colour contrast reviewed
- [ ] No confirmed critical accessibility blockers

---

## Phase 12 — Performance Review

Status: Not started

### Objective

Reduce unnecessary loading and preserve responsive performance.

### Review areas

- Responsive images
- Lazy loading
- Above-the-fold hero image
- Layout shift
- JavaScript usage
- Third-party scripts
- App impact
- Autoplay media
- CSS duplication

### Acceptance criteria

- [ ] Main hero is not lazy-loaded
- [ ] Below-the-fold images are lazy-loaded
- [ ] Image dimensions are reserved
- [ ] No unnecessary dependencies
- [ ] No unnecessary autoplay video
- [ ] No confirmed critical performance blockers

---

## Phase 13 — Final Quality Assurance

Status: Not started

### Objective

Confirm production readiness before upload or publication.

### Required tests

- [ ] Theme Check run
- [ ] Compare Theme Check against baseline
- [ ] Homepage tested
- [ ] Header tested
- [ ] Footer tested
- [ ] Collection tested
- [ ] Product page tested
- [ ] Variant selection tested
- [ ] Sold-out state tested
- [ ] Search tested
- [ ] Cart tested
- [ ] Checkout initiation tested
- [ ] Mobile navigation tested
- [ ] Newsletter tested
- [ ] Policy links tested
- [ ] Long product titles tested
- [ ] Missing image state tested
- [ ] Empty collection tested
- [ ] Empty cart tested
- [ ] Keyboard navigation tested

### Target viewport widths

- 375px
- 430px
- 768px
- 1024px
- 1280px
- 1440px

### Final release rules

Do not publish until:

- [ ] No confirmed critical blockers remain
- [ ] No new Theme Check errors remain
- [ ] Store content is complete
- [ ] Product information is verified
- [ ] Legal policies are complete
- [ ] Shipping is configured
- [ ] Payments are configured
- [ ] Domain is configured
- [ ] Store owner explicitly approves publication