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
- Revenue & profit: Pop Mart's reported H1 2026 group revenue and net profit, revenue by reporting region (Greater China, Asia Pacific, Americas, Europe & other), plus each store's regional figures in its popup (region revenue, retail-store revenue and store count, segment operating profit). Pop Mart does not publish per-store revenue or profit, so none is shown
- "Near me" button using browser location (tap-the-map fallback)
- Mobile layout with a bottom drawer

## Files
- `index.html`: the whole site (HTML, CSS, JavaScript and data in one file)

## Updating the data
Store data lives in the JSON array inside the `<script type="application/json" id="store-data">` tag in `index.html`. One store per line, with fields:
`name, country, city, address, type (flagship | standard | popup), opened, lat, lng, status (verified | unverified), note, source`.
Change the `"updated"` date at the top of the JSON when you edit it.

Revenue and profit figures live in the `"financials"` object in the same JSON (RMB thousand, from Pop Mart's interim results announcement for the six months to 30 June 2026). Countries map to Pop Mart's reporting regions in `FIN_REGION`; Middle East stores (Qatar, UAE) are counted under Asia Pacific, following the report's definition of Asia Pacific as Asia and Oceania outside the PRC.

## Data notes
Data last updated 24 November 2026. It lists 1,005 stores, 875 of them in mainland China. Pop Mart reported 676 stores worldwide (419 on the Chinese mainland) at 30 June 2026. Most mainland China entries come from Baidu Maps listings for 泡泡玛特 (checked 24 November 2026), with ROBO SHOP vending machines, pop-ups, places Baidu marks as closed and duplicates of hand-checked stores removed. Baidu still lists some stores that have closed or moved, so the China count runs higher than Pop Mart's figure, and these entries are marked unverified. Their names and addresses are in Chinese, and their coordinates were converted from Baidu's BD-09 system to WGS-84. Other coordinates are approximate (mall or street level). Sources are listed in the page footer.

## Running locally
Open `index.html` in a browser, or use the VS Code "Live Server" extension.
