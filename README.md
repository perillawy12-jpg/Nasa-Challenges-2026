# Nasa-Challenges-2026
# Lunar Polar Planner

Live app: https://perillawy12-jpg.github.io/Nasa-Challenges-2026/

A web tool that compares landing sites near the Moon's south pole. Pick sites and a date range and it shows where the Sun and Earth are in the sky from each site, when solar power is available, when a direct radio link to Earth is possible, and which start dates keep both for a whole mission. NASA's south pole animation plays in sync with the chosen date.

Made for the NASA Space Apps Challenge 2026. Team: Martin Roa, Samuel Chaparro, Laura Ramírez, Contreras, Amaya, Héctor.

## Run it

Open `index.html` in a browser (keep `nasa-south-pole.mp4`, `nasa-south-pole.webm` and `nasa-poster.jpg` in the same folder). No build step, no server, no libraries.

## How it works

- Moon position, Sun position and libration use the series from J. Meeus, *Astronomical Algorithms* (chapters 47, 25 and 53), implemented in plain JavaScript.
- From those we get the sub-Earth and sub-solar points on the Moon, then the Sun and Earth azimuth and elevation at each site.
- Checked against NASA/JPL Horizons (DE441) on 25 dates in 2026: largest difference about 0.03 degrees.
- Limits: the Moon is modeled as a smooth sphere, site positions are approximate, and the dates of the NASA video were inferred (within about half a day). Real LRO terrain horizons are the next step.

## NASA data and resources

- NASA Scientific Visualization Studio, animation 5228 (Ernie Wright, USRA): https://svs.gsfc.nasa.gov/5228
- NASA/JPL Horizons System, used to validate our results: https://ssd.jpl.nasa.gov/horizons/
- NASA Artemis III candidate landing regions, as the basis for the preset sites (approximate positions): https://www.nasa.gov/news-release/nasa-identifies-candidate-regions-for-landing-next-americans-on-Moon/

## Other resources

- J. Meeus, *Astronomical Algorithms*, 2nd edition (formulas and coefficients).
- Fonts from Google Fonts: Barlow, Bricolage Grotesque, IBM Plex Mono.

## Use of Super Intelligence (SI)

The code, the text of the app and the project documents were written with the help of an SI tool (Claude, by Anthropic) and reviewed by the team. The project contains no SI-generated images, video or audio, and uses no NASA logos or mission identifiers.

This project is not affiliated with or endorsed by NASA.
