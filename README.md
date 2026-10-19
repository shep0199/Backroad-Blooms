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
- Full browser width: 1200px, 4 product columns.
- Half browser width: 600px, 1 product column.
- Auto-fit and minmax adjust the gallery without media queries.
- Footer Grid placement: line 1 to line 3, verified in DevTools.

### Product Card Measurements

- 1200px browser width: 4 columns
- Card width: 220px
- Card height: 350.5px

- 600px browser width: 1 column
- Card width: 340px
- Card height: 350.5px

- Minimum Grid column width: 220px
- Used auto-fit and minmax so the number of columns adjusts automatically without a media query.

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
Poppins is used for headings and Nunito Sans for the rest of the text.

- Main heading: 32px, line height 38.4px
- Section headings: 24px, line height 31.2px
- Product names: 16px, line height 22.4px
- About subheadings: 18px, line height 25.2px
- Body text: 16px, line height 24px
- Navigation: 16px, line height 24px
- Social media text: 13px, line height 19.5px