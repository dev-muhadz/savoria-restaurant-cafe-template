# Savoria — Restaurant & Cafe Menu Showcase

A modern, mobile-first restaurant/cafe marketplace template built with semantic HTML5, CSS3 and Vanilla JavaScript only.

## Features
- Immersive homepage hero and opening hours
- Daily specials and customer review slider
- Interactive menu category and dietary filters
- Accessible filter state announcements with `aria-pressed`
- Menu pricing, descriptions and dietary badges
- Reservation date/time controls and guest counter
- Client-side form validation and confirmation modal
- Keyboard-friendly mobile navigation and modal focus management
- Accessible review controls and live slide counter
- Sticky scrolling header
- Page-specific canonical, Open Graph and Twitter metadata
- CSS custom properties for colors, fonts, radii and spacing
- No external CSS/JS frameworks

## Structure
```text
savoria-restaurant-cafe-template/
├── index.html
├── menu.html
├── reservation.html
├── README.md
├── css/styles.css
├── js/main.js
└── images/
```

## Rebrand
Edit the `:root` variables in `css/styles.css`:
```css
:root {
  --ink: #1d211e;
  --paper: #f7f4ee;
  --accent: #c86b3c;
  --body: "DM Sans", Arial, sans-serif;
  --display: "Playfair Display", Georgia, serif;
}
```
Change these values to update the visual system globally.

## Menu editing
Menu items live in `menu.html` as `.menu-item` articles. Use `data-category` values such as `breakfast`, `lunch`, `dinner`, and `drinks`. Use `data-diets` values `vegan`, `gluten-free`, and `spicy`, separated by spaces. Add or remove badges inside `.badges` as needed.

Example:
```html
<article class="menu-item" data-category="dinner" data-diets="vegan gluten-free">
  <div class="menu-item-image"><img src="dish.jpg" alt="Dish name"></div>
  <div>
    <div class="menu-item-top"><h2>Dish Name</h2><strong>$22</strong></div>
    <p>Short description.</p>
    <div class="badges"><span class="badge vegan">Vegan</span><span class="badge gf">GF</span></div>
  </div>
</article>
```

## JavaScript
`initMobileNavigation()` handles the hamburger menu and keyboard focus. `initStickyHeader()` changes the header after scrolling. `initMenuFilters()` filters menu items without a reload and exposes active filter state. `initReviewSlider()` powers the homepage review carousel. `initReservationForm()` handles date constraints, guest controls, validation and the confirmation modal with keyboard focus management.

## Accessibility
The mobile navigation and reservation confirmation modal support Escape-to-close and keyboard focus management. Menu filters expose their selected state through `aria-pressed`, and review controls include accessible labels with a live slide counter.

## Images
The demo uses Unsplash image URLs as placeholders. For a commercial marketplace release, replace them with images you are licensed to distribute, preferably optimized WebP/AVIF assets in the `images/` directory.

## Marketplace tips
Use a strong preview screenshot, provide alternate color presets, keep the JS dependency-free, optimize food photography, make every demo link functional, and document customization clearly. Restaurant buyers respond strongly to visual polish and easy menu editing.
