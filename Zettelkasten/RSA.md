## How to represenations in brains and models relate? 
(pp. 1-3)
- we cannot assume a one-to-one correspondency between voxels and model units
- we have many techniques of multi-channel brain-activity measurement which all sample activity patterns fundamentally different
	- invasive electrophysiology
		- ideal modality in terms of resolution in space and time
		- only small quantity of neurons can be recorded
	- scalp eletrophysiology
	- fMRI
		- measures hemodynamic aspect of brain activity
		- rise of oxygen level of brain regions (voxels) comprised of multiple neurons
- it is important to characterize a brains region represenation independent of the modality (technique of measurement)
	- find out how different modalities provide consistent or inconsistent information
-  comparison of activity-pattern dissimilarity matrices does so!

***
## Represenatatonal dissimilarity matrix 
(pp. 2) 
- each cell of matrix contains the dissimlarity between the activation patterns of two different stimuli
- RDM is symmetric
- usage of correlation distance (1-correlation) is recommended
- use it as signature of represenations in brain regions and computational model

***
## Matching dissimilarity matrices: a second-order isomorphism
- First-order isomorphism: reflection of stimulus property in activity level of a neuron
- Second-order isomorphism: establish correspondence between relations among stimuli and between relations among their representation

***
## Representational similarity analysis -step-by-step

### Step 1: Estimating the activity patterns
- record data with stimuli 
- decide on how to estimate the activity pattern of record
- the activity patterns form the bases of representational dissimilarities

### Step 2: Measuring activity-pattern dissimilarity
- compare the activation patterns in terms of dissimilarity
- correlation distance normalizes the mean level of activity
- also possible Euclidean distance, Mahalanobis distance
- assemble all dissimilarities in RDM

### Step 3: Predicting representational similarity with a range of models
- dont really understand the point still have to read about it
- we can evaluate different model types with RSA
#### Complex models

#### Simple computational models
- they provide benchmarks
- the help to characterize information represented in a given brain region

#### Conceptual models

### Step 4: comparing brain and model dissimilarity matrices
- compute dissimilarity of dissimilarity matrices
- compute correlation of upper triangle of RDMs

### Step 5: Testing relatedness of two dissimilarity matrices by randomization
- testing if two dissimilarity matrices are related? what does that mean
- done by random permutation of conditions
- rows and columns are reordered and dissimilarity matrices are compared to this permutation repeating over 10000 times
### Step 6: Comparing RDM with MDS

***
## Upsides and Downsides of RSA
### Upsides
- relates representations from computational modeling, behavioral experimentation, brain-activity experimentation (p. 15)
- provides solution to ==fine-grained spatial-correspondancy problem== when comparing fmRI experiments of different brain regions (p. 15)
	- conventially this was done by transforming data in to different frame, such as: Talairach space, cortial-surface space
- RSA offers way of abstracting of spatial layout with which is an empirical question if it exists (p. 16)
- RSA is able to relate brain data of different modalities and different species (p. 16)
- simulaneously exploit the spatial and temporal richness of multi-channel brain data, but for that we need high-resolution data (p. 17)
- addresses the question how well measured brain-activity patterns represent neuronal patterns (p. 20)

### Downsides
- we need high resolution-data as the input, otherwise there is nothing really to analyse, commonly used fMRi doesn't offer high-resolution

## Further approaches and ideas to use RSA
### Composite modeling of brain's region's representational dissimilarity matrix
- model empirical RDM with combination of model RDMs as linear combination with weights and further methods (p. 16)






