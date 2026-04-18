Tues and Thursday
## Exploratory Analysis
Semiovarigram for spatial autocorrelation overtime
temporal autocorrelation
- what is this over different timesteps
- is it important to include a temporal components
- CONV-LSTM is much heavier (wait to do this)
	- CNN-LSTM much more lightweight, shared weight of CONV backbone
	- is NDVI too course for the task 
		- maybe larger areas would work
## Coarse temporal embeddings 
- Location Encoder 
	- climplict location encoding
	- just do this, temp precipitation 
		- rshf repo
	- Satclip use spherical harmonics (be careful)

## S2
include mask layer for certain clouds, algorithms can remove clouds 
- using masking layer with the clouds
- find existing algoritm to work with s2
	- 2 stage data pipeline, this will be alot of work 


---

[[../J-STARS.md|Back to J-STARS]]
