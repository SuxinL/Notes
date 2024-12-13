#  Test Procedures Comparison

When testing whether or not we grasp a word, there are 3 phases:
1. write
2. check
3. update

### Different procedures

When testing a group of words, we might combine some adjacent phases together for each word. As a result, there are following strategies:
- write, check, update
- (write, check), update
- write, (check, update)
- (write, check, update)

## Efficiency Concerns

### Workspace Switch - Share of Common Preparation

The main workspace for each phase is
- write: note
- check: dictionary
- update: note

So the general rule is that grouping repeated actions of a phase helps each of these actions to share the common preparation step (workspace switch). 

Notice that this grouping requires a phase only need the output of its previous phase as its input but not additional knowledge about its previous phase.  

### Reasoning Behind the Answer - Share of Information

Based on the reasoning depth behind the final answer, there are 2 type of knowledge
- one with deep knowledge base.
- one as to which the answer of the problem represents the knowledge 

Nature science belong to the first type. For this type, the answer of a quiz question does not represent the knowledge, but is a result of reasoning from the complex knowledge base containing formulas. Then it is easy to check by comparing our result with the reference answer. But updating our knowledge when our result is wrong requires refine our knowledge base additionally. 

English words belong to the second type. A meaning of word represents the knowledge. For this type of knowledge, check and update are highly coupled and share information. When we find that the reference meaning of a word is different from our knowledge, we can directly use this information to update our knowledge.

## Final Strategy

**write, (check, update)**

- separate write: for group efficiency
- combine check and update: check and update at the same time for word meanings.