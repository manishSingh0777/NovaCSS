# NovaCSS
NovaCSS is a lightweight custom CSS framework built with Sass. It gives a clean, consistent theme for common HTML elements (headings, lists, buttons, forms, tables) and a set of utility classes you can use to style layouts faster.

## Key points

- Built with Sass and organized with Sass partials.
- Includes CSS variables and Sass maps so you can change colors, spacing, and other values in one place.
- Provides a compiled stylesheet at `css/main.css` for use in projects.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/manishSingh0777/NovaCSS.git
cd NovaCSS
```

2. Install dependencies (this installs Sass):

```bash
npm install
```

3. Build the compiled CSS:

```bash
npm run build
```

Or to rebuild automatically while you work:

```bash
npm run watch
```

4. Link the compiled CSS in your HTML (use the compiled file at `css/main.css`):

```html
<link rel="stylesheet" href="css/main.css">
```

## Usage

Below are simple examples showing how to use NovaCSS classes in your HTML.

### Buttons

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-outline">Outline</button>
```

### Utility classes

- Spacing: `.m-2` (margin), `.p-3` (padding)
- Colors: `.bg-primary`, `.text-gray-600`
- Font weight: `.fw-bold`, `.fw-light`
- Borders: `.border`, `.border-primary`

Example:

```html
<div class="p-3 m-2 bg-primary text-center">Primary background</div>
<p class="fw-bold">Bold text</p>
<div class="border border-primary p-2">Box with primary border</div>
```
### Features

- Modular Sass architecture
- Theme customization via variables & maps
- Prebuilt components
- Utility-first helpers
- Clean default HTML styling

### Forms

Use the form utility classes for consistent forms:

```html
<div class="form-group">
	<label class="label" for="email">Email</label>
	<input id="email" class="input" type="email" />
</div>
```

Inputs use `.input`, `.textarea`, and `.select`. Focus styles are applied automatically.

### Tables

Use the `.table` class for clean tables:

```html
<table class="table">
	<thead>
		<tr>
			<th>Name</th>
			<th>Role</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Alice</td>
			<td>Developer</td>
		</tr>
	</tbody>
</table>
```

## Customization

All the main customization values live in `scss/abstracts/_variables.scss`.

- Change colors: edit the `$colors` map. For example, to change the primary color update the `primary:` value.
- Change spacing: edit the `$spacing-scale` map to adjust the values used by `.m-*` and `.p-*` utilities.
- Change radius, font family, or font sizes by editing the respective variables in the same file.

After you change any Sass variables or partials, rebuild the compiled CSS with:

```bash
npm run build
```

Or run the watcher during development to auto rebuild:

```bash
npm run watch
```

## Project structure

- `index.html` — demo page showing the framework in use.
- `scss/` — all Sass source files (organized with partials):
	- `abstracts/_variables.scss` — theme variables (colors, spacing, fonts, radius).
	- `base/` — base and reset styles (`_reset.scss`, `_base.scss`, `_typography.scss`).
	- `components/` — component styles (`_buttons.scss`, `_forms.scss`, `_cards.scss`, `_navbar.scss`, `_tables.scss`, `_alerts.scss`, `_badges.scss`).
	- `utilities/` — utility classes (`_colors.scss`, `_spacing.scss`, `_typography-utils.scss`, `_borders.scss`, `_grid.scss`).
	- `main.scss` — imports every partial and is the Sass entry point.
- `css/main.css` — compiled CSS (ready to use in a site).
- `css/main.css.map` — source map for debugging.
- `package.json` — build scripts and Sass.

## Notes

- The framework is built to be simple and easy to customize. Edit `_variables.scss` to restyle the whole theme.
- Use `npm run build` to produce `css/main.css` before linking it in projects.

