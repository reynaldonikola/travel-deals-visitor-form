# Travel Deals, visitor registration form

A single-page travel site with a visitor registration form validated entirely in vanilla JavaScript. No framework and no build step.

![Travel Deals](preview.jpg)

**Live site:** https://reynaldonikola.github.io/travel-deals-visitor-form/

## What it does

- Validates required fields, a two letter US state, a five digit zip, a phone number and an email address, each with its own message under the field
- Checks a field when you leave it and again on submit, so errors show up where you are, not at the top of the page
- Requires at least one contact method from a checkbox group
- Replaces the form with a thank you panel once everything passes
- Switches sections without a page load, keeping one HTML file
- Light and dark themes from `prefers-color-scheme`, and animations that turn off under `prefers-reduced-motion`

## How the code is organized

```
validation.js   the validation library: regexes, per-field rules, custom messages
page.js         section switching for the single page site
main.js         wires it together on DOMContentLoaded
css/main.css    design system in custom properties
index.html
images/
```

`validation.js` sets `setCustomValidity` on each field, so the browser's own form validity stays in sync with the custom messages.

## Running it

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Credits

Photography generated for this project; the parks shown are generic. Built by Reynaldo Moros as coursework at Utah Valley University.
