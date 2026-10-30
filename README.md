# Backroad-Blooms
UX assignment mock up - CSS assignment

## CSS Grid Assignment Notes

### Layout Decisions
- CSS Grid organizes the header, sidebar, main and footer.
- The sidebar uses a fixed width of 220px.
- The main content uses 1fr to fill the remaining space.
- CSS Grid arranges the product cards into rows and columns.
- Flexbox aligns the logo and shop name in one row.
- Flexbox stacks the sidebar navigation links vertically.

### Grid Testing

- Desktop browser width: 1200px
- Product columns: 4
- Card width: 220px
- Card height: 350.5px

- Half browser width: 600px
- Product columns: 1
- Card width: 340px
- Card height: 350.5px

- Minimum Grid column width: 220px
- Used auto-fit and minmax to adjust columns without media queries.

- Footer Grid placement: spans from line 1 to line 3.
- Confirmed in Chrome DevTools that the footer covers both columns.

### Product Card Measurements

- 1200px browser width: 4 columns
- Card width: 220px
- Card height: 350.5px

- 600px browser width: 1 column
- Card width: 340px
- Card height: 350.5px

- Minimum Grid column width: 220px
- Used auto-fit and minmax so the number of columns adjusts automatically without a media query.

# Spacing

### Layout
- Header padding: 24px top/bottom, 20px left/right
- Logo to shop name gap: 20px
- Social media text: 8px above
- Sidebar padding: 24px top/bottom, 16px left/right
- Sidebar link gap: 16px
- Main content padding: 20px (max width 1120px)
- Footer padding: 20px

### Content
- Search area: 20px above, 40px below
- Search label: 8px below
- Search input padding: 12px (max width 400px)
- Space between shop sections: 50px
- Section heading: 8px below
- Featured label: 4px below
- About section padding: 30px

### Product Cards
- Gap between cards: 20px
- Space above product grid: 20px
- Card padding: 15px
- Card image height: 180px
- Product name: 5px below
- Button padding: 10px
- Cart label padding: 10px

### Corner Radius
- Product cards: 12px
- Images, buttons, cart label and search input: 8px


### Design Adaptation Notes

My original Backroad Blooms Figma design was created for a 390px mobile screen. For this assignment, I adapted it into a desktop layout using CSS Grid, with a 220px sidebar and a flexible main content area.

I kept the same colours, fonts, branding and product sections, but changed the mobile navigation menu into a desktop sidebar.

The layout was built for desktop, so some content may overflow at smaller mobile widths.

## Colours and Fonts

### Colours
- #454D3E - Dark green (headings, sidebar, text)
- #FFFBEF - Cream (background)
- #F7D38F - Yellow (buttons and accents)
- #C27F5F - Rust (featured labels)
- #FFFFFF - White (product cards)

### Fonts
Poppins is used for headings and Nunito Sans for body text.

- Main heading: Poppins, 32px, line height 38.4px
- Section headings: Poppins, 24px, line height 31.2px
- Product names: Poppins, 16px, line height 22.4px
- About subheadings: Poppins, 18px, line height 25.2px
- Body text: Nunito Sans, 16px, line height 24px
- Navigation: Nunito Sans, 16px, line height 24px
- Social media text: Nunito Sans, 13px, line height 19.5px

### Week 7 Assignment
520px: two cards fit side by side (about 220px each) without looking cramped.
760px: enough room for the 220px sidebar beside the products, so the menu moves to the side.
960px: three cards fit beside the sidebar. The first Fall card spans the full row so the 4 Fall cards leave no gap.

### Container query
- `.product-card` is a container (`container-type: inline-size`, `container-name: product`).
- At 420px+ card width, the image sits beside the text using Grid.
- Tested in two spots: the wide featured Harvest Sunrise card (image beside text) vs. the regular cards (stay stacked) at the same screen width.

### Small-screen decisions (not shown in the desktop mockup)
- Sidebar menu:moves above the products on phones, with links in a wrapping row, so every section stays reachable without a hidden menu.
- Product cards:1 column on phones instead of a sideways scroll, keeping the same product order as desktop.
- Featured card:spans the full row at 960px+ so the Fall section stays balanced.
- Shop name: shrinks on phones with clamp() so it fits beside the logo and cart. At 320px it wraps onto two lines, which still reads clearly.
- 100dvh: not used, since there's no full-screen section.

### Fluid sizing
- Shop name: `clamp(1.5rem, 1rem + 2vw, 2rem)`
- Section headings (h2): `clamp(1.5rem, 1.25rem + 1vw, 1.75rem)`
- Section intro text and About text capped at `max-width: 65ch`
- `img { max-width: 100%; height: auto; }` applied site-wide

### Flexbox and Grid
- Flexbox: logo and shop name (`.brand`), sidebar menu (`.sidebar nav`)
- Grid: page layout (`body`), header (`.site-header`), product grid (`.product-grid`), card layout in the container query (`.card-content`)

### Testing
- Chrome DevTools: checked 320px to 1201px with no horizontal scroll.
- Iphone 13: checked header, menu, product cards and About section.
- Safari browser on Mac and Iphone