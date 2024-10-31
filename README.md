# Project1-TDS
1. ***An explanation of how you scraped the data***

   I used the REST API documentation and ChatGPT to proceed with REST API.

   To scrape data of GitHub users hailing from Chicago with over 100 followers and their repositories, I used the GitHub REST API.

   I created a Github personal token access to authenticate the requests.

   This query was formatted as q=location:Chicago+followers:>100 for the users.

   Data was retrieved in json format and then processed in to a pandas dataframe upon which analysis was done.

   The repository data was retrived using REST API but with user login information previously retrieved.

2. ***The most interesting and surprising fact you found after analyzing the the data***

   The regression slope between length of bio written by the user and the followers is about 7, is huge. Which means writing a bigger bio will actually get you more followers. Also, it can be analysed that people with bigger bios are the ones who produce the best quality content helping them gain more followers. This can be looked upon next time I analyse a user.

   While making a request to Github, it maintains a dictionary of the first page, last page, current page, previous page and next page numbers. So we can track where we are and when to stop a loop based on this information. This is useful because REST API returns only 30 entries per page. 

3. ***An actionable recommendation for developers based on your analysis***

   I have used dataframes in pandas and it is timetaking to run code for 1000's of lines. Use DuckDB in place of dataframes. It is also easily compatible with dataframes and csv. It reduces time drastically.

   Using a personalized token for the API request increases the no of requests you make to about 15000 per hour compared to just requesting it.


  
