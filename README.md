
# Portland Water Meter Finder (Public)

Preconfigured for the public FeatureServer:
`https://services3.arcgis.com/DAf01WuIltSLujAv/arcgis/rest/services/Portland_Water_Meters__UBO_Version/FeatureServer`

## Features
- Auto-selects the first "meter-like" layer in the service (or layer 0 if none match).
- Search by account or address; click map to pick a meter.
- Draw a rectangle to select many; or **Select visible** to grab everything in the current extent.
- Edit the account number (configurable field name).
- Toggle `Needs_Review` flag.
- Export current selection to CSV.
- Works without API keys (layer must allow public read; edits require public edit or logged-in user in the host app).

## Deploy (GitHub Pages)
1. Create a new repo (e.g., `meter-finder-public`).
2. Upload these files.
3. Enable **Settings → Pages**: Deploy from branch `main` at root.
4. Use the Pages URL in Experience Builder **Embed (URL)** widget.

## Configure
- Expand **Settings** to change the **Account # field** (default `Customer_Account_Number`). This preference saves in localStorage.
- If your layer uses a different review field, change `Needs_Review` in `index.html` → `toggleReview()`.
