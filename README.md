# SpacetimeCrawler
project framework https://github.com/Mondego/spacetime-crawler

Run generate_crawler_application.py: It will generate files in two folders:
applications/search and datamodel/search with the crawler code in them customized by the details in team.txt.

***
Implemented function extract_next_links (applications/search/crawler_frame.py)
This function extracts links from the content of a downloaded webpage.
Save the details that have been downloaded in your own machine.
Input: raw_content_obj
Output: list of URLs in string form. Each URL should be in absolute form. 
It is not required to remove duplicates that have already been downloaded. The frontier takes care of ignoring duplicates.

Implemented function is_valid (applications/search/crawler_frame.py)
This function returns True or False based on whether a URL is valid and must be downloaded or not.
Input: URL is the URL of a web page in string form
Output: True if URL is valid, False if the URL otherwise. Robot rules and duplication rules are checked separately and should not be checked here. This is a place to
1. filter out crawler traps (e.g. the ICS calendar)
2. double check that the URL is valid and in absolute form. Returning False on a URL does not let that URL to enter your frontier.
