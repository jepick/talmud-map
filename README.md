# מפת התנאים והאמוראים — Talmudic Sages Map

An interactive map and timeline of the Tannaim and Amoraim — the sages of the Mishnah and Talmud — showing where they lived, when they flourished, and which pages of Masechet Chullin they appear on.

**Live site:** [https://jepick.github.io/talmud-map/](https://jepick.github.io/talmud-map/)

---

## What it does

### 🗺️ Interactive Map
- Every sage appears as a colored dot on a real map (OpenStreetMap), positioned at the city where they primarily taught
- Dot color indicates generation — Tannaim in gold/purple tones, Amoraim in warm/red tones
- Sages from the same city are clustered with slight overlap so each one is individually hoverable
- **Hover** over any dot to see a popup with the sage's name, generation, role, city, and a brief description
- **Click** any dot to open the full timeline chart and highlight that sage's entry

### ⏱️ Generation Timeline
- The slider moves through history from ~10 CE to ~500 CE
- Only the sages alive during the selected period appear on the map
- **Generation labels** (ת׳ א through א׳ ו) are clickable — click any one to jump straight to that generation
- **Historical event markers** below the slider show key moments in context:
  - 🔴 Churban HaBayit — Destruction of the Second Temple (70 CE)
  - 🟠 Wars — Revolt of the Diaspora (115), Bar Kokhba Rebellion (135)
  - 🔵 Texts — Codification of the Mishnah (~220), Jerusalem Talmud (~370), Babylonian Talmud (~500)
  - 🟣 Political — Edict of Milan (312), Abolition of the Patriarchate (425)
- Click any event marker to jump the timeline to that year

### 📜 Timeline Chart
- Opens as a slide-out panel from the left
- Shows all 78 sages grouped by generation
- Click any name to jump the map to their location and highlight their dot
- In daf mode (see below), filters to show only the sages on that specific page

### 📖 Masechet Chullin Daf Selector
- Dropdown covering all 281 pages of Masechet Chullin (2a–142a)
- Selecting a **verified page** shows only the sages cited on that specific daf:
  - All other markers disappear so the map is uncluttered
  - Each sage appears as a colored dot (color = generation)
  - The map resets to a fixed view showing both the Land of Israel and Babylonia together
  - The chart filters to show only those sages, grouped by generation
  - Hover a dot or a name to see the sage's details
  - Click a name in the chart to pan the map to that sage (without resetting the zoom)
  - Click the same dot or name again to deselect
- Pages not yet verified show a clear ⚠️ warning rather than appearing empty

### 🖨️ Print Reference Table
- Click **"הדפס טבלה"** to print a single-page A4-landscape reference chart of all sages, organized by generation with roles and approximate dates

---

## Current Data

| | Count |
|---|---|
| Total sages | 78 |
| Tannaim | 26 |
| Amoraim | 52 |
| Chullin dapim verified | ~16 |

Sages covered span from Hillel and Shammai (~10 CE) through the Savoraim (~500 CE), including major figures from both the Land of Israel (Tiberias, Caesarea, Tzippori, Jerusalem, Yavneh) and Babylonia (Sura, Pumbedita, Nehardea, Mahoza).

### Date honesty
Exact birth and death years are **not** historically documented for nearly all Tannaim and Amoraim — ancient rabbinic sources essentially never record them. Every sage therefore displays only their **generation's approximate range** (e.g. ~80–~120 for Tannaim Generation 2), marked with `~` to make clear these are scholarly approximations, not personal dates. A small number of figures have a genuinely attested year (e.g. Rabbi Akiva's death tied to the Bar Kokhba revolt) — these are noted where used.

### Chullin daf citations
Sage citations for each daf are verified against the actual Talmud text via [Sefaria.org](https://www.sefaria.org). Pages marked ✓ have been individually checked; pages marked ⚠️ have not yet been verified and show no sages rather than guessing.

---

## Sources

- **Talmud text and citations** — [Sefaria.org](https://www.sefaria.org) (William Davidson Edition)
- **Rabbinic chronology** — Heinrich Graetz periodization; Encyclopaedia Judaica generational framework
- **Map tiles** — [OpenStreetMap](https://www.openstreetmap.org/) contributors via Esri/CARTO basemaps
- **Historical events** — Standard dates per Encyclopaedia Judaica and general Jewish historiography

---

## Technical

Built as a single self-contained HTML file with no build step or server required — just open `index.html` in any modern browser.

- **Map:** [Leaflet.js](https://leafletjs.com/) 1.9.4
- **Tiles:** Esri World Street Map (English labels, no API key required), with automatic fallback to CARTO Voyager and OpenStreetMap
- **Fonts:** Noto Serif Hebrew (Google Fonts)
- **No backend, no database, no tracking**

---

## License

This project is shared openly. The underlying Talmud text is in the public domain. Map tile usage is subject to [OpenStreetMap's tile usage policy](https://operations.osmfoundation.org/policies/tiles/).
