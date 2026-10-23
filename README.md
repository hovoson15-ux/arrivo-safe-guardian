# Arrivo Safe · Guardian page

The page guardians open from the text message, e.g.
`https://hovoson15-ux.github.io/arrivo-safe-guardian/#t=<walk code>`

- No login or app needed. It shows the walker's live position, expected arrival time, battery and last update, and switches to a red SOS view or an "arrived safely" view.
- The walk code sits after `#`, so browsers never send it to any server (not even GitHub).
- Data comes from the Supabase function `get_shared_walk`, which only returns a location while the walk is active or in SOS. After arrival it returns nothing about location.
- The key in `index.html` is Supabase's **publishable** key, which is meant to be public.
- The map is MapLibre GL 4.7.1 (bundled in `maplibre/`) with free OpenFreeMap street maps (© OpenMapTiles, © OpenStreetMap contributors). If the map can't load, the page says so and the Google Maps button still works.

The main app lives in the private repo `hovoson15-ux/arrivo-safe` (a copy of this page is in `guardian-page/` there).
