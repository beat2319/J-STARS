## 5m SM S1 high severity detections
- s1 6 channels both ascending and descending orbits vv, vh, rvi 
	- for s1 speckle filtering to the  multi month composites
		- multi temporal lee
		- radiometric terrain correction
	- pre-learned weight at 10m -> projected to 5m res 
		- maybe just moco with resnet-50, or look for resnet-18 with s1
	- binary focal loss
		- 1:20 ratio or just use hyper parameter tuner 
	- use stride when building chips
## 10m IW S2+S1 low to medium severity detections 
- s2 13 channels  + s1 6 channels both ascending and descending orbits vv, vh, rvi and with 16 channel projection of alpha earth or raw 64
	- both S1 and S2 10m pre-learned weights
		- i think I can just use both (if not just use s2 as more channels)
	- for s1 speckle filtering to the  multi month composites
		- multi temporal lee
		- radiometric terrain correction
	- heavy cloud filtering (multi month composites)
		- ```js
			// Harmonized Sentinel-2 Level 2A collection.
			ee.ImageCollection('COPERNICUS/S2_SR_HARMONIZED');
			
			// Cloud Score+ image collection. Note Cloud Score+ is produced from Sentinel-2
			// Level 1C data and can be applied to either L1C or L2A collections.
			ee.ImageCollection('GOOGLE/CLOUD_SCORE_PLUS/V1/S2_HARMONIZED');
		  ```