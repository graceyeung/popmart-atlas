# Pop Mart Atlas: Pop Mart stores around the world

**🌍 [View the live site](https://graceyeung.github.io/popmart-atlas/)**

An interactive, single-page map of Pop Mart retail stores worldwide (flagships, stores and pop-ups).

## Features
- Interactive 3D globe (D3 orthographic projection, Natural Earth country outlines): drag to spin, scroll or pinch to zoom, gently auto-rotates until you touch it
- Zoom, pause/resume spin and reset-view buttons; selecting a store flies the globe to it
- Nearby stores group into numbered gumball bubbles (pie-coloured by store type) that split apart as you zoom in; tapping a bubble zooms in or lists its stores
- "Store bars" view: a stacked column per city, height = number of stores, coloured by type; tap a column to list that city's stores
- Opening timeline: drag the slider back in time or press play to watch stores appear month by month (new openings pulse). Stores with no known or only planned opening date appear only at "Now"
- Colour-coded markers by store type, with a legend
- Popups with name, address, type, opening date and a "Get directions" link (Google Maps)
- Sidebar search (city, country, store name), country/region and type filters, live count
- Clickable store list that flies the globe to each store
- Stats panel: total stores, number of countries, top 5 countries
- "Near me" button using browser location (tap-the-map fallback)
- Mobile layout with a bottom drawer

## Files
- `index.html`: the whole site (HTML, CSS, JavaScript and data in one file)

## Updating the data
Store data lives in the JSON array inside the `<script type="application/json" id="store-data">` tag in `index.html`. One store per line, with fields:
`name, country, city, address, type (flagship | standard | popup), opened, lat, lng, status (verified | unverified), note, source`.
Change the `"updated"` date at the top of the JSON when you edit it.

## Data notes
Data last updated 23 November 2026. It lists 155 stores, about 23% of the 676 stores Pop Mart reported at 30 June 2026. Mainland China is still under-represented (25 stores listed of about 455). Several China entries come from an investor's store-tracking post and are marked unverified. Coordinates are approximate (mall or street level). Sources are listed in the page footer.

## Running locally
Open `index.html` in a browser, or use the VS Code "Live Server" extension.
