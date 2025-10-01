
# Water Meter Finder & Editor

Single-file web app for searching, selecting (by click or drawn rectangle), and updating water meter account numbers in an ArcGIS Online/Enterprise Feature Layer.

## Quick Start (GitHub Pages)
1. Create a new repo (e.g., `meter-finder`) and make it **Public** (or org-private with Pages enabled).
2. Add `index.html` from this bundle.
3. Commit & push.
4. In **Settings → Pages**, set:
   - Source: *Deploy from a branch*
   - Branch: `main` and root (`/`)
5. Open the Pages URL (e.g., `https://<org-or-user>.github.io/meter-finder/`).

## Using the App
- Paste your **Feature Layer URL** (the layer endpoint, not the service root).
- If the layer is not public, paste an **ArcGIS API Key** with appropriate privileges and restrict it to your site domain.
- Specify the **Account # field** (defaults to `Customer_Account_Number`).
- Search by **account or address**, **draw a rectangle** to select, or **click map features**.
- Select a feature in the list to **view details** and **update** its account number via `applyEdits`.

## Deploy on Render (Static)
- Create a new **Static Site**, connect this repo, branch `main`, publish directory `/`.
- Use the Render URL in Experience Builder (Embed by URL).

## Embed in ArcGIS Experience Builder
- Add **Embed → URL** and paste your Pages/Render URL.
- Resize the frame as desired.

## Notes
- The app auto-detects your layer's `objectIdField`.
- Fields searched: your account field, `Customer_Account_Number`, `Account`, `Service_Address`, `Address`, `FullAddres`.
- Edits require permissions; verify your key/user can edit the target layer.
