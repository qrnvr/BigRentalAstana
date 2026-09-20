# CSS Checklist — Assignment 2

Student: Arnur Sadyrov  
Group: SE-2532  
Project: Big Rental Astana

## Selectors

- Universal selector `*` — `css/base.css`
- Type selector `body` — `css/base.css`
- Class selector `.product-card` — `css/arnur.css`
- ID selector `#camera-list` — `css/arnur.css`
- Descendant selector `main p` — `css/base.css`
- Child selector `.site-nav > ul` — `css/base.css`
- Child selector `.product-grid > article` — `css/arnur.css`
- Adjacent sibling selector `h2 + p` — `css/base.css`
- Grouping selector `h1, h2, h3` — `css/base.css`
- Attribute selector `a[target="_blank"]` — `css/base.css`
- Attribute selector `input[type="email"]` — `css/arnur.css`
- Universal selector `*` — `css/base.css`
- `:hover` — `.site-nav a:hover` in `css/base.css`
- `:focus` — `.site-nav a:focus` in `css/base.css`
- `:first-child` — `.site-nav li:first-child a` in `css/base.css`
- `:nth-child` — `.price-table tbody tr:nth-child(2n)` in `css/arnur.css`
- `::after` — `a[target="_blank"]::after` in `css/base.css`
- `::before` — `.cart-total::before` in `css/arnur.css`

## Classes and IDs

Reusable classes include:

- `.page-header`
- `.site-nav`
- `.page-main`
- `.content-section`
- `.product-grid`
- `.product-card`
- `.featured-card`
- `.card-badge`
- `.price-table`
- `.equipment-categories`
- `.about-float`
- `.contact-card`
- `.auth-form`
- `.cart-table`

IDs include:

- `#about`
- `#camera-list`
- `#lens-list`
- `#login-form`
- `#signup-form`
- `#rental-cart`

Comments in the HTML explain why unique IDs are appropriate.

## Colors and Typography

- Palette comment — top of `css/base.css`
- Hex colors — `css/base.css`
- RGB colors — `css/base.css`
- RGBA colors — `css/arnur.css`
- Named color `white` — `css/base.css`
- Font stack 1: `Arial, Helvetica, sans-serif` — `css/base.css`
- Font stack 2: `Georgia, "Times New Roman", serif` — `css/base.css`
- `font-size` — `css/base.css`
- `font-weight` — `css/base.css`
- `line-height` — `css/base.css`
- `letter-spacing` — `css/base.css`

## Box Model and Alignment

- `box-sizing: border-box` — `css/base.css`
- `margin` — `css/base.css`
- `padding` — `css/base.css`
- `border` — `css/base.css`
- Margin-collapse explanation comment — `css/base.css`
- `text-align` — `css/base.css`

## Cascade and Specificity

- `base.css` is linked first
- `arnur.css` is linked second
- Cascade override: `.site-nav a` appears in both stylesheets
- Exactly one internal `<style>` block — `index.html`
- Exactly one inline `style` attribute — `index.html`
- No `!important` is used

Specificity experiment:

- `.product-card.featured-card`
  - specificity: `0-2-0`
- `#camera-list .featured-card`
  - specificity: `1-1-0`
  - wins because the ID selector has higher specificity

## Flexbox

Navigation:

- `.site-nav > ul`
- `display: flex`
- `flex-direction: row`
- `flex-wrap: wrap`
- `justify-content: center`
- `align-items: center`
- `gap`

Second Flexbox example:

- `.equipment-categories`
- `display: flex`
- `flex-direction: row`
- `flex-wrap: wrap`
- `gap`
- `.equipment-categories > li` uses `flex: 1 1 280px`

## CSS Grid

Catalog grid:

- `.product-grid`
- `display: grid`
- `grid-template-columns`
- `repeat()`
- `minmax()`
- `fr`
- `gap`

Grid spanning:

- `.product-grid .featured-card`
- `grid-column: span 2`

Grid centering:

- `.product-card figure`
- `display: grid`
- `place-items: center`

A comment in `arnur.css` explains why Grid is better than Flexbox for the catalog.

## Positioning

- `position: static` — `.site-footer` in `css/base.css`
- `position: relative` — `.product-card` in `css/arnur.css`
- `position: absolute` — `.card-badge` in `css/arnur.css`
- `position: fixed` — `.fixed-rental-link` in `css/base.css`

`.product-card` is the containing block for the absolutely positioned badge.

## Float and Clear

- `float: left` — `.about-float` in `css/arnur.css`
- `clear: both` — `.clear-after-float` in `css/arnur.css`

The CSS comment explains what would happen without `clear`.

## Centering Techniques

1. Flexbox centering — `.page-header`
2. `margin: auto` centering — `.page-main`
3. Grid centering — `.product-card figure`

## Author

Arnur Sadyrov  
SE-2532