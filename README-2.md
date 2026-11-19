# PantryGains

A high-protein recipe finder and workout planner for gym-goers, built with **pure HTML and CSS** (no JavaScript, no database).

Tick the ingredients you have in your pantry and the recipes you can cook right now light up. A second page offers a simple push, pull, legs routine with a recipe suggestion for after each session.

**Live demo:** https://kbytyci24.github.io/pantrygains/

## Features

- **Pantry recipe finder:** 10 ingredients and 7 high-protein recipes. A recipe becomes "ready" when you have everything it needs.
- **Filter:** a toggle to show only the recipes you can make.
- **Live counters:** the number of picked ingredients and ready recipes updates as you click.
- **Workout page:** push, pull and legs tabs with exercises, sets, reps and rest times, plus a weekly plan.
- **Light and dark theme:** switch with the button in the header.
- **Responsive design:** works on desktop, tablet and mobile.

## How it works without JavaScript

| Feature | CSS technique |
| --- | --- |
| Ingredient chips and filter toggle | Hidden checkboxes styled through their `<label>` |
| Recipes lighting up | The `:has()` selector checks which checkboxes are ticked |
| Picked and ready counters | CSS counters (`counter-reset`, `counter-increment`) |
| Workout tabs | Radio buttons and the general sibling selector (`~`) |
| Exercise numbering | CSS counters |
| Dark theme | A hidden checkbox that changes CSS custom properties |
| Layout | CSS Grid and Flexbox with media queries |

## Project structure

```
pantrygains/
├── index.html      Recipes page (home)
├── workouts.html   Workouts page
├── style.css       Shared styles for both pages
└── README.md
```

## Run locally

1. Download or clone the repository.
2. Open `index.html` in a browser, or use the Live Server extension in VS Code.

An internet connection is needed to load the Google Fonts and the Unsplash photos.

## Known limitations

- The "Reset pantry" button restores the starting selection instead of clearing everything, because that is how HTML forms reset without JavaScript.
- The theme choice is not remembered when you switch pages.
- Browsers need to support the `:has()` selector (current Chrome, Edge, Safari and Firefox do).
- Nutrition values are rough estimates.

## Credits

- Design prototyped in Figma Make, then rebuilt in HTML and CSS.
- Food photos from [Unsplash](https://unsplash.com).
- Fonts: [Archivo Black](https://fonts.google.com/specimen/Archivo+Black) and [Inter](https://fonts.google.com/specimen/Inter).

## Author

Kersild Bytyci, Web Technologies course project, Epoka University.
