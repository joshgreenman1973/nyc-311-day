# A day on the 311 line — NYC service-request explorer

Pick any New York City police precinct and any day, and this pulls every non-emergency 311
service request from that neighborhood that day — noise, parking, heat, potholes, rats — from
the city's own records, and rebuilds an interactive map, a timeline and a resolution breakdown.
The third of a trio, alongside the [police 911](https://joshgreenman1973.github.io/nyc-precinct-day/)
and [fire & medical](https://joshgreenman1973.github.io/nyc-fire-medical-day/) explorers.

**Live:** https://joshgreenman1973.github.io/nyc-311-day/

## Data & method
- **Source:** [311 Service Requests](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2020-to-Present/erm2-nwe9) (`erm2-nwe9`), NYC Open Data. Near-real-time. Queried live in the browser.
- **Clipped to the precinct** by point-in-polygon against the official boundaries (`y76i-bdw7`), since 311 carries no police-precinct field — matching how the police page defines a precinct.
- **"Time to close"** = created→closed timestamp. This is *resolution*, not emergency response (minutes for a police-handled call, days for a housing repair) — read each agency on its own.
- **Agency codes** are spelled out from the city's own agency list. **Families** are an editorial grouping of hundreds of raw complaint types (raw type always shown).
- No verified-condition or cross-system links; a request reflects what a resident reported.

Map tiles © OpenStreetMap contributors © CARTO.
