- Slides
	- ![04slides.pdf](../assets/04slides_1706012197241_0.pdf) J&M3 4.7-4.10
-
-
- # Annotation
	- ## Factors in Annotation
		- ((65afae75-9a67-403e-b25c-f997550a1713))
		-
	- ## Annotation Scheme
		- Some kinds of annotation are straightforward for most inputs
		- ### Others.. are not
			- *Yesterday* was my birthday
			- *Yesterday* I ate cake
			- We have been *walking* quite quickly | Verb
			- *Walking* was the remedy | Noun
			- We all lived within *walking* distance | Adjective
		- ### Why so complicated?
			- Human language needs to be flexible, it cuts corners and is reshaped over time
		- ### Annotation Quality
			- Follows guidelines
			- However errors occur:
				- Simple | Wrong Button
				- Not reading full context
				- Erroneous pre-annotation
				- Forgetting guidelines
				- Cases not anticipated by or amniguous in guidelines
			- How to measure quality?
	- ## Inter Annotation Agreement (IAA)
		- ### The essence
			- Estimates reliability
			- Annotate a common example, and measure agreement
			- Raw agreement rate, proportion of labels in agreement
			- In theory they agree 100%
			- Examine source of disagreement
				- COnsider additional training
				- Changing guidelines
			- This rate is the upper bound, human ceiling
		- ### Better
			- The raw rate counts all annotation decisions equally
			- However not all equal
		- ### Crowdsourcing
			- Quality control is even more important
			- You can pay people small amounts of money for small amounts of work
			- Need to make sure they are qualified
			- cost vs quality
			- Sometime quality lowers over time
-
- # Evaluation
	- The scientific method rests on making and testing hypotheses
	- (Basically eval is testing)
	- Not just for public view
		- How internal development was managed
		- And how systems improve themselves
	- ## Gold Standard
		- The best judgement as to what is correct
		- Used for training and evaluation
		- Testing must be done on unseen data
	- ## Tuning
		- Trying several configuration options and choosing the one that works best
		- Risk of overfitting!!
		- ((65afb5cb-87b9-4a0e-a449-4908d5505702))
		- Can be wasetful if dataset is small
		- ### $k$-fold Cross-validation
			- Partition into $k$ peices as mini-sets
			- Each fold is an experiment with a different held out set
			  ((65afb63b-2399-46de-9afe-90dce6da7426))
			- After $k$ fold, every point will have a held-out prediction
			- Still good to have a blind test set
			- Make $k$ as big as you can
	- ## Measuring Performance
		- ### Accuracy
		  $$\dfrac{|right|}{|test-set|} \times 100$$
		- ### Precision