# Diani Beach → Masai Mara: 3-Day Fly-In Safari Map

An interactive 3D map of a 3-day **fly-in safari** from **Diani Beach** on Kenya's south coast to the **Masai Mara National Reserve**. The trip covers game drives around the Talek area and the **Mara Triangle**, with a stay at **Mara Intrepids Tented Camp**.

🗺️ **See the full itinerary and the live map:**
[3-dniowa przygoda safari z przelotem do Masai Mara](https://safarikenia.com.pl/3-dniowa-przygoda-safari-z-przelotem-do-masai-mara) on **Safari Kenia**

---

## The route

| Stop | Location | Accommodation / Area |
|------|----------|----------------------|
| Start | Ukunda Airstrip, Diani Beach | Flight to the Masai Mara |
| Day 1 | Talek area, Masai Mara | Mara Intrepids Tented Camp |
| Day 2 | Mara Triangle | Mara Triangle Conservancy |
| Day 3 | Return flight | Ukunda Airstrip, Diani Beach |

**Flights:** Ukunda (Diani) ⇄ Masai Mara airstrip, drawn as direct lines across Kenya.
**Game drives:** a loop through the Talek area on Day 1, then a loop through the Mara Triangle on Day 2.

The interface labels are in Polish, matching the tour page it's embedded on.

## Features

- **Flight and drive legs in one route.** Legs tagged as flights are drawn as straight air paths. Game-drive legs are fetched from the Mapbox Directions API (driving profile), so the line follows real tracks inside the reserve.
- **Satellite basemap with 3D terrain.** The map uses the Mapbox Standard Satellite style with DEM terrain (1.5× exaggeration) and a tilted camera, which shows off the Oloololo Escarpment above the Mara Triangle.
- **Animated route line.** The route is a golden "marching ants" dashed line over a soft glow layer.
- **Interactive itinerary panel.** A glassmorphism sidebar lists each day. Clicking a card flies the camera to that stop and opens its popup.
- **Custom markers.** Gold SVG pins mark the main stops. Hidden waypoints shape the game-drive loops without cluttering the map.
- **Mobile-friendly layout.** On small screens the sidebar becomes a bottom sheet, and cooperative gestures keep page scrolling smooth.
- **WordPress-ready embed.** Styles are scoped to a single container, so you can paste the code into a Custom HTML block.

## Tech stack

- [Mapbox GL JS](https://docs.mapbox.com/mapbox-gl-js/) v3.9.0
- [Mapbox Directions API](https://docs.mapbox.com/api/navigation/directions/)
- Vanilla JavaScript with no build step
- Plus Jakarta Sans (Google Fonts)

## Usage

1. Copy the HTML into a WordPress **Custom HTML** block or any web page.
2. Replace the Mapbox access token with your own and restrict it to your domain in your [Mapbox account](https://account.mapbox.com/access-tokens/).
3. Adjust the container height in `.wp-safari-itinerary-container` to fit your layout.

To change the route, edit the `itineraryData` array:

- Any stop whose `id` contains `flight` makes the legs on either side of it straight air lines instead of road routes.
- Entries with `isWaypoint: true` shape the route only.
- Every other entry gets a marker and a sidebar card.

## About

Built for [Safari Kenia](https://safarikenia.com.pl/), which offers Polish-language safari tours and travel guides for Kenya.

➡️ [View this fly-in safari itinerary](https://safarikenia.com.pl/3-dniowa-przygoda-safari-z-przelotem-do-masai-mara)
