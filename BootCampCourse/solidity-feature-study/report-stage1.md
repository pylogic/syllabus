This report incluing 2 parts:
-----------------------------

 - this stage's achievements 
 - next stage's plans


----------


***this stage's achievements:***
*1st stage (10.Jul-14.Jul)*

*results (smart contract sources)：*

 - found 567 Ethereum projects. 
 - 308 of them have shared their source code publicly in GitHub. 
 - crawled and extractted all the GitHub links,and stored in 'github_links.txt'(in attachment).

*process & tools:*

 - connect others' server (urllib2) 
 - get and read the contents from others' server (urllib2) 
 - parse the contents, only extract links containing 'github', as the solidity codes we need could be found from them (beautifulsoup) 
 - store the targeted data


----------


***next stage's plans:***

***2nd stage (15.Jul-28.Jul):***

*crawl all the solidity codes:*

 - start from the 308 GitHub links. 
 - recursively crawl, which means the crawling spider should cover all the connective links, until no more new links.

 
*store the data to mongodb:*

 - these data including solidity codes and its attached properties, like sources web sites, project name and so on.

***3rd & 4th stage (29.Jul-25.Aug):***

 - automatically update source and database
 - classify, extract feature, make tag to the solidity codes, by using machine learning algorithm.

