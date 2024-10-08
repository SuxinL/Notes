# Learn from Others

To learn from others is to understand from materials provided by others, not from our experiences.

## Goals

Deduction is impractical or not enough for knowledge formation.

### Reduction of Cost

Learning from others helps us to establish and fasten a theory efficiently. Theories requires
large amounts of evidence to support like those of nature science including physics, chemistry and biology. A single human has too limited resources of time and money to conduct enough experiments to deduct and support theories. Then we need accumulated wisdom of mankind to quickly get
	
- the theory itself like physics
- evidence for our theory   

For a single experiment, the cost might be too high to pay if without previous knowledge. Disassembling a machine like car engine without knowing its internal structure before can cause bad results like a mess of tiny units and even physical harm to the operator.

### New Thoughts

To get new ideas is another main benefit of referring to others. 

It can help us to notice a more efficient method to finish some work, which we might be never ware of before like an elegant algorithm.

It also reminds us of more factors in problem solving.

## Handling of Mismatch

To handle the difference between our memory and the current knowledge due to

- memory failure
- technology progress

and related anxiety, there are 2 principles.

### Goal Orientation

The questions are: 
- If our knowledge is deemed to be outdated one day, should we learn it?
- What if systems developed by our flawed knowledge cause problems later?

Remember that
- There are no perfect solutions.
- As long as our outdated knowledge has helped us solve problems, it has values. **Incremental Improvement**: It at that time helped us to build our current platform where we improve technologies to continue the iterative progress.

### The Main Structure

To handle tech progress, the main structure is goal oriented. As a result, it is the usual case that the main structure is stable and only the implementation of a specific component improves.

To crack memory failures, The main structure only takes a small portion of our mind load compared to the whole knowledge. **Maintaining the main structure in memory enables us to reuse it quickly for later applications.** Catch and memorize the main structure, and back up it with documentation.

#### Model

The main structure can be specified as

- what
	- what is it?
	- general behaviors
- [purposes](./thoughts/Purposes.md)
	- efficiency
	- security
- context: when & where
- how
	- structure
		- composite: if the system consists of multiple individual functionalities, divide it into modules **based on functionalities** recursively.
		- leaf: For a single-use module, divide it to components **based on dependencies**.
	- behaviors(rules)
		- composite: manages its modules and interactions among
		- leaf: provides services to end users
 

##### category

For different types of knowledge, we focus on different aspects about the **leaf behaviors** in the main model.

- [tools](./models/tool.md#tool)
	- **interface**
		- input
			- instruction
			- object
		- output
			- get
				- source
					- data source
					- **what information is available**
				- presentation
					- filters
					- report format
			- set 
				- what the tool does to the object specifically.
				- philosophy to describe how the tool treats the object.
				- diagrams to group related interfaces.
					- component diagrams
					- data flow diagrams 
					- state diagrams
- practices of doing something
	- use goal achievement model to specify the procedure
	- manage avoidance tips  

## Procedure

Learning is a sub type of goal achievement, then the procedure follows the same framework.

### The initial Test
	
1. set goals in the form of questions about the main structure.
2. test current knowledge by answering these questions.
3. plan what to learn based what questions we can not answer with confidence.

### Acting

1. search materials
	- first-hand evidence: official documents
	- the rule of three if the above one is unavailable.
2. for each article, use
	- catch the TOC, but [not memorize it](./thoughts/Handling_book_TOC.md).
	- critical thinking
	- for each paragraph, 
		- if the contention is clear, skip the path.
		- else understand the **path** and combine it with our knowledge base.
	- after each section, test
		- the main idea
		- **involved operations**
	- after leaning the article, test current main structure
		- whether it is complete and meets our requirements.

### The final Test
	
Retest the main structure of the knowledge.

1. To test our memory, recall the whole main structure in mind
2. Then write it down with details for confirmation and backup 

### Post

After the final test,

- arrange the main structure written down in the final test for later reference when memory fails. 
- apply the knowledge to real-world projects.
