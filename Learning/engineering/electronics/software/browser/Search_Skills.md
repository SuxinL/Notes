# Search Skills
- **default: In default, AND search is applied.**
- basic
	- types
		- web
		- image
		- video
		- news
		- map
	- specification
		- start from simple words
			```hungry```
		- add words gradually
			```mechanism of being hungry```
	- words choices
		- use terminology
	- ignore little things
		- spelling: The automatic spelling checker will choose the most commonly used word.
		- capitalization: does not matter.
- advanced
	- operators
		- OR: to narrow the search range to a small group
			```anxiety site:(verywellmind.com OR apa.org)```
		- AND
			- to enforce relationships between items
				```apple AND China```
			- to compare items
				```google AND bing``` 
		- NOT: to exclude some results for a word with ambiguous meanings.
			```amazon -company```
		- group
	- words
		- exact match: to search a professional phrase like error messages
			```"handshake failed; returned -1, SSL error code 1, net_error -100"```
		- wildcard: combined with phrase match, to search lyrics or words that we do not fully remember or are not clear of. (google)
			```"take * roads"```
	- attributes(*name:value*)
		- source: when the builtin search engine of a site is poor, use a general search engine to search a site for the target.
			```anxiety site:verywellmind.com```
		- date: if we want results from a specific time like the most updated research results. (google) 
			- ```anxiety site:verywellmind.com after:2022```
			- ```internet before:2000```
		- scope: search for items within a place of each page
			| scope | google | bing |
			| --- | --- | --- |
			| url | inurl | inanchor |
			| title | intitle | intitle |
			| body | intext | inbody |
		- related: if we know a good site, and we want more similar sites for a more objective view of some topic. (google)
			```related:google.com```
		- cache: if a page is unavailable like being removed or banned.
		- file type: to search academic materials like books.
			```linux filetype:pdf```

<!--stackedit_data:
eyJoaXN0b3J5IjpbNTQ0Njk0NzYzXX0=
-->