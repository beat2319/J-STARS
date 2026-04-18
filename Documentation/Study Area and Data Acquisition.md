## 2. Study Area and Data Acquisition
#### AI
The study area encompasses the Hawaiian Archipelago, utilizing a nine-year longitudinal dataset of **Rapid ʻŌhiʻa Death (ROD)** detections. The ground truth masks were derived from an aggregated collection of aerial flyover surveys (ArcGIS StoryMap, B. Tucker). To facilitate deep learning, the study area was partitioned into **21,021 chips** of 128 $\times$ 128 pixels at a 10m spatial resolution, covering approximately 34,440 $km^2$.
#### ME
Our study area confines the Hawaiian Archipelago, which involves a nine-year longitudinal dataset of Rapid ʻŌhiʻa Death (ROD) detections. The ground truth mask are a derivative product of an aggregated collection of aerial flyover surveys (ArcGIS StoryMap, B. Tucker). To assist deep learning, the study area is divided into 21,021 chips of 128 x 128 pixels at a 10m spatial resolution, covering approximately 34,440 $km^2$.
### 2.1 Remote Sensing Data
#### AI
We utilized **Sentinel-1 SAR** data from three relative orbits (22, 95, and 124) in ascending mode. To augment the structural information from SAR, we integrated **AlphaEarth Satellite embeddings** via Google Earth Engine, providing high-level latent representations of the landscape. To ensure a robust training signal, we enforced a 1:1 balance between positive (ROD-infected) and negative (healthy canopy) chips. Negative samples were constrained using the **NLCD Tree Canopy Cover (TCC)** product with a 10% threshold to ensure the model distinguishes ROD from healthy forest rather than non-forested land.
#### ME
We employ Sentinel-1 SAR data from three relative orbits (22, 95, and 124) with ascending orbit. To supplement the structural information from SAR, we implement AlphaEarth Satellite embeddings via Google Earth Engine, this will provide a high-latent representation of the landscape. To enforce a robust training signal, we use a 1:1 balance between positive (infected) and negative (healthy canopy) chips. Negative samples are restricted to the NLCD Tree Canopy Cover (TCC) product with a 10% threshold to ensure the model is able to determine ROD from a healthy forest without interference from non-forested land.


---

[[../J-STARS.md|Back to J-STARS]]
