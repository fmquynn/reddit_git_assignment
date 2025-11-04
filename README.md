
# Reddit API Assignment
### Frances Quynn

## Overview
This notebook downloads popular posts about climate, renewable energy, 
and sustainability from Reddit, searches posts with the key word "weather"
and then saves them to a CSV file. The Python script reads in API credentials
(Client ID, Client Secret, User-Agent) from the reddit_api_template.env file to
connect to the API.

## How to Run
1. Prerequisites
 - Python 3.8 or higher
 - Reddit API credentials (client ID, client secret, user agent)
2. Installation
 - pip install -r requirements.txt
3. Configuration: Create a .env file (reddit.env) and put it in the 
   same folder as Python script with the following format:
 - REDDIT_CLIENT_ID=your_client_id_here
 - REDDIT_CLIENT_SECRET=your_client_secret_here
 - REDDIT_USER_AGENT=your_user_agent_here
4. Execution: To execute, enter the command "python reddit_code.py" in your command line.
   If using Google Colab, ensure your Drive is mounted and the .env path is correctly set in your notebook.

## Output
The output file reddit_data.csv includes the following columns:
- "title" of the post
- "score": (# upvotes - # downvotes)
- "upvote_ratio": Ratio of upvotes to total votes
- "num_comments" - number of comments per each post.
- "author": username of the post's author
- "subreddit" - which of the 3 subreddits the post belongs to: climate, RenewableEnergy, or sustainability
- "url" - The URL of the post
- "permalink" - The permanent URL to the Reddit post itself
- "created_utc" - the Unix timestamp of post creation.
- "is_self" - True if the post is text-only, otherwise False.
- "selftext" - The body of the post (truncated to 500 chars)
- "flair" - The category tag assigned to the post (in this case, politics or science)
- "domain" - the domain of the linked content.
- "search_query" - search term that marks posts that contain the keyword "weather". 

Within the file, we see there are a lot of posts on the climate crisis and political
posts about the Trump administration cancelling federal funding for renewable energy projects.
