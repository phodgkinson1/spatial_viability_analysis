# spatial_viability
Geospatial machine learning pipeline for site viability &amp; retail footprint optimization of artisan food hubs. Trains XGBoost classifiers on global benchmark clusters (MXC, Portland, Austin) to map high-potential corridors in North County San Diego for a local business seeking to move from the cheap product to high price market rebrand.


Spatial Transfer Learning & Artisanal Site Viability Engine
A geospatial machine learning pipeline designed to evaluate commercial site viability and retail footprint optimization for artisanal food production hubs specializing to their market niche.

This framework trains an XGBoost classifier on national and international benchmark anchor markets—ranging from Mexico City to Portland and New York—and projects spatial viability probabilities across target corridors (such as North County, San Diego).

Key Features
Resilient OpenStreetMap Ingestion (osmnx): Includes automated endpoint fallback management and mirror redirection to bypass public Overpass API rate limits and memory timeouts.

Multi-Tier Benchmark Modeling: Incorporates spatial distribution patterns from proven success cases across diverse metropolitan typologies:

Global Epicenter: Mexico City (Molino "El Pujol", Maizajo)

Mid-Sized Metro Validation: Kansas City (Yoli Tortillería)

High-Density Urban Model: New York City (Tortillería Nixtamal)

Regional Co-op Scale: Portland (Three Sisters Nixtamal)

Chef-Driven High Growth: Austin (Nixta Taqueria)

Direct SoCal Proxy: Los Angeles & Orange County (Kernel of Truth Organics)

Demographic & Commercial Feature Engineering: Integrates median income percentiles, educational attainment ratios (pct_bachelors), and local commercial/craft density scores.

Interactive Folium Mapping: Generates color-coded spatial probability overlays (.html) highlighting high-potential target zones for retail establishment and distribution hubs.

Pipeline Architecture
Step 1: Benchmark Training Corpus Ingestion — Pulls global artisan food hubs, craft mills, and organic markets with synthetic spatial fallbacks for robust baseline training.

Step 2: Target Corridor Ingestion & Boundary Processing — Handles municipal geocoding for target areas (e.g., Carlsbad, Encinitas, Vista, San Marcos) with State Plane coordinate projection (EPSG:2230).

Step 3: Supervised Classification & Pseudo-Absence Generation — Generates spatial background pseudo-absences and trains a gradient boosted decision tree (XGBoost) on relative craft density and demographic variables.

Step 4: Spatial Probability Scoring & Visualization — Computes viability probabilities across target census tracts and exports an interactive HTML choropleth map.

Tech Stack
Python 3.13

Geospatial: osmnx, geopandas, shapely

Machine Learning: xgboost, scikit-learn, numpy, pandas

Visualization: folium
