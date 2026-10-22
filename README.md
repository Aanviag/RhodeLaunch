# Rhode Launch
Rhode Launch.... Know the local economy before you sign the lease. 
Rhode Launch is a web app that helps aspiring entrepreneurs evaluate the real-world feasibility of starting a small business anywhere in Rhode Island using live public data instead of guesswork. Built for the Congressional App Challenge.

**What it does :** Users select a county, a business type, a monthly rent budget, and a planned number of employees. The app generates a formation feasibility score built from five weighted factors: Household demand Median household income + 5-year income growth, Census ACS 5-Year Estimates Labor cost headroom Estimated average weekly wage vs. staffing/rent plan, Census ACS 5-Year Estimates Market depth County business establishment density, Census County Business Patterns Institutional support Chambers, SBA counselors, and lenders serving the county Curated local resources directory, Labor stability County unemployment rate BLS Local Area Unemployment Statistics (LAUS)

The score and its breakdown are shown with hand-built Canvas charts (a radar chart for the breakdown, a bar chart for county comparisons).
Beyond the estimator, the app includes:
County Snapshot : compare all five RI counties side-by-side across any metric Resources directory, filterable list of real local organizations (SBA counseling, mentoring, chambers of commerce, state agencies) that can help a founder improve their odds.
Saved scores: create an account to save and revisit past feasibility runs Live data, with honest fallbacks.
The app fetches data from three live government APIs on page load: U.S. Census Bureau- American Community Survey (ACS) 5-Year Estimates U.S. Census Bureau - County Business Patterns (CBP), U.S. Bureau of Labor Statistics - Local Area Unemployment Statistics (LAUS)

Each data point is fetched independently. If any individual metric fails to load (rate limit, connectivity issue, changed data vintage, etc.), only that specific metric falls back to a cached, clearly-labeled snapshot - the rest of the live data is unaffected. The UI always tells you whether you're looking at live or fallback data.

**Tech stack**

HTML, CSS, and vanilla JavaScript. All charts (radar chart, bar chart, animated line chart) hand-written with the Canvas 2D API. 

**Project structure**
index.html # Main app (estimator, county snapshot, resources, saved scores) 
login.html # Sign in / create account 
script.js # Data fetching, scoring logic, chart rendering, app state 
auth.js # Client-side accounts + score storage 
login.js # Login page interactions + animated chart 
style.css # Shared design system 
login.css # Login page styles


**A note on accounts**

Accounts and saved scores are stored in the browser's local Storage, in plain text, with no server involved

Data sources:  U.S. Census Bureau - American Community Survey, U.S. Census Bureau - County Business Patterns, U.S. Bureau of Labor Statistics - Local Area Unemployment Statistics. 


